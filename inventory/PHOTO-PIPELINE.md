# Photo capture and inventory recognition

## The honest promise
Photos can create a useful **inventory draft**. They cannot document a kitchen perfectly. The product must measure success by how little confirmation work remains, not by claiming every object was recognized.

## Why one fridge photo fails
- Occlusion: front-row objects hide the rest.
- Packaging ambiguity: similar cartons, tubs, bags, and leftovers share visual shapes.
- Date visibility: expiration labels are small, curved, reflective, or on another side.
- Quantity ambiguity: a box can be full, nearly empty, or contain something else.
- State ambiguity: an unopened product and Tuesday’s leftovers need different shelf-life logic.
- Duplicate views: overlapping photos can count the same milk or jar twice.
- Container opacity: vision may know “plastic container,” while the useful fact is “cooked chicken from Tuesday.”
- Produce identity and condition: bags, drawers, lighting, and condensation obscure both.
- Inventory drift: consumption, freezing, cooking, and household actions quickly make a perfect scan stale.

## How existing products make it seem easier
Most combine several imperfect sources:
- object detection and multimodal language models for visible items
- OCR for package names, receipts, and dates
- barcode databases for exact packaged products
- category shelf-life defaults
- user confirmation and manual correction
- recurring reminders to rescan or resolve items

Marketing usually shows a clean, front-facing grocery haul. Real refrigerators require multiple views and confirmation.

## Body Kitchen capture flow

### 1. Guided coverage
The app asks for a small sequence rather than an undirected video:
1. top and middle shelves
2. lower shelf and drawers
3. door shelves
4. freezer
5. optional leftovers close-up

A coverage map shows what is done. The user can stop after any step; partial capture remains useful.

### 2. On-device quality gate
Before upload:
- blur and exposure checks
- warn when labels occupy too few pixels
- detect extreme overlap or an obstructed lens
- identify likely duplicate frames
- crop obvious empty borders

Failed quality checks are suggestions, not blockers.

### 3. Proposal extraction
Each image produces candidates with:
- bounding box or segmentation mask
- proposed normalized food name
- package/product text from OCR
- location zone
- quantity range
- opened/leftover clues
- date text candidates
- confidence by field
- image and crop provenance

The model returns proposals, never committed inventory rows.

### 4. Cross-view fusion
Candidates are merged using visual embeddings, product text, spatial location, timestamps, and overlapping scene geometry. A milk carton visible in two shelf photos becomes one proposal with two source crops. Conservative fusion is safer than aggressive merging because duplicate suggestions are easy to dismiss; a silently lost item is invisible.

### 5. Product resolution
When a barcode is visible, query Open Food Facts first. Nutrition and category defaults can fall back to USDA FoodData Central. OCR product names are matched against those catalogs. User corrections become household aliases, such as a recurring restaurant container or preferred yogurt.

### 6. Expiry reasoning
Dates carry a source:
- package date read by OCR
- user supplied
- receipt purchase date
- cooked/opened event
- category estimate

Exact dates are shown only when supported. Otherwise the interface says “check this week” or “date unknown.” Food-safety rules remain separate from freshness and waste-reduction estimates.

### 7. Confidence-shaped review
High confidence: grouped quick accept.
Medium confidence: tap between two likely names or quantities.
Low confidence: crop plus one short question.
Opaque leftovers: “What is this?” with voice reply and optional cooked date.

The review queue prioritizes information that changes action. Exact grams of rice can wait; whether a container is raw chicken or cooked tofu cannot.

### 8. Drift correction
Inventory stays useful through events:
- consumed, cooked, frozen, discarded
- receipt or barcode additions
- household member changes
- small “still here?” cards
- quick rescans of one shelf rather than the whole kitchen

The app learns disappearance rates and recurring staples but never silently deletes uncertain food.

## What we can do better

### Optimize for decisions, not catalog completeness
An 80% draft that reliably catches urgent food is more valuable than a brittle 98% catalog that takes ten minutes to correct.

### Ask fewer, more consequential questions
Use expected information gain. Ask about identity, opened/cooked state, and dates when the answer materially changes urgency or safety. Defer brand and precise quantity.

### Let receipts establish priors
A grocery receipt says what probably entered the home. Shelf photos then confirm location and remaining presence. This is stronger than vision alone.

### Remember the household’s containers
If the same glass container usually holds meal-prepped chicken, suggest it with household-specific confidence while still asking for confirmation.

### Make uncertainty visible
Every inferred field can show its source and confidence. Users should understand why the app thinks something is urgent.

### Support variable effort
Capture can end after one shelf. Review can be done later. A user can say “accept all obvious packaged items” and leave leftovers unresolved.

### Learn from resolutions
When a user marks an item eaten, frozen, or discarded, that outcome improves ranking and reminder timing. Personal behavior should tune prompts, not fabricate food-safety certainty.

## Proposed technical pipeline

```text
iOS guided capture
  -> on-device blur/exposure/duplicate gate
  -> direct encrypted object-storage upload
  -> capture job + image manifests
  -> OCR / barcode / object proposals in parallel
  -> cross-view fusion
  -> product catalog resolution
  -> expiry-source rules
  -> ranked review queue
  -> confirmed InventoryEvents
  -> current inventory projection
```

### Service boundaries
- `capture-api`: signed uploads, manifests, job status
- `vision-worker`: image proposals and crops
- `ocr-worker`: package/date/receipt text
- `catalog-service`: Open Food Facts and USDA adapters
- `fusion-worker`: cross-view deduplication
- `inventory-service`: confirmation and event ledger
- `ranking-service`: use-first and meal scoring

### Proposal contract
```json
{
  "proposal_id": "uuid",
  "capture_id": "uuid",
  "zone": "fridge.middle_shelf",
  "sources": [{"image_id":"uuid","box":[0.12,0.18,0.31,0.56]}],
  "fields": {
    "name": {"value":"Greek yogurt","confidence":0.92,"source":"vision+ocr"},
    "quantity": {"value":3,"unit":"cup","confidence":0.63,"source":"vision"},
    "date": {"value":null,"confidence":0,"source":"unknown"}
  },
  "possible_duplicate_of": null,
  "review_priority": 0.41
}
```

## Cost and privacy controls
- Resize and compress on device; upload full resolution only for date/barcode crops when needed.
- Run cheap quality, barcode, and OCR stages before a multimodal model.
- Batch images from one zone so the model has scene context.
- Cache product resolution by barcode and normalized text.
- Delete original images after extraction by default; retain proposal crops only while review is open.
- Let users opt into saving originals for future rescans.
- Never use kitchen photos for model training by default.
- Strip image metadata that is not needed and encrypt transport/storage.

## Evaluation
Build a consented test set of real, messy kitchens with item-level ground truth. Report:
- visible-item recall
- proposal precision
- duplicate and mistaken-merge rates
- exact product resolution rate
- date extraction precision
- median review actions per confirmed item
- time from first photo to useful queue
- urgent-item recall
- correction rate by food category and lighting condition

The key product metric is **confirmed useful items per minute of user effort**. The safety guardrail is false confidence on identity, date, and raw/cooked state.

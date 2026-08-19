# Body Kitchen: product blueprint

## Product sentence
A kitchen memory system that notices food before you forget it and turns the food you have into a meal you can handle today.

## Audience and wedge
Launch for adults with ADHD, autistic adults, burned-out caregivers, and anyone whose executive function changes day to day. The public category is food inventory and meal planning. The sharp entry point is “I bought food, forgot it existed, and ordered delivery anyway.”

The product is useful without diagnosis or disclosure. Accessibility appears in the interaction model: recognition over recall, low-decision defaults, interruption-safe drafts, forgiving estimates, variable-effort recipes, and no shame loops.

## Core loop
1. **Capture:** point the camera at a fridge shelf, freezer drawer, grocery haul, barcode, or receipt. Voice and manual quick-add remain first-class.
2. **Confirm:** the app presents a short review queue, grouped by confidence. One swipe accepts; uncertainty is visible.
3. **Notice:** a use-first queue shows only the food that needs a decision soon.
4. **Choose:** recipes rank by food urgency, current energy, time, equipment, sensory preferences, protein goal, and missing ingredients.
5. **Resolve:** cooked, eaten, frozen, discarded, or “still here.” Inventory and waste learning update from that action.

## The differentiators

### Fridge photo becomes a living draft
Computer vision proposes products, produce, containers, and rough quantities. It never silently pretends to know exact expiry dates. The user can say “all of that except the sauce” or “those are leftovers from Tuesday.”

### Effort is an input
Every cooking suggestion has an effort profile:
- **Open and eat**
- **Assemble**
- **Microwave / one pan**
- **I can cook today**

Energy can be changed with one tap. The meal list re-ranks immediately.

### Food has states, not just dates
`fresh → use soon → decide today → frozen/used/discarded`. Opened date, cooked date, and confidence matter. “Check today” is used when a precise safety claim is not supportable.

### Rescue mode
A guided five-minute sweep: choose one urgent item, select cook/freeze/eat/compost, then stop. No demand to clean the whole fridge.

### Household memory
Optional shared kitchen with roles, duplicate-purchase warnings, “someone plans to eat this” holds, and non-annoying notifications. Changes are attributed and undoable.

### Body integration
With explicit permission, meal suggestions can consider the user’s macro target, appetite, workout/recovery context, and known food preferences. The paid standalone product must work fully without health data.

## App information architecture

### Today
Use-first queue, one recommended meal, latest captures waiting for review, quick actions.

### Kitchen
Fridge, freezer, pantry, leftovers. Search, filters, item detail, edit history, household ownership.

### Cook
Energy selector, time, available equipment, dietary/sensory filters, recipes ranked by pantry coverage and urgency. Missing items can become a shopping list.

### Shop
Shared list, duplicate detection, staple reminders, receipt import, store mode. Purchased items enter the capture review queue.

### Me
Preferences, household, nutrition connection, notification budget, privacy controls, subscription, export/delete.

## Capture stack
1. Manual and voice quick-add
2. Barcode via Open Food Facts, with USDA FoodData Central fallback for nutrient data
3. Receipt OCR and parsing
4. Multi-item fridge/haul photo recognition
5. Email receipt integrations where users explicitly connect an account
6. Optional smart-fridge and retailer integrations only after the core loop proves retention

Canonical inventory stays in our database. Public datasets supply product metadata, never personal history.

## Safety and trust
- The app does not certify that food is safe to eat.
- Expiry estimates show source and confidence: package date, user statement, receipt inference, or category default.
- High-risk foods use conservative prompts and official food-safety guidance.
- AI recognition always has a review state and original image provenance.
- Nutrition estimates remain distinct from official package facts.
- Full account export and deletion are available in-app.
- No sale of household, food, health, or behavioral data.

## Paid App Store model

### Free
One kitchen, manual/barcode capture, use-first queue, basic recipes, limited photo scans each month.

### Plus: proposed $5.99/month or $39.99/year
Unlimited photo and receipt capture, household sharing, advanced rescue recipes, history, nutrition-aware ranking, home-screen widgets, and pantry sync across devices.

### Founding lifetime
A limited early-adopter offer can finance inference costs and create a committed testing cohort. Do not promise lifetime cloud AI without a fair-use clause.

Annual is the default highlighted plan. Subscription value comes from ongoing capture automation and household coordination, not locking the user’s own inventory behind payment.

## App Store readiness
- Native-feeling iOS app built with Expo React Native for product speed; native Swift modules for VisionKit, barcode scanning, widgets, share extensions, and App Intents as needed.
- Sign in with Apple plus optional email magic link.
- StoreKit 2 through RevenueCat initially, with server-side entitlement verification.
- Accessibility labels, Dynamic Type, VoiceOver, reduced motion, color-independent urgency states, 48pt targets.
- Privacy nutrition labels mapped from real data flows.
- Account deletion inside the app.
- Offline writes and conflict-safe household sync.
- Background notifications respect a user-defined notification budget.

## Technical architecture

### Client
Expo React Native + TypeScript; Expo Router; SQLite local cache; TanStack Query; Zustand only for ephemeral UI state; camera and photo picker; native widgets later.

### API
FastAPI or TypeScript service behind versioned REST endpoints. PostgreSQL with row-level household authorization. Object storage for images with short retention after extraction unless the user saves originals. Background jobs for OCR, vision, product lookup, and recipe indexing.

### Core entities
`User, Household, Membership, StorageZone, FoodItem, Lot, Capture, CaptureProposal, Product, InventoryEvent, Recipe, RecipeIngredient, Preference, MealResolution, ShoppingItem, Entitlement, NotificationBudget`.

Inventory is event-backed. `InventoryEvent` records add, adjust, open, freeze, cook, consume, discard, restore, and household transfer. Current state is a projection, which keeps undo and sync reliable.

### AI boundary
A provider-neutral extraction contract returns proposals with bounding boxes, normalized names, quantity ranges, confidence, and unresolved questions. Rules and retrieval handle expiry defaults. Recipe ranking is explainable scoring before generative rewriting. Personally identifying images are never used for model training by default.

### Suggested repository
```
apps/mobile          Expo iOS/Android app
apps/body-miniapp    Telegram proving ground
apps/api             API and auth
packages/domain      schemas and inventory rules
packages/ui          accessible shared tokens/components
packages/vision      provider-neutral capture contracts
packages/catalog     Open Food Facts/USDA adapters
infra                 deployment and observability
```

## Delivery sequence

### Phase 0: Body proving ground, now
Use-first inventory, quick add, local persistence, easy meal ranking, Telegram event return.

### Phase 1: Private alpha
Real image capture and review, backend sync, item editing, barcode lookup, expiry confidence, telemetry, 20–40 design partners.

### Phase 2: TestFlight
Receipt import, household sharing, rescue mode, notification budget, paywall experiments, crash/error observability, privacy controls.

### Phase 3: App Store launch
Subscription, onboarding variants, widgets, referral loop, creator launch cohort, App Store assets and support operations.

### Phase 4: Retention moat
Preference learning, retailer receipts, seasonal rescue packs, household behavior, local-first recipe ranking, integrations.

## Product metrics
North star: **food decisions resolved per active kitchen each week**.

Activation: first capture reviewed + first item resolved within 48 hours.
Retention indicators: use-first queue opens, captures reviewed, meal suggestions acted on, food frozen/used, shopping duplicates avoided.

Guardrails: review corrections, false expiry confidence, notification disables, capture abandonment, image processing cost, support requests, and account deletion rate.

Avoid vanity “money saved” claims unless computed from user-confirmed prices and resolutions.

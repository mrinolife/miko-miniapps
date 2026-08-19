# Body Kitchen: product blueprint

## Product sentence
A recipe memory and kitchen companion that starts with food you already want, makes it easier for the effort you have today, and gradually learns what is at home.

## Onboarding wedge: desire before inventory
The first-run experience asks for recipes, cravings, and foods the user already likes. They can paste TikTok, Instagram, YouTube, and web links; share a post into the app; add a screenshot; dictate an idea; or type messy text. Body Kitchen stores the source, extracts a recipe draft when permitted, and keeps an unresolved save useful even when extraction fails.

Inventory is introduced later as a way to answer specific questions: “Can I make this?”, “What substitute do I have?”, and “What should I buy?” Quick photo capture is offered contextually from a saved recipe or shopping trip. A user can keep a recipe box without cataloging their kitchen.

The recurring delight loop is an effort-filtered **Dinner Draw**. It reveals one saved or compatible recipe with a tactile animation. The draw honors energy, time, sensory preferences, equipment, dietary needs, and available ingredients; it never chooses from food the user has rejected.

## Audience and wedge
Launch for adults with ADHD, autistic adults, burned-out caregivers, and anyone whose executive function changes day to day. The public category is food inventory and meal planning. The sharp entry point is “I bought food, forgot it existed, and ordered delivery anyway.”

The product is useful without diagnosis or disclosure. Accessibility appears in the interaction model: recognition over recall, low-decision defaults, interruption-safe drafts, forgiving estimates, variable-effort recipes, and no shame loops.

## Core loop
1. **Want:** save a recipe, social post, craving, screenshot, or rough meal idea. The source remains attached and creator attribution is preserved.
2. **Shape:** extract a recipe draft where platform access permits, then offer effort modes, substitutions, equipment changes, and sensory/dietary adjustments.
3. **Choose:** use Dinner Draw or browse by current energy and time. The reveal is playful; the candidate pool stays predictable and user-controlled.
4. **Connect:** show what is probably available, what is missing, and substitutions. Invite quick inventory capture only when it reduces work for this recipe.
5. **Resolve:** cook, save for later, add missing items to shopping, or choose something easier. Inventory learns naturally from confirmed purchases and cooking events.

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

## Fair paid App Store model

### Principle
Free solves the complete basic problem. Plus removes labor, coordinates households, and pays for ongoing AI/cloud work. Accessibility, food urgency, safety context, corrections, export, and deletion never sit behind the paywall.

### Free: a useful kitchen, indefinitely
- One kitchen on one primary device
- Unlimited manual and voice quick-add
- Unlimited barcode lookup
- Full fridge/freezer/pantry inventory
- Use-first queue and expiry-source/confidence display
- Basic effort-aware meal suggestions
- Rescue Mode
- Shopping list
- Offline use, reminders, widgets, accessibility controls, and notification budget
- Inventory corrections, undo, full export, and account deletion
- A recurring allowance of guided AI capture **sessions**, counted per fridge/receipt session rather than per image; retries and quality-check failures never consume allowance
- One optional household partner with basic shared inventory so couples do not have to pay merely to coordinate

Free users keep confirmed inventory after the AI allowance is used. They can continue entering, editing, resolving, and exporting food without interruption.

### Plus: proposed $4.99/month or $34.99/year
- Generous high-volume photo and receipt recognition under a transparent fair-use policy
- Automatic cross-photo merging and advanced receipt reconciliation
- Multi-device sync and larger households
- Shared assignments, holds, activity history, and duplicate-purchase warnings
- Advanced preference learning and nutrition-aware ranking
- Full inventory and waste-history insights
- Recipe adaptation, batch rescue planning, and richer household meal coordination
- Priority processing during high demand

At $34.99, annual is about $2.92/month and 41.6% below twelve monthly payments. Test willingness to pay before launch rather than treating this as final pricing.

### Avoid meter anxiety
- Show the allowance before capture starts, in plain language.
- Count one guided sweep as one session even when it contains several photos.
- Never charge for blurry shots, upload failures, model failures, or retries.
- Give a soft warning before the limit; never reveal a hard stop after the user has completed the work.
- Keep a small emergency/rescue allowance so a free user can scan urgent groceries after reaching the normal cap.
- Let unused allowance roll over modestly without creating a game-like balance users must manage.

### Trial and billing ethics
- Let people experience successful capture and review before showing the paywall.
- Offer a seven-day Plus trial only after the user chooses a Plus feature.
- State the exact renewal date and price on the trial screen and send an optional reminder before renewal.
- No countdown timers, preselected annual plan, disguised close button, guilt copy, streak loss, or repeated full-screen paywalls.
- Make downgrade and cancellation easy to find. A downgrade preserves all user data and converts the kitchen to free limits.
- Honor Apple Family Sharing when unit economics permit.

### Access program
Provide renewable sponsored Plus access through creator codes and partner organizations for users facing financial hardship. Keep eligibility lightweight and private; do not require diagnostic paperwork. Students and disability/community partners can receive longer trials or discounted annual access. Measure abuse quietly without treating every user as suspicious.

### Founding plan
A limited founding purchase can finance development and create a committed testing cohort. It should promise lifetime access to the core paid software features, while unusually expensive third-party AI can remain subject to a clearly stated generous fair-use limit. Never advertise unlimited lifetime cloud inference.

### What we do not monetize
No advertisements, sponsored recipe ranking, grocery-brand placement disguised as advice, or sale of household, food, health, or behavioral data. Affiliate shopping links, if ever added, are optional, clearly labeled, and never alter the use-first ranking.

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

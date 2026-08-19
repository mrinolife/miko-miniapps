# Neurodivergent cooking and meal-planning: evidence, lived experience, and product opportunities

**Research date:** 19 August 2026

**Scope:** ADHD, autism, sensory food preferences, and the design of recipe-saving, planning, grocery, and cooking tools. This is product research, not medical or nutrition advice. “Neurodivergent” is used broadly and does not imply that every autistic or ADHD person has the same needs, that a person needs a diagnosis to benefit from an accommodation, or that a product can infer a user’s abilities from a label.

## Executive summary

Meal planning is usually described as a content and logistics problem: find recipes, put them on a calendar, create a list, cook. For many people it is also a repeated chain of executive, sensory, energy, and body-signal demands. The chain includes noticing a need to eat; stopping another activity; choosing a tolerable meal; estimating time and effort; locating ingredients and equipment; sequencing preparation; monitoring heat and timers; tolerating sound, smell, touch, and uncertainty; storing leftovers; and doing it again. Failure at any link can make an otherwise good recipe library or grocery-list generator feel unusable.

There is established evidence that, at group level, ADHD is associated with executive-function and time-perception differences, and that autistic people have a higher prevalence of food selectivity that is often related to sensory processing. There is useful but incomplete evidence on interoception. In contrast, claims such as “all autistic people need safe foods,” “ADHD people cannot meal plan,” or “demand avoidance is a settled autism subtype” are not established facts. The relevant needs vary within and across people, and can shift with stress, illness, sensory load, medication, hunger, money, and available support.

Existing mainstream apps are strong at recipe capture, calendar planning, ingredient consolidation, dietary/allergen filters, sharing, and sometimes food-waste optimisation. They are weaker—at least in their publicly documented feature sets—at representing *state-dependent capability* and sensory experience. A weekly plan typically assumes the user can execute a selected recipe on the assigned day. It rarely offers a genuine “today I have 2/5 energy” adaptation, an ingredient-level texture/smell/temperature profile, a no-judgment rescue route, instruction variants for low working memory, or a personal memory of what a recipe was actually like in this kitchen.

The clearest opportunity is not a generic “AI meal planner.” It is a user-controlled **adaptive meal system**: one that records trusted foods and sensory constraints in the user’s own words; lets a plan degrade gracefully from cook-from-scratch to shortcut to ready-to-eat; externalises time, steps, and perishable inventory; and makes the next possible action visible without turning eating into a compliance task. Community features matter when they transmit credible first-person adaptations—substitutions, sensory notes, reheating reality, and low-energy routes—rather than presenting an unmoderated stream of aspirational recipes.

## Method and evidence labels

This report combines four evidence types. They are intentionally kept separate.

1. **Established/reviewed evidence** means peer-reviewed systematic reviews, meta-analyses, or well-supported clinical/public-health material. It supports population-level patterns, not a prediction about an individual.
2. **Direct qualitative evidence** means research that analyzes autistic adults’ accounts or other primary qualitative research. It is evidence of reported experience, but not a prevalence estimate.
3. **First-person community evidence** means public posts by people describing themselves as autistic, ADHD, or AuDHD. It is useful discovery research for language, friction points, and workarounds. It is self-selected, unverified, and not representative; it must not be treated as clinical evidence.
4. **Product-documentation evidence** is what vendors say their products do in their current public pages/help centers. It is not an independent usability or accessibility audit. “Not documented” does not prove a feature is absent; it indicates that it was not visible in the reviewed material.

The comparison covers Paprika, AnyList, Mealime, and Samsung Food because they represent common patterns: personal recipe-box tools, shared-list/planner tools, curated meal-plan generators, and social recipe platforms. Public sources and apps change frequently; links below are the source of truth for a feature claim.

## What the evidence actually supports

### Executive function, working memory, initiation, and decisions

Executive function is a family of processes used to plan, hold information in mind, begin and switch tasks, regulate attention, and monitor progress. It is not a measure of intelligence or motivation. A large direct-comparison meta-analysis reported that ADHD and autism groups, on average, performed worse than typically developing comparison groups across several domains including attention, flexibility, working memory, processing speed, and inhibition; the two diagnostic groups did not differ in planning in that analysis ([peer-reviewed article](https://doi.org/10.1177/10870547231190494)). This is an important corrective to simplistic “ADHD versus autism” feature mapping: individual assessment and context matter more than a stereotype.

For cooking, working memory matters because the cook has to retain an instruction while locating an ingredient, remember whether an ingredient has already gone into the pan, and reconcile the ingredient list with the procedure. Experimental instruction-following research describes working memory as a limited system for holding and manipulating information and explicitly names cooking from a recipe as an everyday example ([Scientific Reports](https://www.nature.com/articles/srep17657)). This does **not** establish that any one person who loses their place has ADHD or autism. It does establish a general human constraint that a product can reduce through external supports.

Task initiation is especially relevant because a meal is not a single task. “Make dinner” contains deciding, standing up, walking to the kitchen, locating food, washing, chopping, heating, monitoring, plating, eating, and cleaning. A product that only sets a 6 p.m. recipe reminder still leaves the activation energy intact. The most defensible design response is to split a task into reversible, concrete actions (“open freezer,” “choose one of three,” “put rice in microwave”), allow stopping, and preserve progress. Do not frame this as a moral failure or use streak loss as a penalty.

Decision paralysis is a plausible product-level consequence of a huge recipe catalog plus uncertain appetite, effort, and sensory tolerance. It is not a diagnostic criterion. Apps should treat it as an interface problem: reduce the option set, make the criteria visible, and offer a satisfactory default that the user can reject. A “surprise me” control is only helpful when it is constrained by trusted foods, current energy, pantry state, and stated dislikes—not when it produces novelty for novelty’s sake.

### Time perception (“time blindness”) and cooking time

“Time blindness” is popular lived-experience language, not a formal diagnostic label. It should not be dismissed, though: a 2024 systematic review and meta-analysis of ADHD time perception found an overall difference across 824 effect sizes (mean *g* = 0.688), with moderators including age and working memory ([PubMed record](https://pubmed.ncbi.nlm.nih.gov/38145491/)). An adult-ADHD review also notes mixed results across individual studies, which argues for careful language rather than certainty about every user ([full review](https://pmc.ncbi.nlm.nih.gov/articles/PMC9962130/)).

In a cooking product, the practical implication is to externalise *time-to-first-bite*, active minutes, passive minutes, unavoidable waits, and latest-start time. “30 minutes” is too coarse if it excludes preheating, washing, chopping, locating a pan, cooling, or dishes. A user who starts at 6:45 may need an automatic alternate route: “Your selected meal is estimated 55–70 minutes including prep. Here are three 10-minute plans using the same groceries.” Timers should be named by action, survive app navigation, permit pausing/adding time, and warn about simultaneous deadlines.

### Sensory preferences, food selectivity, and predictable food

The evidence base most clearly supports a relationship between autism, sensory processing, and eating behavior. A systematic review found that atypical eating behaviors, particularly food selectivity, were consistently correlated with sensory-processing differences; it also stresses that the reviewed evidence was child-heavy and included no adult participants in that review ([review](https://pmc.ncbi.nlm.nih.gov/articles/PMC9545673/)). A newer systematic review of food selectivity in autism reports that smell, texture, taste, color, and temperature can be relevant and that severity and impact vary widely ([review](https://pmc.ncbi.nlm.nih.gov/articles/PMC12304907/)). Adult-specific evidence is still comparatively sparse, so adult design should be built with adults, not inferred from child feeding studies.

The product conclusion is **not** “make bland food” or “filter out vegetables.” Sensory experience can involve seeking as well as avoiding intensity; a person may prefer crunchy, spicy, hot, visually separated, strongly flavored, predictable, or novel food. Preferences can also be medical, cultural, ethical, financial, religious, trauma-related, or simply personal. The right data model is ingredient/technique-specific and editable: for example, “raw onion: no,” “onion powder: yes,” “mushroom texture: no,” “crisp roasted mushrooms: maybe,” “foods touching: fine only in bowls,” “needs a crunchy element,” “leftovers change texture: unacceptable.” A Boolean “dislike onion” field cannot capture this.

“Safe food” is community language, not a clinical prescription. In a product it can be respectfully implemented as **trusted/reliable food**: an accessible personal collection with no pressure to expand variety. A separate, opt-in “curious to try” collection can support gradual experimentation. Never score a person down for repeating a meal, and never make novelty a required health goal.

### Interoception, hunger, thirst, and the moment a plan becomes irrelevant

Interoception includes sensing internal bodily signals such as hunger, thirst, fullness, temperature, and discomfort. It is tempting to claim a simple autism-to-poor-interoception relationship, but the science is more nuanced. A recent systematic review/meta-analysis found inconsistent results across interoception studies; its meta-analysis of five adult studies using comparable cardiac-interoception tools found no statistically significant autism/non-autism difference ([review](https://pmc.ncbi.nlm.nih.gov/articles/PMC12406136/)). A systematic review of interoception in ADHD found evidence still emerging and describes possible links with ADHD symptoms, while emphasizing heterogeneity and measurement limitations ([review](https://pmc.ncbi.nlm.nih.gov/articles/PMC11842156/)).

There is nevertheless direct qualitative evidence worth hearing. A study analyzing self-identified autistic adults’ texts found many accounts of limited awareness of hunger, satiation, or thirst and associated eating difficulties; it calls for better measures, not for universal assumptions ([PubMed abstract](https://pubmed.ncbi.nlm.nih.gov/33389300/)). A meal product should therefore offer optional, neutral body-check prompts (“Would food, water, a snack, or no action help right now?”) and scheduled supports chosen by the user. It should not diagnose hunger, impose calorie targets, shame missed meals, or tell a user to override discomfort.

### Demand avoidance: useful experience term, unsettled diagnostic claim

Some people describe cooking, even self-chosen cooking, becoming aversive once it feels like an obligation. The need for autonomy, low-pressure language, and alternate paths is a legitimate design consideration regardless of diagnosis. However, **PDA/pathological demand avoidance is not an established separate autism diagnosis or validated subtype.** The UK National Autistic Society states that demand avoidance is widely reported/observed in some people, but that research has not found strong evidence for the proposed PDA trait group or established its clinical validity/usefulness ([NAS guidance](https://www.autism.org.uk/advice-and-guidance/behaviour/demand-avoidance)). A 2024 scoping review likewise highlights limited and contested methods ([Frontiers review](https://www.frontiersin.org/journals/education/articles/10.3389/feduc.2024.1230011/full)).

Design implication: provide autonomy-supportive interaction because it can help many users. Prefer “Pick a route that fits,” “Save for later,” and “What sounds possible?” over “You must cook tonight” or a punitive overdue alert. Do not label a user PDA or market an unvalidated clinical solution.

### Variable energy and capacity

“Energy” is a useful self-report of present capacity, not a stable trait or a diagnosis. Capacity can vary with sleep, pain, sensory overload, work, caregiving, mood, medication, illness, heat, and access to equipment. The research above supports the need to avoid one-size-fits-all assumptions; first-person accounts make the day-to-day variability especially visible. A viable system should plan for reality rather than consider deviations from a Sunday plan as failures.

An **energy ladder** is a stronger abstraction than a “healthy versus unhealthy” split:

| Route | Example product meaning |
| --- | --- |
| Ready now | a trusted shelf-stable, refrigerated, or freezer meal/snack; no prep stigma |
| Heat/assemble | microwave, toaster, kettle, bagged salad, pre-cooked components |
| Shortcut cook | frozen/pre-chopped/pre-marinated components, one pan/appliance |
| Full recipe | original recipe, prep and cleanup included |

The user should decide what counts at each level. A product can offer swaps and keep a plan’s nutrition/allergen information honest, but should not imply that a freezer meal is a personal failure.

## Clearly labeled first-person community evidence

The following observations are **anecdotes, not prevalence claims**. They are selected because the same product implications recur across threads, not because Reddit is a representative sample. Posts can be deleted or edited; identifiers are intentionally omitted.

* In an [r/AutisticWithADHD discussion](https://www.reddit.com/r/AutisticWithADHD/comments/1fps6p6), a poster described sensory sensitivities and the executive load of choosing a cuisine/meal; a pre-made plan could fail when the day required a lower-energy meal or takeaway. This supports flexible plan substitution, not the claim that plans never work.
* In an [r/AutismInWomen thread](https://www.reddit.com/r/AutismInWomen/comments/1n32yep), contributors described needing food immediately when hungry, using batch-cooked lunches, freezer items, pre-chopped food, steam-in-bag vegetables, and air-fryer options. One person also reported being sensory-seeking and unable to tolerate the same daily meal. The key pattern is that “easy” and “repetitive” are individual, not universal.
* In an [r/AutisticAdults thread](https://www.reddit.com/r/AutisticAdults/comments/1uuh9bj), a contributor separated difficulty with preparation/executive load from sensory issues and described needing recovery after cooking. A tool should therefore not treat sensory filters as the only accommodation.
* In another [autistic-adult conversation](https://www.reddit.com/r/AutisticAdults/comments/1po1nno), people described both reliable breakfasts/meal rotations and deep enjoyment of cooking or food as a special interest. Some kept many frozen dinners; another became bored quickly. Product choices should preserve both predictability and exploration.
* A [neurodiversity recipe-tool thread](https://www.reddit.com/r/neurodiversity/comments/1rud5ue) includes a first-person preference for flow-chart-like instructions because ordinary recipes made the person lose their place and reread. This aligns with HCI research on reducing split attention; it does not establish that flow charts suit all neurodivergent cooks.
* Community evidence also shows that an ordinary app can be helpful. In an [ADHD post about Mealime](https://www.reddit.com/r/ADHD/comments/ls2ajg), the writer valued a combined list and ingredient amounts embedded within steps; another [ADHD food-waste post](https://www.reddit.com/r/ADHD/comments/zdfuwr) valued realistic planning that reduced overbuying. These are product testimonials, not independent efficacy studies.

## Recipe instruction design: accessibility is not just bigger text

Recipe pages often force split attention: read a step, scroll back to find the quantity, return to the step, remember a prior state, then look for the next timer. This taxes ordinary working memory and becomes more consequential under distraction, time pressure, or fatigue. HCI research on interactive recipes found cooks judged instructions with ingredient information integrated into steps clearer and easier to read, because it reduced looking up and mentally integrating separated information. It recommends support for non-linear navigation, parallel steps, and a procedure overview with sub-goals ([thesis and cooking study](https://etheses.whiterose.ac.uk/id/eprint/5158/)). A separate cooking-interaction study found cognitive overload and uncertainty salient and called for hands-free, non-linear, minimally interruptive instruction support ([TU Delft repository](https://repository.tudelft.nl/record/uuid%3Afb67b746-20e8-43b8-96c1-c536e3ab354b)).

Design requirements derived from that evidence and the community reports:

* **One actionable step at a time, plus a map.** Show the current step in large, plain language, but provide a persistent overview of phases (“prep / cook / finish / store”) so the user is not trapped in a tunnel.
* **Ingredients in context.** Re-state the exact quantity/unit at the step where it is used, visually mark it used, and allow the same ingredient to appear at multiple steps without ambiguity. Preserve the full ingredients checklist for mise en place users.
* **Explicit verbs and success cues.** Replace “cook until done” with observable cues, safe temperatures where relevant, texture options, and approximate ranges. “Sauté until softened, 5–7 minutes; for crisp-tender, stop earlier” supports different preferences better than falsely precise one-path instruction.
* **Parallelism made safe.** Show what can happen while something cooks, versus what requires attention now. Offer a “focus mode” that hides optional parallel tasks. A novice may prefer sequential steps; an experienced cook may want the optimized view.
* **Memory and recovery.** Checkboxes, an undoable step history, named timers, a “where am I?” summary, and a pause/resume state are more valuable than decorative progress rings. A return after interruption should say what is currently on heat and what is next.
* **Modality and physical access.** Support adjustable text, contrast, reduced motion, text-to-speech, voice or touch-free advancement where safe, printable/low-ink views, and a screen that stays on. Do not make video the only route; captions and text are necessary, and some users prefer no autoplay or sound.
* **Actual complexity metadata.** Store active time, elapsed time, waiting periods, number of vessels/appliances, knife skills, cleanup burden, attentional demand, and sensory intensity separately. “30 min, easy” obscures the factors that determine whether a recipe is possible tonight.

This is an accommodation baseline, not an autism-specific visual style. It benefits a distracted, tired, new, disabled, busy, or expert cook in different ways.

## Grocery, inventory, leftovers, and food waste

Food waste is a real financial and emotional pain point when intentions, perishability, and capacity drift apart. It should not be moralized. Public-health guidance recommends planning leftovers, building a list as items run out, mixing fresh/frozen/shelf-stable food, and using fresh food first ([USDA MyPlate](https://www.myplate.gov/eathealthy/budget/budget-weekly-meals)). The FDA notes that misunderstanding date labels contributes to consumer waste and points people to storage guidance ([FDA guidance](https://www.fda.gov/food/consumers/how-cut-food-waste-and-maintain-food-safety)). Safety needs an accurate boundary: USDA FSIS says refrigerate perishable leftovers within two hours, store refrigerator leftovers for 3–4 days, and use safe reheating practices ([FSIS leftovers guidance](https://www.fsis.usda.gov/food-safety/safe-food-handling-and-preparation/food-safety-basics/leftovers-and-food-safety)).

The product opportunity is a low-friction inventory that creates **useful prompts**, not a perfect database that users must maintain. At minimum:

* Let a planned recipe create an expected leftover and a simple “made / skipped / froze / ate / discarded” update. “Skipped” must be easy and guilt-free, because it prevents phantom inventory.
* Translate a purchase into units users see: “1 bag spinach,” “half onion,” “three portions rice,” not merely abstract ingredients. Link each to meals that use it and to a safe storage window, while clearly labelling safety information and not overriding package instructions.
* Provide a “use soon / easiest first” view that considers energy level and trusted foods. A bag of greens is not useful if every suggestion is a 50-minute recipe.
* Preserve ingredient provenance when consolidating a shopping list: users need to see which recipe requires the item, avoid buying something they already have, and decide what to drop if capacity changes.
* Support delivery/pickup, shares, and a household handoff, while respecting consent. A shared list should not become a surveillance device or an obligation dashboard.

## Current app comparison

The table reflects current public documentation, reviewed 19 August 2026. It does not rate overall quality and it should not be read as an accessibility conformance audit.

| App | Documented strengths | Relevant gaps in public feature descriptions / caution | Sources |
| --- | --- | --- | --- |
| **Paprika** | Imports web recipes; local/offline collection; categories/search; reusable menus and weekly/monthly planner; scaled ingredients; smart grocery lists; pantry quantities/expiry dates; cross-off ingredients and highlight current direction; automatic timers; pin active recipes. | Excellent personal recipe management and in-cooking placekeeping. Public pages emphasize conventional categories, meal calendars, pantry fields, and recipe notes—not a structured sensory profile, capacity/energy ladder, automatic rescue substitutions, or native community knowledge. Import quality depends on source formatting. | [Overview](https://www.paprikaapp.com/); [Windows guide](https://www.paprikaapp.com/help/windows/) |
| **AnyList** | Shared and categorized lists; voice item entry; recipe import and collections; recipe cooking view with ingredient/step marking and toggling; scaling; calendar meal plan; grocery generation; household/calendar sharing; item photos. | Strong list and household coordination. Its public material documents notes, collections, calendar planning, and photos, but not sensory attributes, adaptive effort modes, safety-aware leftover tracking, or community discovery. Meal planning and many recipe features require AnyList Complete. | [Feature overview](https://www.anylist.com/); [getting started](https://help.anylist.com/articles/getting-started/); [feature comparison](https://www.anylist.com/features) |
| **Mealime** | Curated recipes; 200+ preference options, diets/allergies/disliked ingredients and custom filters; self-serve or auto-built plans; a documented just-in-time planning mode; grocery list consolidation by department and recipe; ingredient details/substitutes; grocery-delivery integrations; plan optimisation to reduce waste; cooking mode and recipe notes. | Most explicitly addresses decision fatigue, common dislikes, and food waste. But diet/allergen/dislike filters are not a substitute for texture/smell/temperature mapping; official material does not document sensory notes, a user-owned “safe food” system, no-cook rescue modes, energy-sensitive plan switching, or a broad community memory layer. Curated recipes may limit fit for people whose trusted foods are highly specific. | [Getting-started guide](https://support.mealime.com/article/151-getting-started-guide); [site](https://www.mealime.com/); [cooking docs](https://support.mealime.com/category/83-recipes-cooking) |
| **Samsung Food** | Saves web recipes; collections and search; dietary preferences/avoidances; weekly plans, drag/drop, notes and recurring meals; shopping list; nutrition; sharing; recipe communities with questions, advice, ratings and reviews; cross-device access. | The richest documented social layer and broad recipe discovery. Communities currently advertise diet/restriction/needs-oriented discovery, but public pages do not describe structured sensory tolerance, a standardized “what it was actually like” recipe record, energy-aware fallbacks, food-safety-aware leftovers, or moderation designed for disability-informed advice. More discovery can also increase choice load unless the user can tightly constrain it. | [Product page](https://samsungfood.com/); [recipe sharing](https://samsungfood.com/recipe-sharing-app/); [meal planner/FAQ](https://samsungfood.com/meal-planner/) |

### Cross-app reading

All four cover the conventional pipeline in some form: collect or choose recipes → plan → consolidate ingredients → shop → cook. Paprika and AnyList are especially useful where the user already has trusted recipes; Mealime offers the strongest documented plan-generation and waste-optimisation mechanics; Samsung Food has the strongest documented community/discovery surface. These are meaningful wins and first-person ADHD posts specifically describe the value of Mealime’s embedded amounts and consolidated grocery list.

Yet their public product models are mostly **recipe-centric**, not **capability-centric**. They ask “What would you like to make?” and “What are your dietary restrictions?” They rarely ask, in a structured and reversible way: “What feels possible now?”, “Which version of this food is tolerable?”, “What changed after buying it?”, “Will this reheat acceptably?”, “What supplies are available?”, or “What can another household member pick up from here?” The gap is not merely a missing filter; it is a missing state model.

## Features people repeatedly ask for—and why current recipe apps handle them poorly

This section distinguishes a **repeated design signal** from an unproven market-size claim. The request signal comes from recurring first-person accounts and from the mismatch visible in mainstream public feature sets.

### 1. Energy-aware plans with graceful failure paths

People repeatedly describe a planned meal becoming impossible when energy or executive capacity falls. Current tools let users drag, delete, or replace a calendar entry, but that asks the user to do new planning at the moment of least capacity. Build a per-recipe ladder: original recipe; shortcut version; heat/assemble version; emergency trusted option. At cooking time, a single control should switch routes, adjust the grocery/leftover forecast, and carry forward unopened perishable ingredients. Include **“skip without explanation”**.

### 2. Sensory metadata that is granular, private, and user-authored

Allergen/diet filters are valuable but do not encode whether an ingredient is acceptable raw, cooked, blended, crisp, hot, touching another item, or after reheating. Add optional structured tags for texture, smell, flavor intensity, appearance, temperature, mixed/separate components, noise/mess, and predictable brand/product. Let a user create their own terms and mark “unknown,” “depends,” and “currently no.” Never use a preference to make a health judgment or hide food without transparent control.

### 3. “Safe food” / trusted-recipe memory that learns from lived outcomes

Favorites are too shallow. After making a recipe, the app should ask only a few optional, nonintrusive questions: Did it work? Would you make it again? Was the texture right? How much energy did it really take? How were the leftovers? What would you change next time? Store an editable personal record and surface it at decision time. Distinguish “liked the flavor,” “could execute alone,” “works at low energy,” “works for a particular household member,” and “not safe after day one.” This is recipe memory, not a rating average.

### 4. Instruction transforms, not just cooking mode

Major apps provide some current-step highlighting, timers, and note fields. The missing capability is a transformable recipe: sequential or parallel view; one-step cards; an integrated quantity view; “prep all first” versus “measure as you go”; hands-free/print modes; photo or video at a precise step; and recovery after interruption. A tool may use AI to draft these forms, but it must show the original, allow corrections, flag uncertain parses, and never invent food-safety information. Human-authored validation is important for substitutions and temperatures.

### 5. Time that reflects reality

Record personal *actual* active time, elapsed time, cleanup, cooldown, and difficulty. At selection, filter by “time until I need to eat,” “can leave unattended,” “one appliance,” “no knife,” “no dishes,” “no strong smell,” or “can stop halfway.” Use visual clocks and named timers. A recipe’s publisher estimate can remain available, but should not outrank the user’s own history.

### 6. Pantry/leftover support designed for imperfect memory

Traditional pantry trackers often fail because they require perfect data entry. Replace exhaustive inventory with useful objects: photo/receipt import optionally; quick “I have this”; “opened on [date]”; planned portions; a fridge/freezer visual; and the ability to mark it uncertain. Surface a few trusted, low-effort use-up options. An expiration reminder must be adjustable/off by default, with storage safety information from authoritative sources and no claim that an app can determine edibility.

### 7. Community that shares adaptations, not only recipes

Recipe communities can reduce isolation and help people locate foods that match needs, but unstructured social feeds produce choice overload and unreliable advice. Let contributors add standardized, optional experience fields: sensory profile, brands used, substitutions actually tested, number of pans, sound/smell/mess, active versus elapsed time, leftover/reheating result, low-energy shortcut, and access needs. Make “works for me” the default phrasing. Separate medical/allergy claims from ordinary preference advice; require evidence or qualified review for safety claims; provide reporting and moderation. Let users share a private household collection without joining a public community.

### 8. Autonomy-preserving prompts and collaboration

Offer choices, deferral, and handoff: “Would you like to pick, prep, order, or ask someone?” A shared household plan should assign a step only with consent, make dependencies visible (“if you buy this, I can cook it”), and avoid coercive task streaks. For some users the meal plan is a personal aid; for others it is household coordination. These are distinct modes and should not be forced together.

## Product principles and research recommendations

1. **Co-design with a heterogeneous paid panel.** Recruit autistic people, ADHD people, people with both, people without diagnoses who experience executive/sensory barriers, varied ages, cultures, incomes, cooking skills, diets, and household arrangements. Include people who love cooking and people who avoid it. Do not use only caregivers as proxies for adults.
2. **Test states, not only personas.** Prototype when participants are rested and when they are time-pressured, interrupted, or completing a low-energy simulation ethically. Measure completion, mistakes, time-to-first-action, perceived demand, and recovery after interruption—not just preference ratings.
3. **Treat configuration as an ongoing conversation.** Initial onboarding should be short. Let users add sensory tags and energy routes while using the product. A dense diagnostic questionnaire is itself an executive burden.
4. **Protect privacy.** Food, diagnosis, medication timing, eating patterns, and household roles are sensitive. Make diagnosis disclosure unnecessary; keep sensory profiles private by default; explain sharing and recommendation data; support export and deletion.
5. **Avoid ableist success metrics.** Fewer takeout meals, more novelty, more home cooking, a streak, or dietary variety can be positive goals for some people but are not universal measures of success. User-selected outcomes may include eating something, avoiding spoilage, spending less, reducing conflict, finding pleasure, or preserving energy.
6. **Set clinical boundaries.** Provide links to professional support where eating restrictions risk malnutrition, dehydration, food safety issues, or an eating disorder. Do not diagnose ARFID, prescribe diets for autism/ADHD, or make nutrition/medical claims based on app behavior.

## Prioritized concept: an adaptive meal cockpit

A promising minimum product is a **personal meal cockpit**, not another giant recipe catalog.

1. **Today screen:** one optional body/capacity check; three trusted choices ranked by time-to-bite, effort, sensory fit, ingredients on hand, and perishability. Include “I cannot cook,” “choose for me,” and “not now.”
2. **Recipe memory:** a personal, editable record of actual effort, sensory notes, substitutions, portions, leftovers, and confidence. It becomes more valuable than generic star ratings.
3. **Adaptive cook mode:** transform a trusted recipe into selected complexity: full, shortcut, or heat/assemble. Present integrated quantities, current state, named timers, recovery cues, and a clear finish/store step.
4. **Low-maintenance food state:** planned purchases and leftovers with quick corrections, a “use soon” view, and safe-storage references. Do not require barcode-level inventory.
5. **Optional sharing:** household handoffs first; public adaptation community later, with moderation and structured, non-medical claims.

Validate the concept against existing apps rather than rebuilding their mature functions. A prototype should test whether it lowers time-to-first-action and reduces “plan collapse” on variable-capacity days, without increasing configuration effort or guilt. Comparison users should be allowed to keep Paprika, AnyList, Mealime, or Samsung Food as their source of recipes; import/export and deep links are part of accessibility because established personal recipe collections are valuable memory supports.

## Limitations

Research on autistic eating is disproportionately focused on children, and interoception measures and findings are inconsistent. Food selectivity may have many interacting causes; sensory preference is neither a universal autistic trait nor automatically pathology. ADHD/time research identifies group-level differences, not a feature checklist. PDA terminology remains contested and should not be operationalized as a clinical fact. Community posts are indispensable for discovering lived friction but cannot establish frequency, causality, effectiveness, or diagnosis. Vendor pages document intended features, not accessibility outcomes, pricing durability, data practices, or every feature behind a login.

Accordingly, the strongest claim this report makes is practical and bounded: existing evidence and recurring first-person reports justify testing configurable supports for memory, timing, sensory fit, autonomy, and variable capacity. They do **not** justify designing for a caricatured “neurodivergent user,” forcing disclosure, or treating repeated meals and shortcuts as failures.

## Source list

### Primary/reputable research and guidance

* [Metcalfe, McFeaters & Voyer (2024), ADHD time-perception systematic review/meta-analysis](https://pubmed.ncbi.nlm.nih.gov/38145491/)
* [Interoception in autism: systematic review and meta-analysis](https://pmc.ncbi.nlm.nih.gov/articles/PMC12406136/)
* [Interoception in ADHD: systematic review](https://pmc.ncbi.nlm.nih.gov/articles/PMC11842156/)
* [First-hand accounts of interoceptive difficulties in autistic adults](https://pubmed.ncbi.nlm.nih.gov/33389300/)
* [Sensory processing and eating behaviours in autism: systematic review](https://pmc.ncbi.nlm.nih.gov/articles/PMC9545673/)
* [Food selectivity and autism: systematic review](https://pmc.ncbi.nlm.nih.gov/articles/PMC12304907)
* [UK National Autistic Society: demand avoidance evidence guidance](https://www.autism.org.uk/advice-and-guidance/behaviour/demand-avoidance)
* [PDA methods scoping review](https://www.frontiersin.org/journals/education/articles/10.3389/feduc.2024.1230011/full)
* [Interactive recipe instruction research](https://etheses.whiterose.ac.uk/id/eprint/5158/)
* [USDA MyPlate meal-planning/waste guidance](https://www.myplate.gov/eathealthy/budget/budget-weekly-meals)
* [USDA FSIS leftovers and food safety](https://www.fsis.usda.gov/food-safety/safe-food-handling-and-preparation/food-safety-basics/leftovers-and-food-safety)
* [FDA food-waste and date-label guidance](https://www.fda.gov/food/consumers/how-cut-food-waste-and-maintain-food-safety)

### First-person community evidence (explicitly anecdotal)

* [Meal planning and food-related dysfunction, r/AutisticWithADHD](https://www.reddit.com/r/AutisticWithADHD/comments/1fps6p6)
* [Cooking/executive dysfunction and food preferences, r/AutismInWomen](https://www.reddit.com/r/AutismInWomen/comments/1n32yep)
* [Autistic adult food routines discussion, r/AutisticAdults](https://www.reddit.com/r/AutisticAdults/comments/1po1nno)
* [Recipe-reading tool discussion, r/neurodiversity](https://www.reddit.com/r/neurodiversity/comments/1rud5ue)
* [Mealime and ADHD discussion, r/ADHD](https://www.reddit.com/r/ADHD/comments/ls2ajg)

### Official app documentation

* [Paprika](https://www.paprikaapp.com/) and [user guide](https://www.paprikaapp.com/help/windows/)
* [AnyList](https://www.anylist.com/) and [feature comparison](https://www.anylist.com/features)
* [Mealime getting-started guide](https://support.mealime.com/article/151-getting-started-guide)
* [Samsung Food](https://samsungfood.com/), [community features](https://samsungfood.com/recipe-sharing-app/), and [meal-planning features](https://samsungfood.com/meal-planner/)

# Recipe apps through a neurodivergent lens

Research pass: 2026-08-19. This is product research, not a clinical claim set. Established executive-function concepts are kept separate from first-person reports and product hypotheses.

## Research integrity
A planned Claude/Codex research team did not complete: Claude CLI was logged out and Codex CLI was unavailable. The fallback pass used local SearXNG across official app listings, reputable ADHD resources, accessible-cooking products, current comparison pages, and first-person community discussions. Competitor marketing claims still require hands-on testing during discovery.

## What the category already does well

### Recipe capture and organization
Paprika, Samsung Food, Recipe Keeper, Pestle, Crouton, Mela, ReciMe, and newer recipe organizers commonly offer some mixture of web recipe import, categorization, meal planning, grocery lists, scaling, timers, and cloud sync. Modern competitors increasingly market social-video import.

### Recipe notes and community discovery
Samsung Food exposes personal and community notes. Cooked markets personal substitutions, cooking notes, advice, and sharing. Community recipe portals and public reviews are established patterns, so Body Kitchen needs a sharper interaction model than simply adding comments.

### Ingredient-led discovery
SuperCook and similar products recommend recipes from selected ingredients. Pantry products pair inventory with suggestions. This can help, but it usually begins with cataloging ingredients and assumes inventory stays current.

### Accessible instruction precedent
Look, Cook, and Eat and Accessible Chef demonstrate demand for visual, achievable, clearly sequenced cooking instructions. Their existence supports step clarity and visual scaffolding, though they serve broader accessibility needs and should not be treated as ADHD/autism efficacy studies.

## Repeated neurodivergent pain patterns

### More than recipe discovery
People already possess recipes. The breakdown often happens between wanting a meal and completing the chain: deciding, checking ingredients, shopping, initiating, sequencing, timing, handling cleanup, and remembering the outcome.

ADDA describes executive dysfunction as difficulty across planning, focus, organization, time management, and emotional regulation. First-person cooking discussions repeatedly mention multi-step cooking feeling disproportionately effortful, meal planning as high effort, and unclear recipe instructions as a barrier.

### Working-memory tax
Traditional recipes require repeated scrolling and holding several state variables: what step is next, what is already chopped, which burner is active, and how long something has cooked. A checked step list alone does not solve parallel timing.

### Time language is unreliable
“Prep: 10 minutes” often excludes gathering, thawing, washing, interruption, cleanup, or novice pace. Users need active time, waiting time, number of transitions, and cleanup burden.

### Energy changes daily
A recipe classified only by cuisine or total time ignores task initiation. “Open and eat,” “assemble,” “microwave,” “one pan,” and “full cook” are more actionable than easy/medium/hard.

### Decision paralysis
Large recommendation feeds can increase load. A small candidate set or a random draw helps only when the pool already respects hard constraints and current capacity.

### Sensory requirements are personal
Texture, smell, temperature, mixture, predictability, and brand-specific preferences vary by person. Generic “autism-friendly” recipe labels are reductive. The system should learn opt-in individual preferences from ratings and notes.

### Inventory upkeep becomes another abandoned chore
A complete pantry ledger demands continuous correction. Inventory should grow from receipts, cooking events, saved recipes, and quick confirmations. Full cataloging remains optional.

## Product gaps worth testing

### 1. Desire-first onboarding
Start with recipes, cravings, and social saves. Ask what sounds good before asking what is in the refrigerator.

### 2. Recipe memory, not favorites
After cooking, save:
- liked / okay / not for me
- personal notes
- substitutions used
- texture and sensory reactions
- actual time and effort
- cleanup burden
- who else liked it
- “more like this” and “less like this”

A recipe that was randomly revealed must enter the same durable memory.

### 3. Adjustable information density
Default view shows title, effort, time, and one next action. Users can enable notes, substitutions, nutrition, technique detail, household feedback, community tips, and advanced inventory. Preferences persist per person and can change by context.

### 4. Effort adaptation
Transform one recipe into modes rather than recommending a different identity of meal:
- original
- fewer transitions
- fewer dishes
- premade shortcuts
- microwave / air fryer / one-pan
- sensory-safe separation
- batch version

The system must label what changed and preserve the original creator/source.

### 5. Honest time model
Show active work, passive waiting, transitions, equipment, cleanup, and interruption tolerance. Let users record their actual time without framing it as failure.

### 6. Cook mode that externalizes state
One active instruction, visible upcoming step, parallel timers, ingredient quantities repeated at point of use, “I got interrupted,” and safe resume. Offer concise and detailed instruction modes.

### 7. Constrained delight
Dinner Draw chooses only from recipes that satisfy current effort, time, sensory, dietary, equipment, and rejection history. The animation provides novelty without gambling mechanics, streak pressure, scarcity, or paid randomness.

### 8. Community as practical annotation
Community value should center on useful adaptations:
- “I made this with…”
- actual effort and cleanup
- sensory notes
- substitutions that worked
- clearer step photos
- beginner warnings
- household reactions

Sort by relevance to the user rather than raw popularity. Allow the entire community layer to be hidden. Moderation and creator attribution are launch requirements, not later polish.

### 9. Progressive inventory
Ask only when a recipe creates a reason: “Do you already have rice?” A quick fridge photo can improve substitutions, while a complete Deep Scan remains optional.

### 10. Gentle recovery
Saved drafts survive interruption. Missed plans roll forward without red badges, streak resets, or accumulated overdue tasks. “Choose something easier” is a successful outcome.

## Complexity model

### Calm default
Recipe saves, effort filters, Dinner Draw, simple recipe memory, shopping list.

### Optional modules
Community, nutrition, substitutions, inventory, detailed cooking guidance, household collaboration, food-waste insights, advanced planning, and deeper personalization.

### Context modes
- **Low capacity:** one suggestion, minimal steps, no community feed
- **Normal:** saved recipes, notes, substitutions
- **Detail mode:** full timeline, nutrition, inventory, community adaptations

A mode is a reversible view preference, never a judgment about the user.

## Sources and discovery leads
- ADDA, executive function overview: https://add.org/executive-function-disorder/
- Look, Cook, and Eat accessible recipes: https://www.lookcookandeat.com/
- Accessible Chef visual recipes: https://www.instagram.com/accessiblechef/
- Autistic Adults discussion on recipe specificity: https://www.reddit.com/r/AutisticAdults/comments/1n42xml/i_really_need_detailed_clear_instructions_in/
- ADHD discussion on low-friction meal ideas: https://www.reddit.com/r/ADHD/comments/103lke7/adhd_friendly_meal_ideas/
- Samsung Food App Store listing and notes/community claims: https://apps.apple.com/us/app/samsung-food-meal-planner/id1133637674
- Cooked App Store listing: https://apps.apple.com/us/app/cooked-your-recipe-book/id6737872247
- Tandoor open-source recipe system: https://github.com/TandoorRecipes/recipes
- Current competitor comparison lead: https://foodiejournal.app/best/best-recipe-apps-2026
- Paprika/Mela/Crouton comparison lead: https://swoodie.app/blog/paprika-vs-mela-vs-crouton-vs-swoodie-2026

## Next validation work
1. Hands-on teardown of the top ten apps using one identical TikTok recipe, one messy blog recipe, one substitution, and one interrupted cook session.
2. Interview adults who abandoned meal-planning or pantry apps; recruit across ADHD, autism, disability, caregiving, and non-diagnosed executive-function strain without treating any group as uniform.
3. Prototype-test Calm, Normal, and Detail modes.
4. Test whether recipe-first onboarding reaches a first useful moment faster than fridge scanning.
5. Measure review actions, recipe saves that become cooks, repeat cooks, and post-cook feedback completion.

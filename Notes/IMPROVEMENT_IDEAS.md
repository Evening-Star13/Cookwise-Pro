# Cookwise Pro — Improvement Ideas

## UX & Design

- **Animated page transitions** — smooth fade/slide when navigating between recipe list, recipe details, and modals
- **Skeleton loading states** — show placeholder shimmer cards while recipes load instead of a spinner
- **Drag-and-drop meal planning** — let users drag recipe cards directly onto calendar days
- **Recipe card image lazy loading** — only load images as they scroll into view for faster initial paint
- **Responsive image gallery** — masonry/Pinterest-style layout for the photo gallery modal

## Features

- **Recipe scaling** — a slider or input to scale ingredient quantities (e.g., 2x, 0.5x servings)
- **Cooking mode / step-by-step view** — a full-screen distraction-free mode that shows one instruction step at a time with large text
- **Grocery aisle grouping** — auto-sort the shopping list by grocery store section (produce, dairy, pantry, etc.)
- **Meal plan nutritional summary** — show daily/weekly calorie and macro totals for the planned meals
- **Recipe import from URL** — paste a link from a recipe website and auto-parse the title, ingredients, and steps
- **Voice command support** — hands-free "next step" / "start timer" while cooking
- **Seasonal recipe suggestions** — recommend recipes based on what's in season for the user's region
- **Cost estimation** — approximate cost per serving based on average ingredient prices

## Data & Organization

- **Nested collections / folders** — allow sub-collections (e.g., "Weeknight Dinners > Under 30 Min")
- **Custom tags with color coding** — let users assign colors to tags for visual categorization
- **Recipe versioning** — track edits to a recipe over time and allow reverting to a previous version
- **Duplicate detection** — warn when adding a recipe that closely matches an existing one

## Social & Sharing

- **Export to PDF** — generate a printable, nicely formatted recipe card
- **Share collections** — export/import entire collections as a shareable link or file
- **Family/household accounts** — shared recipe library with multiple users

## Technical / Performance

- **Offline PWA support** — service worker for full offline access and "Add to Home Screen"
- **Split code into components** — break the single large HTML file into separate modules for maintainability
- **IndexedDB for images** — store recipe photos locally in IndexedDB instead of base64 in localStorage to avoid storage limits
- **Search indexing** — full-text search across ingredients, notes, and instructions (not just recipe names)
- **Keyboard navigation** — full keyboard accessibility for all modals and card interactions beyond the existing shortcuts

## New Suggestions

### Features

- **Smart recipe suggestions** — recommend recipes based on pantry items you have, dietary restrictions, or cuisine preferences
- **Cooking timers with notifications** — multiple simultaneous timers for recipe steps with alerts
- **Ingredient substitution suggestions** — when viewing a recipe, suggest alternatives for each ingredient
- **Recipe difficulty ratings** — let users mark if a recipe was "Easy / Medium / Hard" after cooking it, useful for filtering
- **Allergen highlighting** — auto-detect and highlight common allergens (nuts, dairy, gluten, etc.) prominently
- **Equipment tagging** — mark what tools/equipment recipes need (blender, mixer, slow cooker) to filter by what you have
- **Batch recipe editing** — apply tags, collections, or notes to multiple recipes at once
- **Recipe analytics** — track most-cooked recipes, favorite cuisines, cooking frequency over time

### Organization

- **Weekly meal plan templates** — save a full week's plan and reuse/duplicate it with one click
- **Recipe bookmarks/favorites** — quick access to recipes you cook frequently
- **Quick recipe access** — "Recent recipes" tab for the ones you viewed/cooked last
- **Recipe comparison** — side-by-side view of similar recipes to pick the best version

### UX

- **Ingredient notes** — add custom notes to ingredients ("use organic," "substitute with X," "buy this brand")
- **Yield/servings persistence** — remember your last used serving size when re-opening a recipe
- **Prep vs cook time breakdown** — separate display of active cooking time vs passive/prep time
- **Unit converter inline** — quick metric/imperial conversion without leaving the recipe

# Design System: Modern African Indulgence

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Embers of Elegance."** 

This is not a standard restaurant interface; it is a digital translation of the hearth. We are moving away from the "template" look of centered grids and white backgrounds. Instead, we embrace **Organic Brutalism**—a style that combines high-contrast, high-impact typography with raw, earthy textures. 

The layout should feel like a premium editorial magazine. We break the grid through intentional asymmetry: images should overlap container boundaries, and typography should bleed across section transitions. This creates a sense of "raw energy" and "soulful" movement, mirroring the unpredictable dance of smoke and fire.

---

## 2. Colors
Our palette is rooted in the "Modern African Indulgence" theme, utilizing deep charcoals to represent ash and rich forest greens to represent life and fresh ingredients.

### The Palette
- **Primary (`#ffb68b`):** The "Glowing Ember." Use this for high-priority calls to action.
- **Primary Container (`#e67f39`):** The "Burnt Orange." Use for major interactive surfaces.
- **Secondary (`#a3d2a4`) & Tertiary (`#aecfae`):** The "Forest Canopy." These greens provide a cooling counterpoint to the heat of the oranges.
- **Surface (`#131313`):** The "Deep Charcoal." Our canvas.

### Design Rules
- **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Define boundaries through background color shifts. For example, a `surface-container-low` section sitting directly on a `surface` background provides all the separation needed.
- **Surface Hierarchy & Nesting:** Treat the UI as physical layers of stone and wood. Use the `surface-container` tiers (Lowest to Highest) to create depth. An inner card should use a higher tier (brighter) than its parent container to feel "lifted."
- **The "Glass & Gradient" Rule:** Use Glassmorphism (semi-transparent `surface` colors + `backdrop-blur`) for navigation bars and floating overlays. 
- **Signature Textures:** Apply subtle linear gradients transitioning from `primary` to `primary-container` on buttons and Hero headers to give them a "flickering fire" soul.

---

## 3. Typography
We use a high-contrast pairing to balance futuristic tech with organic warmth.

- **Display & Headline (Space Grotesk):** This is our "Futuristic" voice. It is clean, wide, and rhythmic. Headlines should be used at large scales (`display-lg`: 3.5rem) with tight letter spacing to feel "High-End."
- **Title & Body (Plus Jakarta Sans):** Our "Modern" voice. It provides exceptional readability for menu descriptions. 
- **The Editorial Mix:** For quotes or signature items, occasionally lean into a serif (like Georgia) to reference the brand’s heritage, but keep it sparse to maintain the sleek, futuristic feel.

---

## 4. Elevation & Depth
In this system, depth is a matter of light, not lines.

- **The Layering Principle:** Stack `surface-container` tiers. A `surface-container-lowest` card placed on a `surface-container-low` background creates a natural, recessed "carved" look.
- **Ambient Shadows:** Shadows must be felt, not seen. Use a blur of 32px–64px with an opacity of 4%–8%. The shadow color should be a tinted version of the `on-surface` color (a warm grey) rather than pure black.
- **The "Ghost Border" Fallback:** If containment is required for accessibility, use the `outline-variant` token at **15% opacity**. Never use 100% opaque borders.
- **Glassmorphism:** For interactive overlays, use `surface-variant` at 60% opacity with a `20px` backdrop blur. This allows the "glow" of the background content to bleed through, creating an "exclusive" atmosphere.

---

## 5. Components

### Buttons
- **Primary:** Gradient fill (`primary` to `primary-container`), no border, `md` (0.375rem) roundedness.
- **Secondary:** `surface-container-high` background with `primary` text.
- **Interaction:** On hover, increase the "glow" by adding a soft `primary` ambient shadow.

### Cards & Lists
- **Rule:** Forbid divider lines. Use `spacing-8` (2rem) of vertical white space or a subtle shift from `surface` to `surface-container-low` to separate items.
- **Visuals:** Images in cards should use `xl` (0.75rem) roundedness and, where possible, break the card's container (negative margin) to create a premium, custom feel.

### Chips
- **Selection:** Use `secondary-container` with `on-secondary-container` text.
- **Style:** Pills (rounded-full) only. These represent "pebbles" or organic elements.

### Input Fields
- **Background:** `surface-container-highest`.
- **Active State:** Change only the bottom border to `primary` (2px). Keep the rest of the field borderless to maintain a sleek, minimal look.

### Signature Component: The "Smoked Overlay"
- A full-screen menu overlay using a `surface` background at 90% opacity with a heavy grain texture and `display-lg` typography, creating an immersive, soulful transition.

---

## 6. Do's and Don'ts

### Do
- **Do** use asymmetrical layouts where text sits 1/3rd into an image.
- **Do** use the Spacing Scale (especially `20` and `24`) to create massive "breathing room."
- **Do** apply `surface-bright` for highlights on small interactive elements like toggles.

### Don't
- **Don't** use pure black (`#000000`) or pure white (`#FFFFFF`). Use our `surface` and `on-surface` tokens.
- **Don't** use "Drop Shadows" that look like dark smudges. Keep them ambient and tinted.
- **Don't** use a standard 12-column centered grid for everything. Experiment with offsets to keep the "Modern African Indulgence" feel alive.
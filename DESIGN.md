# Design System: Maison Demeusy Editorial Language

## 1. Overview & Creative North Star: "The Artisanal Archive"

The Creative North Star for this design system is **"The Artisanal Archive."** 

This system moves beyond the transactional nature of a standard bakery website to create a digital experience that feels like a curated editorial piece—part high-end culinary magazine, part heritage family ledger. We reject the "boxed-in" layout of traditional web design. Instead, we embrace **intentional asymmetry**, high-contrast typographic scales, and layered depth. 

The experience must feel like a French boulangerie at dawn: tactile, warm, and deeply intentional. By using wide margins, overlapping image treatments, and a complete absence of rigid structural lines, we create an atmosphere of premium craftsmanship where the product (the bread) is the hero of a larger story.

---

## 2. Colors: Tonal Breadth & Warmth

Our palette is rooted in the "Golden Hour" of baking. It transitions from the deep, charred grays of a wood-fired oven to the creamy interior of a fresh crumb and the vibrant orange of a perfectly baked crust.

### The "No-Line" Rule
**Structural borders are strictly prohibited.** To separate sections, designers must use background color shifts. A section using `surface-container-low` should sit directly against a `surface` background. The eye should perceive the change in "atmosphere" rather than a hard boundary.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of fine paper. 
- **Base Layer:** `surface` (#fcf9f8).
- **Secondary Narrative:** `surface-container-low` (#f6f3f2).
- **Featured Content/Cards:** `surface-container-lowest` (#ffffff) to provide a subtle "pop" of clean white against the creamier base.
- **Deep Immersion:** `surface-dim` (#dcd9d9) for footers or high-contrast sidebars.

### The Glass & Gradient Rule
For floating navigational elements or premium product overlays, utilize **Glassmorphism**:
- `surface` color at 70% opacity with a `24px` backdrop-blur. 
- **Signature Glow:** For primary CTAs, use a linear gradient transitioning from `primary` (#954a00) to `primary-container` (#ff8200) at a 45-degree angle. This adds a "honeyed" sheen that flat color cannot replicate.

---

## 3. Typography: The Editorial Contrast

The typographic soul of this system lies in the tension between the classic, high-contrast serif and the utilitarian, modern sans-serif.

- **Display & Headlines (Noto Serif):** Used for storytelling. These should be set with generous tracking (letter-spacing) for a luxurious, airy feel. This is the "voice" of tradition.
- **Body & Titles (Work Sans):** Used for clarity and modern efficiency. It represents the precision and technique of the baker.
- **Labels (Inter):** Used for technical metadata (e.g., weights, ingredients, timestamps).

**Hierarchy Strategy:**
Always pair a `display-lg` headline with a `body-md` description. The extreme size difference creates a "Poster" effect that feels curated rather than templated.

---

## 4. Elevation & Depth: Tonal Layering

Traditional shadows are often too "digital." In this system, depth is organic.

- **The Layering Principle:** Instead of shadows, stack `surface-container` tiers. A `surface-container-highest` element placed on `surface` creates an immediate sense of tactile importance without visual noise.
- **Ambient Shadows:** When an element must "float" (e.g., a modal or a floating cart), use a shadow with a blur of `40px` and an opacity of `6%`. The shadow color must be `on-surface` (#1c1b1b), giving it a warm, natural feel rather than a cold gray.
- **The "Ghost Border" Fallback:** If a boundary is required for accessibility, use the `outline-variant` (#dec1af) at **15% opacity**. It should be felt, not seen.

---

## 5. Components: Crafted Primitives

### Buttons
- **Primary:** High-gloss gradient (`primary` to `primary-container`). Roundedness: `full`. No border.
- **Secondary:** `surface-container-highest` background with `on-surface` text.
- **Tertiary:** Text only in `primary`, with a `2px` underline that appears only on hover.

### Cards & Lists (The "No Divider" Mandate)
**Dividers are forbidden.** 
- Separate list items using `spacing-8` (2rem) of vertical white space. 
- For cards, use a subtle background shift (e.g., `surface-container-lowest` on a `surface` background) and a `0.75rem` (xl) corner radius.

### Input Fields
- **Style:** Minimalist. No background color. Only a "Ghost Border" bottom-stroke (1px, 20% `outline`). 
- **Focus State:** The bottom-stroke transforms into a 2px `primary` color line with a soft `surface-tint` glow.

### Signature Component: The "Heritage Overlay"
A specific pattern for Maison Demeusy: Large, high-resolution product photography (e.g., a sourdough loaf) with a `display-sm` headline overlapping the edge of the image by 20%. This breaks the grid and creates an editorial, high-fashion layout.

---

## 6. Do’s and Don’ts

### Do:
- **Embrace White Space:** Use `spacing-20` and `spacing-24` between major sections. Let the content breathe.
- **Asymmetric Grids:** Offset images from text columns. If text is left-aligned, place the supporting image slightly to the right and lower than expected.
- **Tonal Transitions:** Use background colors to guide the user's journey through different story chapters.

### Don’t:
- **Don't use 1px Solid Borders:** They create a "cheap" grid feel that contradicts the artisanal brand.
- **Don't use Pure Black Shadows:** They look like software, not sunlight.
- **Don't Crowd the Header:** Keep the navigation sparse. Only the essentials. The logo needs space to command authority.
- **Don't use "Stock" Animations:** Use slow, elegant fades (300ms-500ms) rather than "bouncy" or "snappy" transitions. High-end feels deliberate, not fast.
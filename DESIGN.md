# Design System Strategy: The Digital Atelier

## 1. Overview & Creative North Star
**Creative North Star: "The Ethereal Heirloom"**

This design system rejects the "web-template" aesthetic in favor of a bespoke, editorial experience that mirrors high-end physical stationery. We are not building a dashboard; we are curating an invitation. The system breaks the traditional digital grid through **intentional asymmetry**, utilizing large typographic breathing room and overlapping elements to mimic the way hand-painted elements interact with fine paper. 

By prioritizing a mobile-first approach, we treat the viewport as a single, precious vellum sheet. We replace rigid containers with organic flow, using "hand-painted" textures and soft brush strokes as functional anchors rather than mere decoration.

---

## 2. Colors & Surface Philosophy
The palette is rooted in a soft ivory (`#faf9f6`) to provide a warm, tactile base, accented by the intellectual calm of pastel blues and the prestige of gold.

### The "No-Line" Rule
Standard 1px borders are strictly prohibited for sectioning. Separation of concerns must be achieved through:
- **Tonal Shifts:** Transitioning from `surface` to `surface-container-low`.
- **Negative Space:** Using generous padding to define blocks of information.
- **Organic Masks:** Using soft brush stroke textures to "break" the edge of a container.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, semi-translucent papers.
- **Base Layer:** `surface` (#faf9f6) for the primary "paper" background.
- **Content Blocks:** Use `surface-container-lowest` (#ffffff) for cards or RSVP modules to create a "bleached" focus area.
- **Nested Depth:** Place a `surface-container-high` element within a `surface-container-low` section to guide the eye toward interactive elements without using a single line.

### The "Glass & Gold" Rule
To elevate the mobile experience, use **Glassmorphism** for floating headers or navigation bars:
- **Token:** `surface` at 70% opacity with a `20px` backdrop-blur. 
- **Signature Accents:** Use `secondary` (#735c00) and `secondary-container` (#fed65b) sparingly for gold-leaf effects, specifically for CTA highlights and decorative icons.

---

## 3. Typography
The typography system is a dialogue between the "Hand-Drawn" (Script) and the "Precision-Crafted" (Sans-Serif).

- **Display & Headline (notoSerif):** While the spec uses Noto Serif, in practice, this represents our "Calligraphy" layer. For Georgian scripts (e.g., „ედი & ნინო“), use the `display-lg` scale to create an atmospheric, artistic focal point. Headlines should be set with generous tracking (letter spacing) to feel airy.
- **Title & Body (manrope):** The Manrope sans-serif acts as the "functional" layer. It should be clean and understated, set in `on_surface_variant` (#42474d) to reduce visual vibration against the ivory background.
- **The Contrast Rule:** Never pair two script fonts. Use the `display-lg` script for names/titles and immediately anchor it with `label-md` in all-caps for functional descriptors (e.g., "DATE", "LOCATION").

---

## 4. Elevation & Depth
We eschew traditional "box shadows" in favor of **Tonal Layering** and **Ambient Light**.

- **The Layering Principle:** Depth is achieved by "stacking." A `surface-container-lowest` card sitting on a `surface` background provides all the "lift" required.
- **Ambient Shadows:** For "floating" elements like a bottom-sheet RSVP, use an ultra-diffused shadow:
    - `color: rgba(66, 97, 125, 0.06)` (A tinted shadow using the primary blue).
    - `blur: 40px`, `y-offset: 10px`.
- **The Ghost Border:** If a form field requires a boundary, use the `outline_variant` (#c2c7ce) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons (The Call-to-Action)
- **Primary:** Background `primary` (#42617d), Text `on_primary` (#ffffff). Use a `full` roundedness scale (pill-shaped). 
- **Secondary (Gold Leaf):** Background `secondary_container` (#fed65b), Text `on_secondary_container` (#745c00). This is reserved exclusively for the final "Confirm RSVP" action.
- **Interaction:** On tap, the button should subtly scale (98%) rather than change color harshly.

### Cards & RSVP Modules
- **Rule:** Forbid all divider lines.
- **Construction:** Use a `surface-container-low` background with `xl` (0.75rem) rounded corners. Use vertical white space (32px+) to separate the "Wedding Ceremony" details from the "Reception" details.

### Text Inputs
- **Style:** Minimalist. Only a bottom "Ghost Border" (15% opacity `outline_variant`). 
- **Focus State:** Transition the bottom border to `primary` (#42617d) with a 2px thickness. 

### Signature Component: The "Artistic Overlay"
- Use a `surface_variant` (#e3e2e0) brush-stroke SVG as a mask for image headers. Photos of the couple should never be hard-edged rectangles; they should feel integrated into the "paper" via soft-edged masking or overlapping with `display-sm` calligraphy.

---

## 6. Do's and Don'ts

### Do
- **Do** use `primary_container` (#a7c7e7) for subtle background washes behind text to improve legibility on ivory.
- **Do** lean into asymmetry. It’s okay to have a name left-aligned and the date right-aligned with a large gap between them.
- **Do** use "High-Contrast Scale." A 56px name next to a 12px date creates luxury; 24px next to 16px feels like a generic form.

### Don't
- **Don't** use pure black (#000000). Use `on_surface` (#1a1c1a) for all high-contrast text.
- **Don't** use standard 1px dividers. If you need a break, use a `32px` vertical gap or a subtle `tertiary_container` horizontal brush stroke.
- **Don't** overcrowd the mobile viewport. If a section feels tight, move the content to a secondary "scrolled" layer or a modal. Luxury is defined by the space you *don't* fill.
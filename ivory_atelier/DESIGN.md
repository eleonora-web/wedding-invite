# Design System Strategy: The Painted Atelier

## 1. Overview & Creative North Star
**Creative North Star: "The Digital Heirloom"**

This design system moves away from the rigid, sterile grids of modern SaaS to embrace the tactile, imperfect beauty of high-end stationery. We are not building a simple utility; we are creating a digital "keep-sake" that feels like a hand-painted wedding invitation brought to life. 

The visual strategy relies on **Artistic Asymmetry**. By breaking the "Instagram-reel" verticality with organic brush-stroke overlays and high-contrast typography scales, we evoke a sense of bespoke luxury. Imagine a world where traditional Georgian calligraphy meets a modern, minimal UI—a seamless blend of heritage and contemporary high-fashion editorial.

## 2. Colors: The Tonal Canvas
The palette is rooted in a base of soft ivory and pastel blue, punctuated by "Artistic Pops" of vibrant tertiary tones.

*   **Primary (`#745c00`) & Primary Container (`#f5ce53`):** These represent our "Gold Accents." Use them sparingly for high-impact moments, like CTA buttons or special ornamental glyphs.
*   **Secondary (`#49636f`) & Secondary Container (`#ceeaf8`):** Our "Pastel Blue" foundation. These tones should handle the bulk of our interactive surfaces, providing a calming, romantic air.
*   **Tertiary (`#8d4774`) & Tertiary Container (`#ffa9dc`):** These are the "Brush Stroke" colors. Use these for expressive accents—pinks, purples, and vibrant greens that mimic hand-painted floral elements.
*   **Neutral Canvas (`#fbf9f5`):** Our "Soft Ivory." This is the primary surface color, designed to feel like premium, heavy-weight paper.

### The "No-Line" Rule
**Borders are strictly prohibited for sectioning.** To define space, we rely on tonal shifts. A `surface-container-low` card sitting on a `surface` background creates a natural boundary. If you feel the urge to draw a line, instead use a background color shift or a change in the Spacing Scale.

### Glass & Gradient Rule
To achieve the "Instagram-reel" premium feel, use **Glassmorphism** for floating overlays (e.g., bottom navigation bars or RSVP drawers). Apply `surface` or `surface-container` colors at 80% opacity with a `20px` backdrop blur. 
*   **Signature Polish:** Use subtle linear gradients for main CTAs, transitioning from `primary` to `primary-container` at a 45-degree angle to mimic the sheen of gold foil.

## 3. Typography: The Calligraphic Soul
The hierarchy is a tension between the ornate and the invisible.

*   **The Hero (Display & Headline):** Utilizing **Noto Serif** (as a proxy for Elegant Georgian Calligraphy), these levels are the soul of the app. They should be used for names, romantic quotes, and section headers. 
    *   *Scale Tip:* Don't be afraid of the `display-lg` (3.5rem). High-end editorial design often uses oversized type as a graphic element.
*   **The Detail (Title, Body, Label):** Utilizing **Manrope**. This clean, geometric sans-serif provides the "Modern" counter-balance. It ensures that logistical details (dates, maps, RSVP instructions) remain hyper-legible and premium. Use `label-sm` for metadata with increased letter-spacing (e.g., 0.05rem) to mimic architectural notation.

## 4. Elevation & Depth: Tonal Layering
We reject the heavy drop shadows of the early web. Our depth is achieved through physical layering.

*   **The Layering Principle:** Stack `surface-container` tiers from Lowest (furthest back) to Highest (closest to user). An RSVP card should be `surface-container-highest` placed on a `surface` background to create a soft, natural "lift."
*   **Ambient Shadows:** If a component must float (like a floating action button), use a shadow tinted with `on-surface` at 6% opacity with a blur radius of at least `24px`. It should feel like a shadow cast by soft sunlight, not a digital effect.
*   **The "Ghost Border" Fallback:** If accessibility requires a container edge, use the `outline-variant` token at **15% opacity**. This creates a "whisper" of a boundary that doesn't break the artistic flow.

## 5. Components: The Bespoke Suite

*   **Buttons:**
    *   *Primary:* Softly rounded (`round-lg`), using the Gold Gradient (`primary` to `primary-container`).
    *   *Secondary:* `surface-container-highest` background with `secondary` text. No border.
*   **Expressive Chips:** Used for "Interests" or "Dietary Requirements." Use the `tertiary-container` with an organic, slightly more rounded shape (`round-full`) to look like paint dabs.
*   **Input Fields:** Text inputs should be "Minimalist Stationery" style—only a bottom stroke using the `outline-variant` (20% opacity), with the label in `title-sm` Manrope.
*   **Cards & Lists:** 
    *   **Strict Rule:** No dividers. Separate list items using `16px` of vertical white space or a subtle `surface-container-low` background on alternating items.
*   **The "Wax Seal" Action:** A custom floating button inspired by the reference image. A circular (`round-full`) button with a `tertiary` (pink/purple) base and a gold `primary` icon, mimicking a traditional wax seal for the "Send RSVP" action.

## 6. Do's and Don'ts

### Do:
*   **Do use Asymmetry:** Place a hand-painted brush stroke (`tertiary`) overlapping the edge of a clean photo or card.
*   **Do embrace White Space:** Luxury is defined by the space you *don't* use. Let the "Soft Ivory" background breathe.
*   **Do use High-Contrast Scales:** Pair a very large `display-lg` heading with a very small, tracked-out `label-sm` sub-header.

### Don't:
*   **Don't use 100% Black:** Use `on-surface` (`#31332f`) for text to maintain the "ink on paper" softness.
*   **Don't use Sharp Corners:** Always utilize the **Refined Roundness** scale (minimum `md: 0.375rem`) to keep the aesthetic romantic and approachable.
*   **Don't Grid-Lock:** Avoid perfectly centered, boxy layouts. Allow elements to "float" and overlap slightly, mimicking a flat-lay photography style.
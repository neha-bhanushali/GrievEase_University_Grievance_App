# Design System Documentation

## 1. Overview & Creative North Star: "The Empathetic Architect"

This design system is built to transform the bureaucratic friction of university grievances into a streamlined, high-end editorial experience. Our Creative North Star is **The Empathetic Architect**. 

Standard university software is often cluttered, rigid, and cold. This system rejects that "template" look. We utilize intentional asymmetry, breathable negative space, and sophisticated tonal layering to create an environment that feels both authoritative and approachable. By breaking the grid with overlapping glass elements and leveraging a high-contrast typographic scale, we guide the student’s journey from frustration to resolution with professional poise.

---

## 2. Colors & Surface Philosophy

The palette is rooted in the depth of **Deep Indigo** (`primary`), energized by **Coral** (`secondary`) for decisive actions, and calmed by **Mint** (`tertiary`) for resolution.

### The "No-Line" Rule
To achieve a premium, custom feel, **1px solid borders for sectioning are strictly prohibited.** Boundaries must be defined solely through background shifts. For instance, a `surface-container-low` section sitting on a `surface` background creates a natural, sophisticated break without the "cheapness" of a line.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of frosted glass. 
- **Base Layer:** `surface` (#f8f9fa)
- **Content Blocks:** Use `surface-container-low` to define major content areas.
- **Interactive Focus:** Nest `surface-container-lowest` (#ffffff) within those blocks to pull specific information forward.

### The "Glass & Gradient" Rule
Standard flat colors lack "soul." 
- **Glassmorphism:** For floating headers or navigation, use a semi-transparent `surface` color with a `backdrop-filter: blur(20px)`. 
- **Signature Gradients:** Main CTAs should transition from `primary` (#142588) to `primary_container` (#303f9f) at a 135-degree angle. This subtle shift provides a tactile, "lit-from-within" quality.

---

## 3. Typography: Editorial Authority

We use a dual-font approach to balance professional weight with modern clarity.

*   **Headlines (Manrope):** High-impact, geometric, and authoritative. Use `display-lg` for welcome screens and `headline-md` for section headers to create an editorial rhythm.
*   **Interface (Plus Jakarta Sans):** Used for `label-md` and `label-sm`. Its slightly wider apertures ensure readability in dense functional areas like forms and status chips.

**Hierarchy as Identity:** 
Always lead with a strong `headline-sm` or `headline-md` followed by a generous gap before `body-md`. This "breathing room" prevents the user from feeling overwhelmed during the grievance process.

---

## 4. Elevation & Depth: Tonal Layering

We avoid traditional "material" shadows in favor of ambient, atmospheric depth.

*   **The Layering Principle:** Instead of an "Outer Glow," place a `surface-container-lowest` card on a `surface-container-low` background. This creates a soft, natural lift.
*   **Ambient Shadows:** For floating action buttons or modal cards, use a tinted shadow. The shadow should be `primary` at 6% opacity with a `24px` blur and `8px` Y-offset. This mimics natural light reflecting off the indigo brand colors.
*   **The "Ghost Border":** If a border is required for accessibility (e.g., in high-contrast mode), use `outline-variant` at 20% opacity. Never use 100% opaque lines.
*   **Glassmorphism Depth:** Elements using glassmorphism must use a `0.5px` border of `on-surface-variant` at 10% opacity to mimic the "catch-light" on the edge of a pane of glass.

---

## 5. Component Guidelines

### Buttons: Decisive & Vibrant
*   **Primary:** Gradient fill (`primary` to `primary_container`), `xl` roundedness (1.5rem), and white text.
*   **Secondary (Coral):** Use `secondary` (#a43c12) for high-urgency actions (e.g., "Submit Grievance"). It should feel like a "pulse" against the indigo background.
*   **Tertiary:** No background; use `primary` text with a subtle `surface-container-highest` hover state.

### Input Fields: The Quiet Foundation
*   **Style:** Minimalist. No bottom line. Use a `surface-container-high` background with `md` (0.75rem) corners.
*   **Focus State:** Transition the background to `surface-container-lowest` and apply a "Ghost Border" of `primary` at 20%.

### Cards & Lists: Flow over Friction
*   **The No-Divider Rule:** Forbid the use of divider lines in lists. Instead, use a `16px` vertical gap between items.
*   **Grievance Cards:** Use a glass effect for cards in "pending" states. Use `surface-container-lowest` for "resolved" states to provide a sense of finality and solid ground.

### Status Chips
*   **Success (Mint):** Use `tertiary_fixed` (#93f993) with `on_tertiary_fixed_variant` text.
*   **Urgent (Coral):** Use `secondary_fixed` (#ffdbcf) with `on_secondary_fixed` text.
*   **Shape:** Always `full` (9999px) pills for a modern, friendly feel.

---

## 6. Do’s and Don’ts

### Do:
*   **DO** use whitespace as a functional tool. If a screen feels cluttered, increase the margin between the header and the first card.
*   **DO** use overlapping elements. A card slightly overlapping a gradient header creates a sense of depth and custom design.
*   **DO** use `manrope` for numbers. Its geometric clarity makes tracking case IDs or dates feel premium.

### Don't:
*   **DON'T** use pure black (#000000) for shadows or text. Use `on-surface` (#191c1d) to maintain tonal harmony.
*   **DON'T** use standard 1px borders to separate content. If you need a separation, use a `12px` height `surface-dim` spacer or a background shift.
*   **DON'T** use sharp corners. Use the `lg` (1rem) or `xl` (1.5rem) tokens to keep the experience feeling modern and soft.
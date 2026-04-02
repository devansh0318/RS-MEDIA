# Design System Document: RS Media Group

## 1. Overview & Creative North Star

### Creative North Star: "The Kinetic Monument"
In the world of outdoor advertising, impact is measured by the split-second gaze of a passerby. This design system moves beyond static layouts to embrace **The Kinetic Monumentalism**—a visual philosophy that combines the heavy, authoritative presence of a billboard with the fluid, high-velocity energy of Bikaner’s rising media landscape. 

We break the traditional "template" look by using **aggressive diagonal cuts** and **overlapping architectural layers**. By eschewing standard grids in favor of intentional asymmetry, the UI mimics the physical experience of urban scale. Large-scale typography sits behind foreground elements, and interactive components emit a "digital glow," ensuring the brand feels ambitious, rooted, and impossible to ignore.

---

## 2. Colors

The color palette is a high-contrast dialogue between Rajasthan’s adventurous spirit and corporate excellence.

### Core Palette
- **Primary (`#0047FF` / `primary_container`):** Deep Electric Blue. Use this as the anchor for authority and digital precision.
- **Secondary (`#FF6B00` / `secondary_container`):** Bright Orange. This is our "Energy" token, used for high-intent actions and visual highlights.
- **Background (`#F4F6FF` / `surface`):** Light Silver. A cool, crisp canvas that rejects "dull" whites in favor of a premium metallic undertone.

### The "No-Line" Rule
**Strict Mandate:** Prohibit 1px solid borders for sectioning. Boundaries must be defined solely through background color shifts. For example, a `surface-container-low` section sitting on a `surface` background creates a natural architectural break. Content should breathe; lines are barriers, but tonal shifts are invitations.

### The "Glass & Gradient" Rule
To elevate the brand, utilize the **RS Signature Gradient**: A linear transition from `primary` (#0035c5) to `primary_container` (#0047ff) at a 135-degree angle. For floating elements, apply **Glassmorphism**: semi-transparent `surface_container_lowest` (opacity 80%) with a `backdrop-blur` of 20px. This ensures the vibrant silver background bleeds through, creating a "frosted" high-end tech feel.

---

## 3. Typography

The typography is an editorial mix of raw power and modern readability.

*   **Headings (Montserrat ExtraBold / Plus Jakarta Sans):** These are our "Billboard Headings." Used at `display-lg` and `headline-lg` scales. Tight letter-spacing (-0.02em) and massive scale communicate dominance.
*   **Body (Poppins Light/Regular / Be Vietnam Pro):** Poppins provides a clean, geometric counter-balance to the aggressive headings. Use Regular for readability and Light for subtle secondary descriptions.
*   **Accents (Barlow Condensed Uppercase / Space Grotesk):** These are our "Utility Labels." Used for metadata, breadcrumbs, and small callouts. The condensed nature feels industrial and efficient.

---

## 4. Elevation & Depth

### The Layering Principle
Depth is achieved by "stacking" surface-container tiers. 
1.  **Level 0:** `surface` (#F4F6FF) – The base layer.
2.  **Level 1:** `surface-container-low` – Used for large background sections (e.g., service listings).
3.  **Level 2:** `surface-container-lowest` (#FFFFFF) – Used for "High-Impact" cards to make them pop against the silver base.

### Ambient Shadows & Glowing CTAs
Traditional "drop shadows" are forbidden. Instead, use **Ambient Tonal Shadows**:
- Blur: 40px to 60px.
- Opacity: 6% to 10%.
- Color: Tinted with `primary` (#0047FF) to create a subtle blue aura rather than a grey smudge.
- **The Glow Effect:** For `secondary` buttons, use a dual-layer shadow—one tight 4px shadow for definition and one wide 20px orange-tinted shadow to simulate a neon "glow" effect.

### The "Ghost Border" Fallback
If separation is absolutely required in tight spaces, use the `outline_variant` token at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### The "Founder Spotlight" (Signature Component)
Incorporate the photo of Pintu Rathi using a **diagonal mask**. The background behind the subject should feature a `primary` to `secondary` radial gradient "spotlight" centered behind the head, creating a halo effect that symbolizes visionary leadership.

### Buttons
- **Primary (Electric Blue):** Heavy-weight Poppins. 1.4rem padding. `rounded-md` (0.375rem).
- **CTA (Bright Orange):** Features the "Glow" shadow. Use diagonal "clip-path" on the hover state to mimic a shutter opening.
- **Tertiary:** Transparent background with `Barlow Condensed` uppercase text and a 2px bottom-heavy underline in `secondary`.

### Cards & Lists
- **Rule:** No divider lines. Use `spacing-8` (2.75rem) to separate list items.
- **Cards:** Use `surface-container-lowest` with a subtle `rounded-xl` (0.75rem) corner. The top-right corner should feature a "Diagonal Cut" (15-degree angle) containing the brand mark or a category label.

### Input Fields
- **State:** Minimalist but bold. No borders.
- **Style:** `surface-container-high` background with a 2px `secondary` bottom-border that animates from the center outward on focus.

---

## 6. Do's and Don'ts

### Do's
*   **DO** use diagonal "Wave Shapes" to transition between major sections (e.g., Hero to Portfolio).
*   **DO** overlap typography. A large `display-lg` headline should partially be obscured by a high-quality billboard render or the "Founder Spotlight."
*   **DO** use the spacing scale religiously. Luxury is defined by generous white space (`spacing-20` and `spacing-24`).

### Don'ts
*   **DON'T** use black. Use `on_background` (#181c22) for text. True black is too harsh for this silver-based system.
*   **DON'T** use rounded corners on everything. Mix `rounded-none` for large diagonal containers with `rounded-md` for buttons to maintain an "architectural" feel.
*   **DON'T** use flat, saturated orange for text. Only use Orange (`secondary`) for buttons, accents, and icons. It is a "light" to be followed, not a "path" to be read.
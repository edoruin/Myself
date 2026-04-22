# Design System: Scholar Ink

### 1. Overview & Creative North Star
**Creative North Star: "The Digital Curator"**
Scholar Ink is a design system that marries academic rigor with high-end editorial aesthetics. It moves away from the "app-like" density of standard interfaces toward a "Slide & Portfolio" feel—where every screen is treated as a curated composition. The system prioritizes breathing room, monochromatic depth, and intentional asymmetry to elevate technical content into a premium narrative experience.

### 2. Colors
The palette is rooted in the "Slate" scale, moving from deep ink blacks to ethereal, paper-like whites.

*   **Primary Roles:** Defined by `#0f172a` (Slate 900). This is used for high-impact typography and anchor elements.
*   **Neutral Roles:** The system uses `#f8fafc` (Slate 50) as the canvas, providing a crisp, slightly cool foundation.
*   **The "No-Line" Rule:** Sectioning is strictly prohibited from using 1px solid borders. Boundaries must be established through shifts from `surface` to `surface_container_low` or through the "Monolith" technique—heavy, dark containers (`primary_container`) set against light backgrounds.
*   **Surface Hierarchy & Nesting:** 
    *   **Level 0 (Background):** `#f8fafc` (The foundation).
    *   **Level 1 (Cards):** `#ffffff` (Elevated focus).
    *   **Level 2 (Insets):** `#f1f5f9` (Subtle grouping).
*   **Signature Textures:** A subtle "Particles" overlay (1px radial dots) should be applied to the base background to provide a tactile, paper-like quality that breaks digital flatness.

### 3. Typography
Scholar Ink utilizes **Manrope** across all roles to maintain a unified, modern-mathematical feel, occasionally supplemented by Monospace for technical attributes.

**Typography Scale (Calibrated to Ground Truth):**
*   **Display (8xl):** `3rem` (on mobile) to `8xl` equivalent for hero names. Tracking is set to `tighter` with a `1.1` line-height to create "text-as-image" blocks.
*   **Headline (3xl - 5xl):** `1.875rem` to `3rem`. Used for section headers.
*   **Title (xl):** `1.25rem`. Used for role descriptors and card titles.
*   **Body (lg):** `1.125rem`. Set to `font-light` with `leading-relaxed` for long-form narrative readability.
*   **Label (sm/xs):** `0.875rem` to `0.75rem`. Characterized by `tracking-widest` and uppercase styling for "Professional Portfolio" tags and metadata.

### 4. Elevation & Depth
Elevation is achieved through extreme diffusion rather than structural shadows.

*   **The Layering Principle:** Depth is created by "stacking." A white card (`surface_container_lowest`) sits on a slate-50 background, while a dark "Monolith" block (`primary_container`) overlaps the card.
*   **Ambient Shadows (shadow-2xl):** As seen in the source, shadows are extremely soft and large. Use a 25px to 50px blur with low opacity (10-15%) to make elements feel as though they are floating inches above the paper.
*   **Asymmetric Shapes:** Use `clip-path` (e.g., `polygon(0 0, 100% 0, 100% 85%, 85% 100%, 0 100%)`) on secondary floating elements to create a bespoke, non-templated geometry.

### 5. Components
*   **Buttons:** Standard buttons are avoided. Instead, use "Text-Link Buttons" with a 1px `border-b` that changes color on hover, or high-contrast pill-shaped chips for CTA's.
*   **Cards:** Use `rounded-4xl` (2rem/32px) corner radii. Cards should frequently be "broken" by overlapping images or text blocks that extend beyond the card's perceived border.
*   **Monolith Blocks:** Solid, dark containers (`primary_container`) with white or slate-300 text. These serve as the "summary" or "key stats" area within a screen.
*   **Skill Bars:** Minimalist 4px height bars. The background track should be `white/20` and the progress fill should be `white/100` when placed on dark containers.

### 6. Do's and Don'ts
*   **Do:** Use grayscale images with a "color-on-hover" transition to maintain the editorial aesthetic.
*   **Do:** Allow typography to overlap visual elements (images/shapes).
*   **Don't:** Use standard material shadows (Level 1-3). Stick to the "shadow-2xl" deep-glow style.
*   **Don't:** Use bright accent colors for navigation. Navigation should be quiet, using `slate-500` and moving to `slate-900` only on interaction.
*   **Do:** Use "Tracking-Widest" for all uppercase labels to signify professional intent.
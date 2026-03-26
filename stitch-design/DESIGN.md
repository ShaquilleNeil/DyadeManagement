# Design System Strategy: Architectural Precision

This document outlines the visual language and implementation guidelines for the design system. Created for a high-end construction firm, this system rejects "industrial" clichés in favor of "Architectural Precision"—an editorial-inspired approach that treats digital space with the same intentionality as a physical floor plan.

---

## 1. Overview & Creative North Star
**The Creative North Star: "The Master Builder’s Manuscript"**

Most construction websites feel cluttered and transactional. This design system breaks that template by utilizing **monolithic layouts** and **asymmetric balance**. We treat the screen as a canvas of raw materials—deep obsidian foundations, warm amber illumination, and precise typography.

By prioritizing generous whitespace (using our `16`, `20`, and `24` spacing tokens) and overlapping elements, we create a sense of three-dimensional depth. The goal is to move beyond "standard UI" into a space that feels curated, professional, and permanent.

---

## 2. Color Theory & Tonal Depth
We move away from flat hex codes to a system of **Environmental Lighting**. Our palette mimics the experience of a high-end interior at dusk: dark shadows contrasted by warm, directed light.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders to define sections. In this system, structure is defined by **Tonal Transitions**. 
*   To separate a section, shift the background from `surface` (#0c1324) to `surface-container-low` (#151b2d).
*   Boundaries are felt through color shifts, not drawn with lines.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. Use the surface-container tiers to create "nested" importance:
1.  **Base Layer:** `surface` (#0c1324) - The foundation.
2.  **Sectional Shifts:** `surface-container-low` (#151b2d) - For large content blocks.
3.  **Component Cards:** `surface-container-high` (#23293c) - For interactive elements.

### The "Glass & Gradient" Rule
To prevent the dark theme from feeling "heavy," use Glassmorphism for floating navigation or overlays. 
*   **Token:** Use `surface_bright` at 60% opacity with a `20px` backdrop-blur.
*   **Signature Textures:** Apply a subtle linear gradient to main CTAs (from `primary_container` #f59e0b to `primary` #ffc174) to simulate the glow of an amber light source.

---

## 3. Typography: The Editorial Edge
Our typography is the "blueprint" of the experience. We use **Manrope** for its geometric, architectural qualities in headings, and **Inter** for its unparalleled legibility in data and body copy.

*   **Display (Manrope):** Use `display-lg` (3.5rem) with `tight` letter-spacing for hero statements. This conveys authority and scale.
*   **Headlines (Manrope):** Always bold. Use `headline-lg` (2rem) for project titles.
*   **Body (Inter):** Use `body-lg` (1rem) with a generous `1.7` line-height. Construction is complex; our reading experience should be effortless.
*   **Labels (Inter):** Use `label-md` (0.75rem) in `all-caps` with `0.1rem` letter spacing for technical specs or categories.

---

## 4. Elevation & Depth
In this design system, "Elevation" is a measure of light, not just shadow.

### The Layering Principle
Stack tiers to create soft, natural lift. Place a `surface-container-lowest` card onto a `surface-container-low` background. This "negative lift" creates a sophisticated, recessed look that feels carved into the interface.

### Ambient Shadows
Shadows must be invisible until noticed.
*   **Spec:** `Blur: 40px`, `Spread: 0`, `Opacity: 6%`.
*   **Color:** Use a tinted version of `on-surface` (#dce1fb) rather than pure black to keep the shadows "airy."

### The "Ghost Border" Fallback
If a container requires a border for accessibility (e.g., input fields), use a **Ghost Border**:
*   `outline-variant` (#534434) at **15% opacity**. 100% opaque borders are strictly forbidden.

---

## 5. Component Guidelines

### Buttons (The Tactile Interaction)
*   **Primary:** Background `primary_container` (#f59e0b), Text `on_primary_container` (#613b00). Use `xl` (1.5rem) roundedness.
*   **Secondary:** Ghost style. No background, Ghost Border (15% opacity `outline-variant`), and `primary` text.
*   **Hover State:** Increase surface brightness by 5% and add a `4px` amber outer glow to simulate a light turning on.

### Cards & Projects
*   **Strict Rule:** No divider lines. Separate content using the `spacing-6` (2rem) token or subtle background shifts between the card header and body.
*   **Radius:** All cards must use `lg` (1rem) or `xl` (1.5rem) corner radius.

### Input Fields
*   **Base:** `surface_container_lowest` (#070d1f).
*   **Focus:** Transition the Ghost Border to `primary` (#ffc174) at 50% opacity.
*   **Labels:** Floating labels using `label-md` for a technical, precise feel.

### Specialized Component: The "Blueprint" Chip
For project status (e.g., "In Progress"), use a chip with `surface_container_highest` background and `tertiary` (#8fd5ff) text. This provides a "technical drawing" aesthetic that complements the construction theme.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical margins. Align a headline to the left but the body text to a center-right column to create an editorial layout.
*   **Do** use high-quality architectural photography with a slightly de-saturated, cool-toned grade to match the `#0c1324` background.
*   **Do** embrace the `20` and `24` spacing tokens for top-level section padding.

### Don't:
*   **Don't** use pure black (#000000). Always use the `surface` token for depth.
*   **Don't** use standard 1px dividers. If you feel the need for a divider, use a `surface-variant` block that is `1px` high but only spans 60% of the container width.
*   **Don't** cram content. If a section feels "full," double the whitespace.
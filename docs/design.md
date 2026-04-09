# Design System Strategy: The Scientific Sanctuary

## 1. Overview & Creative North Star
**Creative North Star: "The Clinical Atelier"**
This design system rejects the clinical coldness of traditional healthcare and the chaotic energy of fitness apps. Instead, it creates a "Clinical Atelier"—a space that is mathematically precise yet artistically empathetic. We move beyond the "template" look by utilizing intentional asymmetry, expansive negative space, and high-contrast typography scales that feel like a high-end wellness editorial.

The goal is to convey **Empathetic Authority**. We achieve this by breaking the rigid grid: images should bleed off-canvas, headlines should overlap subtle tonal containers, and depth should feel organic rather than engineered.

---

## 2. Colors & Tonal Depth

The palette is rooted in deep, authoritative purples transitioned through soft, breathable lavenders to provide a sense of transformative growth.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders for sectioning or containment. Traditional lines create a "boxed-in" feeling that contradicts a transformative wellness journey. Boundaries must be defined solely through background color shifts or subtle tonal transitions.

* **Example:** A `surface-container-low` (#f5f3f5) section sitting on a `background` (#faf9fb) creates a soft, sophisticated edge without a single line.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of frosted glass and fine vellum.
- **Base:** `surface` (#faf9fb)
- **Primary Containers:** `surface-container-low` (#f5f3f5) for large content blocks.
- **Floating Accents:** `surface-container-lowest` (#ffffff) for high-priority cards, creating a "lifted" effect against the background.

### The "Glass & Gradient" Rule
To elevate the experience, use **Glassmorphism** for floating navigation and overlay elements. Apply `surface-container-lowest` at 70% opacity with a `24px` backdrop blur.
- **Signature Texture:** Use a subtle linear gradient (135°) from `primary` (#342a7c) to `primary-container` (#4B4294) for main CTAs to add a "pulse" of energy.

---

## 3. Typography: Editorial Authority

We use a duo-font system to balance scientific expertise with human approachability.

* **Display & Headlines (Manrope):** A geometric sans-serif chosen for its modern, authoritative proportions. Use `display-lg` (3.5rem) with tight tracking (-0.02em) to create a bold, editorial statement.
* **Body & Titles (Inter/DM Sans):** Inter provides exceptional legibility for scientific data, while DM Sans (from the brand profile) should be used for empathetic pull-quotes and secondary titles to soften the clinical edge.

**Identity Through Scale:** Use extreme scale differences. Pair a `display-md` headline with a `body-sm` label to create a sense of professional hierarchy and white-space luxury.

---

## 4. Elevation & Depth

Hierarchy is achieved through **Tonal Layering**, not structural shadows.

* **The Layering Principle:** Stack `surface-container-highest` (#e3e2e4) behind a `surface-container-lowest` (#ffffff) card. The contrast alone provides the "lift."
* **Ambient Shadows:** If a shadow is required for a floating CTA or modal, it must be "Ambient."
* *Spec:* `Blur: 40px`, `Spread: 0`, `Opacity: 6%`, `Color: #1b1c1e` (on-surface). It should feel like a soft glow, not a dark drop.
* **The "Ghost Border" Fallback:** For accessibility in input fields, use `outline-variant` (#c9c4d3) at **15% opacity**. Never use 100% opaque borders.

---

## 5. Components

### Buttons
* **Primary:** Gradient of `primary` to `primary-container`. `Roundedness: full`. No shadow.
* **Secondary:** `surface-container-highest` background with `on-primary-fixed-variant` text.
* **Tertiary:** Ghost style; text only with a `primary` underline that expands on hover.

### Cards & Content Blocks
* **Rule:** Forbid divider lines. Use `1.5rem` to `2.5rem` of vertical white space to separate content.
* **Style:** Use `roundedness-xl` (1.5rem) for all main cards to maintain a friendly, approachable silhouette.

### Input Fields
* **Style:** `surface-container-low` background. No border. On focus, transition the background to `surface-container-lowest` and add a "Ghost Border" of 2px `primary_fixed` (#e4dfff).

### Signature Component: The "Progress Bloom"
Given the weight loss context, replace standard progress bars with a "Progress Bloom"—a circular, glassmorphic container using overlapping circles (referencing the logo) that increase in opacity as the user nears their goal.

---

## 6. Do's and Don'ts

### Do:
* **Asymmetric Layouts:** Place imagery slightly off-center to create a bespoke, high-end feel.
* **Tone-on-Tone:** Use `on-surface-variant` for helper text to reduce visual noise.
* **Breathing Room:** Use the `2.5rem` spacing as your default "breathing" gap between major sections.

### Don't:
* **Don't use pure black:** Use `on-surface` (#1b1c1e) for text to keep the palette soft and sophisticated.
* **Don't use 1px borders:** Rely on background shifts. Lines are for "forms," tonal shifts are for "experiences."
* **Don't crowd imagery:** Allow high-quality photography to occupy 50% of the screen real estate in Hero sections; let the brand's transformative nature speak through visuals.

### Accessibility Note:
While we use soft tonal shifts, always ensure the contrast between `on-surface` and its respective `surface` container meets WCAG AA standards. If a shift is too subtle for a specific screen, use a **Ghost Border** at 10% opacity for definition.

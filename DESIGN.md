# Design System: High-End Editorial Wedding Experience

## 1. Overview & Creative North Star: "The Ethereal Manuscript"
The creative direction for this design system is **"The Ethereal Manuscript."** We are moving away from the "event landing page" template and toward a bespoke, digital heirloom. Inspired by the Pavagadh Hills at sunset, the system prioritizes light, air, and the passage of time. 

To achieve a signature look, we break the traditional grid through **intentional asymmetry**. Images should rarely align perfectly with text blocks; instead, use overlapping layers where a photo might bleed off-edge while a caption sits tucked into a generous margin. This creates a sense of "pacing"—like turning the pages of a high-end fashion editorial.

---

## 2. Colors & Tonal Depth
The palette transitions from the warmth of ivory stone to the deep, muted terracotta of a setting sun.

### The "No-Line" Rule
Standard 1px solid borders are strictly prohibited for structural sectioning. To define boundaries, use **background color shifts**. A section utilizing `surface-container-low` (#f7f3ee) should sit flush against the `background` (#fdf9f4). The transition should be felt, not seen.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of fine vellum paper. 
- **Base Layer:** `surface` (#fdf9f4) for global backgrounds.
- **Content Blocks:** Use `surface-container` (#f1ede8) for large content areas.
- **Interactive Elements:** Use `surface-container-lowest` (#ffffff) for cards to create a "lifted" appearance without shadows.

### The "Glass & Gold" Rule
To capture the "sunset" mood, use Glassmorphism for navigation bars and floating overlays. Use `surface` at 70% opacity with a `20px` backdrop-blur. 
- **Signature Accents:** Apply `secondary` (#735c00) sparingly for "Gold Accents"—primarily for thin ornamental motifs or icons.
- **Tonal Soul:** Use a subtle linear gradient on the Hero CTA: `primary` (#8f4b3f) to `primary_container` (#eb9687) at a 135-degree angle.

---

## 3. Typography: The Romantic Dialogue
The typography system is a dance between the whimsical and the structured.

- **Display & Headlines (notoSerif):** These represent the "Romantic Cursive" intent. Use `display-lg` for the couple's names. Letter spacing should be tight for headlines to feel like hand-inked script, but use generous line-height (1.4+) to maintain airiness.
- **Body & Titles (manrope):** A modern sans-serif that provides a clean, neutral counterpoint. This ensures the "Editorial" feel doesn't become "Old World." 
- **Labeling:** Use `label-md` in all-caps with `0.1rem` letter-spacing for date/time/location details to evoke the feel of a luxury invitation.

---

## 4. Elevation & Depth
We eschew the "Material" look for "Atmospheric" depth.

- **The Layering Principle:** Depth is achieved by stacking. A `surface-container-highest` card placed on a `surface` background creates a natural, tactile elevation.
- **Ambient Shadows:** Only use shadows on floating modals or "Save the Date" popups. Use: `0px 20px 40px rgba(28, 28, 25, 0.06)`. The shadow color is a tinted version of `on-surface`, never pure black.
- **The "Ghost Border" Fallback:** If a container needs definition (e.g., a photo frame), use `outline-variant` (#d4c4b7) at **15% opacity**.
- **Subtle Mandala Motifs:** Use `outline` (#82756a) at 5% opacity as a large, scaled-up background watermark behind text blocks. It should be felt as a texture, not read as a graphic.

---

## 5. Components

### Buttons
- **Primary:** `primary` (#8f4b3f) background with `on-primary` (#ffffff) text. Use `Roundedness.md` (0.375rem). No shadow.
- **Secondary (The Gold Variant):** `outline` (#82756a) border at 40% opacity, `secondary` (#735c00) text.
- **States:** On hover, primary buttons should transition to `primary_container` with a slow 0.4s ease-out.

### Input Fields
- **Styling:** Underline-only style. Use `outline` (#82756a) as a 1px bottom border. Labels should use `body-sm` and sit 8px above the input.
- **Focus:** Transition the bottom border to `primary` (#8f4b3f) with a soft `primary_fixed` glow.

### Cards & Lists
- **Forbid Dividers:** Do not use horizontal lines between list items (e.g., the Schedule of Events). Use 32px of vertical white space or a slight color shift to `surface-container-low` for alternating items.
- **Image Cards:** Images should use `Roundedness.sm` (0.125rem) to maintain a crisp, editorial look.

### Unique Component: The "Ceremony Timeline"
A vertical line using `outline-variant` (#d4c4b7) at 20% opacity. Icons are replaced by `secondary` (#735c00) gold dots. This maintains the "High-End" minimalist aesthetic.

---

## 6. Do’s and Don’ts

### Do:
- **Do** use asymmetrical padding. For example, a 15% left margin and a 5% right margin for text blocks.
- **Do** use "Soft Animations." Every element should fade and slide up 10px when entering the viewport.
- **Do** favor white space. If you think there is enough space, add 20% more.

### Don’t:
- **Don't** use high-contrast black (#000000). Use `on-surface` (#1c1c19) for all text to keep the look "organic."
- **Don't** use "Roundedness.full" for buttons. It feels too much like a tech app; stay with `md` or `none` for an editorial feel.
- **Don't** crowd the Mandala motifs. They are "whispers" in the background, not primary illustrations.
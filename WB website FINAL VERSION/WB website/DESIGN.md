# Design System Document: The Transatlantic Bridge

## 1. Overview & Creative North Star
**Creative North Star: "The Editorial Bridge"**

This design system is built to reflect the dual identity of Westbound Alliance: the centuries-old prestige of Dutch commerce meeting the bold, expansive energy of the American market. We are moving away from "Corporate SaaS" aesthetics toward a **High-End Editorial** experience. 

The system rejects the rigid, boxy constraints of standard web grids in favor of **Intentional Asymmetry** and **Tonal Depth**. Think of the UI as a high-end financial journal or an architectural monograph. We use white space not just as "padding," but as a structural element that commands respect. The "Bridge" is represented through overlapping elements, where bold Navy components intersect with warm Sand backgrounds, creating a physical sense of connection across the Atlantic.

---

## 2. Colors
Our palette balances the "establishment" of the US financial sector with the "heritage" of the Netherlands.

### The Palette
- **Primary (Deep Navy - #0A1628):** Used for primary typography and high-impact containers. It represents power and institutional trust.
- **Secondary (Vibrant Orange - #994600 / #E07830):** Our "Action" color. Use this for CTAs and critical wayfinding. It is the energetic spark of Dutch innovation.
- **Neutral/Surface (Warm Cream/Sand - #F5F0E8 / #F2EFE6):** These are our foundational layers. They prevent the site from feeling cold or clinical.

### The "No-Line" Rule
**Standard 1px borders are strictly prohibited for sectioning.** To define boundaries between content blocks, you must use background color shifts. 
*   *Example:* A `surface-container-low` (#F8F3EB) hero section should transition directly into a `surface` (#FEF9F1) content block. The change in tone is the divider.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of fine stationery.
*   **Base:** `surface` (#FEF9F1).
*   **Secondary Content:** `surface-container` (#F2EDE5).
*   **Floating Elements:** `surface-container-lowest` (#FFFFFF) to create a subtle "lift" against the cream backgrounds.

### The "Glass & Gradient" Rule
To add a "Signature" feel, use Glassmorphism for floating navigation bars or overlay cards. Use a `backdrop-blur` of 12px-20px combined with a semi-transparent `surface-container-lowest` (80% opacity). For primary CTAs, apply a subtle linear gradient from `primary` (#0A1628) to `primary-container` (#101C2E) to give the button a tactile, "weighted" feel.

---

## 3. Typography
The type system is a dialogue between the old world (Newsreader Serif) and the new world (Inter Sans).

*   **Display & Headlines (Newsreader):** Used for storytelling and core value propositions. These should be set with tight leading (1.1) to look like premium editorial headers.
    *   *Display-LG (3.5rem):* Reserved for Hero moments.
*   **Titles & Body (Inter):** Used for functional information and navigational clarity.
    *   **The "Eyebrow" Treatment:** All `label-md` tokens (used for section headers above headlines) must be uppercase with a +10% to +15% letter-spacing. This adds an immediate sense of "high-fashion" precision.
*   **The Hierarchy Goal:** Use the Serif for the "Why" and the Sans-serif for the "How."

---

## 4. Elevation & Depth
We eschew the standard Material Design shadow approach for a more "Ambient" and "Atmospheric" style.

*   **The Layering Principle:** Depth is achieved via **Tonal Stacking**. An article card should be `surface-container-lowest` (#FFFFFF) sitting on a `surface-container` (#F2EDE5) background. This creates a soft, natural edge.
*   **Ambient Shadows:** If a card must float (e.g., a modal or a floating CTA), use a massive blur (40px+) and very low opacity (4%-6%). The shadow color should be a deep navy tint, never pure black.
*   **The "Ghost Border" Fallback:** If a layout feels too "bleary," you may use a Ghost Border. This is a 1px stroke using the `outline-variant` token at **15% opacity**. It should be barely visible, acting as a whisper of a boundary rather than a wall.
*   **Asymmetric Overlaps:** To break the template look, allow images to "break" out of their containers or overlap two different surface colors.

---

## 5. Components

### Buttons
*   **Primary:** Deep Navy background, White text. No border. Radius: `md` (0.375rem).
*   **Secondary (The Bridge):** Vibrant Orange. Use for "Action" items like "Start Consultation."
*   **Tertiary:** Transparent background with a `Ghost Border` and a Serif font-weight of 600.

### Input Fields
*   **Style:** Minimalist. No background color (transparent). Only a bottom stroke using `outline-variant`. On focus, the stroke transitions to `secondary` (Orange).
*   **Labels:** Use `label-md` (Inter) in uppercase above the field.

### Cards & Lists
*   **The No-Divider Rule:** Vertical lists must never use horizontal lines. Use generous vertical spacing (at least 32px) and a subtle background hover state (`surface-container-high`) to define the interactive area.
*   **Editorial Cards:** Use large Serif headlines within cards, paired with high-contrast architectural photography.

### Signature Component: The "Perspective Split"
A recurring component where the screen is split 60/40. The 60% side holds a "Newsreader" headline on a Sand background, while the 40% side holds a high-end, grayscale architectural photo that slightly overlaps the text container.

---

## 6. Do's and Don'ts

### Do
*   **Do** use extreme white space. If it feels like "too much," it’s probably just right.
*   **Do** use "Newsreader" for quotes and testimonials to give them an authoritative, trustworthy voice.
*   **Do** treat photography as art. Use architectural shots of Rotterdam and New York to subtly reinforce the "Bridge" concept.

### Don't
*   **Don't** use 100% black. Use `on-primary-fixed` (#101C2E) for text to keep the "Navy" soul alive.
*   **Don't** use standard "drop shadows" or heavy borders.
*   **Don't** center-align long blocks of text. Stick to sophisticated left-aligned editorial layouts.
*   **Don't** use icons as primary decors. This is an editorial system; let typography and photography do the heavy lifting.
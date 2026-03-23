# Design System Strategy: The Neon Pulse

## 1. Overview & Creative North Star: "The Neon Pulse"
This design system is engineered to capture the kinetic energy of live performance. Moving away from static, boxy social media templates, our Creative North Star is **"The Neon Pulse."** This philosophy treats the UI not as a flat screen, but as a multi-layered stage where content is the protagonist and the interface is the lighting rig.

To achieve this "High-End Editorial" feel, we reject the rigid grid in favor of **intentional asymmetry**. Hero elements should overlap container boundaries, and typography should vary wildly in scale to create a rhythmic, musical flow. We prioritize depth through light and glass rather than lines and borders, ensuring the app feels like a premium, immersive dark-mode experience.

---

## 2. Colors & Surface Architecture
The palette is rooted in a high-contrast relationship between the void (`#0E0E0E`) and hyper-saturated light.

### The "No-Line" Rule
**Explicit Instruction:** 1px solid borders are strictly prohibited for sectioning. Differentiation must be achieved through background shifts. For example, a `surface-container-low` section sitting on a `background` provides a sophisticated, seamless transition that feels expensive and custom.

### Surface Hierarchy & Nesting
Instead of a flat plane, treat the UI as stacked sheets of obsidian and frosted glass. 
*   **Base:** `background` (#0E0E0E) for the deepest level.
*   **Sections:** Use `surface-container-low` (#131313) for primary content areas.
*   **Focus Cards:** Use `surface-container` (#1A1919) to bring elements forward.
*   **Floating Elements:** Use `surface-container-highest` (#262626) to signify maximum prominence.

### The "Glass & Gradient" Rule
Standard flat buttons are insufficient. Main CTAs and high-energy touchpoints must utilize a **Signature Texture**:
*   **Primary Pulse:** A linear gradient from `primary` (#DF8EFF) to `primary-container` (#D878FF) at a 135° angle.
*   **Glassmorphism:** For floating overlays (like chat bubbles or player controls), use `surface-variant` (#262626) at 60% opacity with a `20px` backdrop-blur. This allows the high-energy livestream content to "bleed" through the UI, integrating the interface with the media.

---

## 3. Typography: Editorial Impact
We utilize a dual-font strategy to balance aggressive brand energy with long-form readability.

*   **Display & Headlines (Plus Jakarta Sans):** These are your "vibe" setters. Use `display-lg` (3.5rem) for stream titles or creator names to create an editorial, "poster" look. High tracking (letter-spacing) should be avoided; keep it tight and bold.
*   **Body & Labels (Inter):** Inter handles the functional heavy lifting. It provides the necessary clarity for fast-moving live chats and UI metadata. 
*   **The Hierarchy Rule:** Create drama by pairing a `display-sm` headline with a `label-sm` metadata tag. This extreme contrast in scale is the hallmark of premium digital design.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are often too "muddy" for high-energy dark modes. We use light to define space.

*   **The Layering Principle:** Depth is achieved by "stacking." A `surface-container-lowest` card placed on a `surface-container-low` background creates a natural "recessed" look without a single pixel of stroke.
*   **Ambient Shadows:** When an element must float (e.g., a Gift Menu), use a large, diffused shadow: `box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4)`. To add "soul," tint the shadow with a 4% hint of the `primary` color.
*   **The "Ghost Border" Fallback:** If a container requires definition against a complex background, use the `outline-variant` token at **15% opacity**. This creates a "shimmer" edge rather than a hard line.

---

## 5. Component Guidelines

### Buttons (High-Energy Variants)
*   **Primary:** Gradient fill (`primary` to `primary-container`), `md` (1.5rem) or `lg` (2rem) corner radius. Use `on-primary` (#4F006D) for text to ensure high-contrast legibility.
*   **Secondary:** `surface-container-highest` background with a `secondary` (#00EEFC) text/icon color. 
*   **Glass Action:** `backdrop-blur(12px)` with a 20% white overlay for buttons sitting directly on top of video feeds.

### Cards & Lists
*   **Strictly Prohibited:** Dividers and lines. 
*   **Separation:** Use `spacing-8` (2rem) of vertical whitespace or a subtle shift from `surface` to `surface-container-low`.
*   **Interaction:** On hover/active states, transition the background color slightly higher in the surface tier (e.g., from `surface-container` to `surface-container-high`).

### Livestreaming Specifics
*   **The Pulse Badge:** "LIVE" indicators should use `tertiary` (#FF8D86) with a subtle outer glow (drop-shadow) of the same color to mimic a neon sign.
*   **Chat Bubbles:** Use `surface-container-low` with a `sm` (0.5rem) corner radius. For the streamer's own comments, use a `glassmorphism` effect to make them stand out in the feed.
*   **Gifting Chips:** Selection chips should use the `full` (9999px) radius and the `secondary_fixed` (#00EEFC) color for high visibility.

---

## 6. Do’s and Don’ts

### Do
*   **DO** use the `xl` (3rem) corner radius for large hero cards to emphasize the "sleek" aesthetic.
*   **DO** overlap elements (e.g., a creator's avatar overlapping the edge of a video thumbnail) to break the "boxed-in" feel.
*   **DO** use `surface-bright` (#2C2C2C) for active states on dark surfaces.

### Don't
*   **DON'T** use pure white (#FFFFFF) for long-form body text; use `on-surface-variant` (#ADAAAA) to reduce eye strain in dark mode.
*   **DON'T** use standard 1px borders. If you feel the need for a line, use a 2rem gap of whitespace instead.
*   **DON'T** use harsh, small-radius corners. Anything under 16px (`DEFAULT`) is too "corporate" for this system.

---

## 7. Spacing & Rhythm
This system breathes. Use `spacing-10` (2.5rem) and `spacing-12` (3rem) as your default "macro" padding for sections. Reserve smaller spacing (`spacing-2` to `4`) strictly for internal component groupings. The goal is a layout that feels spacious, confident, and premium.
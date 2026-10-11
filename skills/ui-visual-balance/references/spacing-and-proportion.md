# Spacing and Proportion

This document defines systems for managing spatial relationships, component padding, margins, container constraints, and proportional harmony across screens.

---

## 1. Spacing Systems

Always anchor layout decisions to a consistent spacing scale rather than arbitrary, one-off values.

### The 8pt / 4pt Spatial Cadence

Base your layout measurements on an 8-point system, using 4-point steps for micro-adjustments:

| Step | Value | Primary Usage |
| :--- | :--- | :--- |
| **3xs** | `2px` / `0.125rem` | Micro hairline offsets, focus rings, fine border alignments |
| **2xs** | `4px` / `0.25rem` | Tight inline gaps, icon-to-label spacing, badge padding |
| **xs** | `8px` / `0.5rem` | Form field internal padding (vertical), compact button padding |
| **sm** | `12px` / `0.75rem` | Standard card internal padding (compact), input horizontal padding |
| **md** | `16px` / `1rem` | Standard gutter, default card padding, list gap |
| **lg** | `24px` / `1.5rem` | Container padding, card padding (spacious), section subtitle margin |
| **xl** | `32px` / `2rem` | Component separation, modal padding, column gaps |
| **2xl** | `48px` / `3rem` | Major section gap, dashboard widget separation |
| **3xl** | `64px` / `4rem` | Page section padding (vertical), marketing section gaps |
| **4xl** | `96px+` / `6rem+` | Hero section vertical breathing room |

---

## 2. Spatial Relationships: Proximity Law

The distance between two elements signals their semantic relationship:

* **Internal Padding < Element Margin**: The padding inside a component must always be distinct from the margin separating it from sibling components.
* **Label to Input < Input to Next Group**: Form labels must sit closer to their associated input field (`4px`–`8px`) than the distance to the subsequent input field (`16px`–`24px`).
* **Heading to Body < Body to Next Section**: A heading must sit closer to the paragraph it introduces (`8px`–`16px`) than to the section preceding it (`32px`–`48px`).

---

## 3. Container Widths and Page Bounds

Unconstrained layouts cause elements to drift apart on wide screens, destroying visual cohesion.

### Standard Layout Constraints

* **Reading / Prose Containers**: Max width `65ch` to `75ch` (approximately `640px`–`720px`). Text lines spanning wider viewports become fatiguing to read.
* **Form / Authentication Cards**: Max width `400px` to `480px`. Constrains inputs to a predictable, easily scannable vertical line.
* **Standard Web Application Shell**: Max width `1200px` to `1440px`. Ensures dashboards and data grids do not over-stretch across ultra-wide monitors.
* **Full-Width Bleed**: Reserved strictly for dominant background canvases (60% Primary) and panoramic hero visuals, while internal content remains bound to the layout grid.

---

## 4. Component Proportions & Padding Balance

### Button & Pill Proportions

* Horizontal padding should typically be **1.5x to 2x** the vertical padding (e.g., `8px` vertical, `16px` horizontal; or `12px` vertical, `24px` horizontal).
* Buttons with identical vertical and horizontal padding look square, heavy, and unrefined.

### Card Padding Proportions

* Outer card padding must be proportional to internal content density:
  * Compact data card: `16px` padding, `12px` row gap.
  * Standard content card: `24px` padding, `16px`–`20px` row gap.
  * Hero/Feature card: `32px`–`48px` padding, `24px` row gap.

---

## 5. Responsive Spacing Adaptation

Spacing must contract gracefully on smaller viewports to prevent empty gaps from displacing core content:

```text
Desktop (>= 1024px)     Tablet (768px - 1023px)     Mobile (< 768px)
--------------------     -----------------------     ----------------
Section Y: 64px - 96px   Section Y: 48px - 64px      Section Y: 32px - 40px
Container X: 32px        Container X: 24px           Container X: 16px
Component Gap: 24px      Component Gap: 16px         Component Gap: 12px
Card Padding: 24px       Card Padding: 20px          Card Padding: 16px
```

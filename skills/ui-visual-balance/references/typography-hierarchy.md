# Typography Hierarchy & Readability

This document defines standards for text scaling, weights, line heights, line lengths, and typographic contrast.

---

## 1. Type Scale & Functional Roles

Maintain a clear modular scale (e.g., 1.200 Minor Third or 1.250 Major Third) so font sizes have distinct, recognizable differences:

| Level | Size (rem / px) | Weight | Line Height | Role |
| :--- | :--- | :--- | :--- | :--- |
| **Display** | `2.5rem`–`3.5rem` (40–56px) | Bold / Black (700–900) | `1.1`–`1.15` | Hero titles, landing page focal statements |
| **Heading 1** | `2.0rem`–`2.25rem` (32–36px) | Bold (700) | `1.2`–`1.25` | Primary page title, dashboard screen name |
| **Heading 2** | `1.5rem`–`1.75rem` (24–28px) | Semi-Bold (600) | `1.25`–`1.3` | Major section headers, card modal titles |
| **Heading 3** | `1.25rem` (20px) | Semi-Bold (600) | `1.3`–`1.35` | Sub-sections, individual card titles |
| **Body (Default)** | `1.0rem` (16px) | Regular (400) | `1.5`–`1.6` | Standard body copy, form fields, long reading |
| **Body (Compact)** | `0.875rem` (14px) | Regular / Medium (400/500) | `1.4`–`1.5` | Table cell data, secondary notes, sidebars |
| **Caption / Meta** | `0.75rem` (12px) | Medium (500) | `1.3`–`1.4` | Timestamps, tags, fine print, field hints |

---

## 2. Typographic Contrast Rules

Hierarchy is built through contrast between adjacent text elements.

* **Size Difference Rule**: Never place two different headings adjacent to one another if their size difference is less than 4px. If Heading 1 is 24px and Heading 2 is 22px, the eye perceives an error rather than a hierarchy.
* **Weight Difference Rule**: Pair heavy headings (600–700) with regular body text (400). Avoid pairing 500-weight headings with 400-weight body text unless size difference is substantial.
* **Tone & Color Contrast**:
  * Primary Headings: High contrast (`--text-primary`, e.g., Slate 900 on white).
  * Body Copy: Balanced neutral (`--text-body`, e.g., Slate 700 on white).
  * Secondary Metadata: Muted neutral (`--text-muted`, e.g., Slate 500 on white).
  * Never reduce contrast below WCAG AA thresholds (4.5:1 for body text, 3:1 for large text).

---

## 3. Line Length & Measure

* **Optimal Line Length**: **45 to 75 characters per line** (including spaces). Around 60 characters is ideal for reading comfort.
* **Too Long (> 85 characters)**: The eye struggles to find the start of the next line when scanning back to the left edge.
* **Too Short (< 35 characters)**: The eye must break rhythm constantly, fragmenting sentences and increasing cognitive fatigue.

---

## 4. Line Height (Leading) Mechanics

* **Inverse Relationship with Font Size**:
  * Large Display & Headings require **tighter leading** (`1.1` to `1.25`). Loose leading on huge text causes lines to look disconnected.
  * Body copy requires **comfortable leading** (`1.5` to `1.65`) to allow the eye to track smoothly between lines.
  * Dense table data or UI labels require **compact leading** (`1.2` to `1.35`) to prevent container bloat.

---

## 5. Common Typographic Mistakes to Flag

1. **All-Caps Body Text**: Reserve uppercase styling strictly for short 1–2 word badges, eyebrows, or table header labels with expanded letter-spacing (`tracking-wider`). Never apply all-caps to sentences.
2. **Centered Long-Form Copy**: Never center-align text longer than 3 lines. Left-align body copy to give the eye a stable visual anchor on the left margin.
3. **Too Many Font Sizes**: If a single card component utilizes 5 different font sizes, consolidate down to at most 2 or 3 distinct scale steps.

---
name: ui-visual-balance
description: Evaluates and improves the visual balance, spacing, 60/30/10 color distribution, visual hierarchy, and clutter reduction of web and application interfaces across code, mockups, and designs.
---

# UI Visual Balance & Composition

## Purpose

This skill equips agents to evaluate, audit, design, and refactor user interfaces for visual balance, intentional whitespace, disciplined color application, and unambiguous hierarchy.

---

## When to Activate

Activate this skill when:

- Auditing existing UI code, components, wireframes, or screenshots for visual polish and balance.
- Designing or implementing new layouts, landing pages, dashboards, forms, or UI components.
- Refactoring cluttered interfaces to reduce cognitive load.
- Reviewing PRs or codebases for spatial consistency, typography scales, or color restraint.
- Resolving competing visual elements or broken visual hierarchy.

---

## Core Principles at a Glance

1. **Whitespace as an Active Element**: Space is intentional structure, not an empty void to fill. Never add elements merely to occupy empty canvas.
2. **60 / 30 / 10 Color Distribution**: Limit views to 3 core visual roles: 60% dominant canvas (Primary), 30% structural panels and surfaces (Secondary), and 10% scarce focal actions (Accent).
3. **Hierarchy and Anchor Points**: Every screen must have a clear entry point. Determine what users should see first, next, and last.
4. **Ruthless De-cluttering**: If everything looks important, nothing is important. Eliminate gratuitous borders, shadows, icons, and nested containers.

*For in-depth explanations, consult [Visual Principles](references/visual-principles.md).*

---

## Operational Workflow

### Mode A: Visual Audit

Execute when reviewing, critiquing, or diagnosing a user interface.

1. **Establish Inspection Modality**:
   - If screenshots or browser viewports are provided: conduct an empirical visual inspection.
   - If only source code or markup is provided: perform a static structural inspection. Explicitly state to the user that findings are derived from source code analysis, not a rendered visual canvas.
2. **Identify Primary Intent & Focal Point**:
   - Determine the single most important action or data point the user must see first.
3. **Audit Against Core Criteria**:
   - Evaluate against the 4-part framework: Space, Color, Hierarchy, and Purpose.
   - Consult [Spacing and Proportion](references/spacing-and-proportion.md) for padding, grid, and density issues.
   - Consult [Typography Hierarchy](references/typography-hierarchy.md) for font weight, measure, and scale conflicts.
   - Consult [Layout Patterns](references/layout-patterns.md) for pattern-specific anti-patterns.
4. **Synthesize Findings**:
   - State the highest-impact visual friction points backed by concrete file/line references or visual coordinates.
   - Deliver prioritized, actionable recommendations ranked from structural layout fixes to micro-refinements.

### Mode B: Visual Improvement & Implementation

Execute when modifying, refactoring, or generating interface code.

1. **Inspect Existing Context**:
   - Analyze existing design tokens, CSS variables, utility classes, and component primitives before touching styles.
   - Never introduce arbitrary hex codes, arbitrary spacing values, or new typography scales if project tokens exist.
2. **Determine Minimal Effective Changes**:
   - Favor adjusting margins, padding, alignment, font weights, and contrast over rewriting DOM trees or replacing components.
3. **Execute Non-Destructive Refactoring**:
   - Preserve application state, event handlers, accessibility attributes, and responsive breakpoints.
   - Apply semantic color roles (60% background, 30% surface, 10% accent).
4. **Verify Across Viewports & Accessibility**:
   - Verify that whitespace scales appropriately from mobile to desktop viewports.
   - Ensure text contrast meets WCAG AA standards (minimum 4.5:1 for body text, 3:1 for large text).
   - Ensure touch targets remain at least 44x44px (or 48x48px where applicable).
5. **Summarize Refactoring**:
   - Provide a concise summary of spacing, color, and hierarchy adjustments made, noting any architectural trade-offs.

---

## Decision Framework

Before adding, modifying, or retaining any visual element, apply these four tests:

- **The Space Test**: Does this element justify occupying visual real estate? If removing it leaves the message intact, remove it.
- **The Color Test**: Does this element require a distinct color? Ensure it fits the 60 / 30 / 10 ratio and does not compete with the accent color.
- **The Hierarchy Test**: Does this element clarify what to focus on next? If it creates competing focal points, demote its weight, size, or contrast.
- **The Purpose Test**: What specific user goal does this element serve? Decorative elements with no functional purpose must be eliminated.

---

## Safe Editing Rules

- **Do Not Redesign Unrelated Scope**: Restrict modifications strictly to the component, view, or section requested.
- **Do Not Break Semantic HTML**: Never replace semantic tags (`<nav>`, `<main>`, `<button>`, `<h1-h6>`) with generic `<div>` tags for layout convenience.
- **Do Not Prioritize Symmetry over Usability**: Asymmetry is natural when guiding eye movement toward a primary call to action.
- **Do Not Introduce Custom CSS Frameworks**: Adapt strictly to the styling paradigm present in the host repository (vanilla CSS, Tailwind, CSS Modules, styled-components, etc.).

---

## Reference Map

Consult supporting references based on task requirements:

- **Conceptual foundation & color balance**: Read [references/visual-principles.md](references/visual-principles.md)
- **Spacing scales, padding, margins, & grids**: Read [references/spacing-and-proportion.md](references/spacing-and-proportion.md)
- **Type scales, line lengths, & readability**: Read [references/typography-hierarchy.md](references/typography-hierarchy.md)
- **Common component & page structures**: Read [references/layout-patterns.md](references/layout-patterns.md)

---

## Completion Criteria

A review or implementation is complete only when:

- [ ] Whitespace feels intentional and sections have distinct breathing room.
- [ ] Color distribution adheres to the 60 / 30 / 10 ratio without competing accents.
- [ ] A user can identify the primary action/focal point within 2 seconds.
- [ ] Unnecessary cards, borders, shadows, and icons have been eliminated.
- [ ] Text lines maintain comfortable reading lengths (45–75 characters per line).
- [ ] Layout degrades gracefully on narrow viewports without clipping or cramped padding.

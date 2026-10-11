# UI Visual Balance (`ui-visual-balance`)

[![Agent Skills Specification](https://img.shields.io/badge/Agent%20Skills-Compatible-blue.svg)](https://agentskills.io/specification)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A portable, framework-agnostic Agent Skill for AI coding assistants and autonomous agents. It enforces visual balance, intentional whitespace, the **60 / 30 / 10 color rule**, clear typography scales, and clutter reduction across web and application interfaces.

Designed for seamless integration with AI coding tools such as **Claude Code**, **Gemini CLI**, **Cursor**, **Windsurf**, and any agent platform supporting the open [Agent Skills](https://agentskills.io) specification.

---

## Overview

When generating or editing UI code, AI agents often clutter interfaces: adding unnecessary containers, excessive badges, multiple competing buttons, and inconsistent padding.

`ui-visual-balance` equips AI agents with a disciplined design decision framework:

* **Whitespace as an Active Element**: Prohibits filling empty space simply because canvas is available.
* **60 / 30 / 10 Color Distribution**: Enforces 60% dominant canvas (Primary), 30% structural surfaces (Secondary), and 10% scarce focal points (Accent).
* **Strict Visual Hierarchy**: Ensures users immediately recognize the primary action within 2 seconds.
* **Safe Implementation**: Inspects existing design tokens and code conventions before making surgical, non-destructive improvements.

---

## Installation

Install directly into your project using the standard `skills` CLI:

```bash
npx skills add irfangani/ui-skills --skill ui-visual-balance
```


---

## Platform Setup & Compatibility

### Claude Code & Open Agent Frameworks

Install via CLI as shown above. The skill will reside in your local `.agent/skills/` or `.skills/` directory, and your agent will discover it automatically.

### Cursor / Windsurf

1. Run the installation command or copy `skills/ui-visual-balance/SKILL.md` into your `.cursor/rules/` directory (e.g., `.cursor/rules/ui-visual-balance.mdc`).
2. Add the following rule instruction:

   ```text
   Always apply the guidelines in skills/ui-visual-balance/SKILL.md when reviewing or generating UI components, templates, and styles.
   ```

### GitHub Copilot

Reference the skill in your `.github/copilot-instructions.md`:

```markdown
Follow the design guidelines and review checklist in skills/ui-visual-balance/SKILL.md whenever generating, auditing, or refactoring user interfaces.
```

---

## How to Use

Once installed, invoke the skill through natural conversation in your agent tool:

### Mode A: Visual Audit

Ask your agent to evaluate an existing layout:

* *"Audit this dashboard screen against ui-visual-balance principles."*
* *"Review this modal component for visual hierarchy and clutter."*
* *"Perform a spatial review on this marketing landing page template."*

### Mode B: Visual Implementation & Refactoring

Ask your agent to improve code directly:

* *"Refactor this card component to reduce visual clutter and align with the 60/30/10 color rule."*
* *"Fix the spacing and typography hierarchy in this pricing table without changing the underlying logic."*
* *"Improve the visual balance of this form using our project's existing design tokens."*

---

## Repository Structure

```text
ui-skills/
├── skills/
│   └── ui-visual-balance/
│       ├── SKILL.md                          # Executable entry point for agents
│       └── references/
│           ├── visual-principles.md          # Visual weight, 60/30/10 color, & clutter
│           ├── spacing-and-proportion.md     # Spacing scales, margins, & padding rules
│           ├── typography-hierarchy.md       # Type scale, measure, & readability
│           └── layout-patterns.md            # Component blueprints (cards, nav, forms)
├── README.md                                 # Public documentation
├── LICENSE                                   # MIT License
└── CONTRIBUTING.md                           # Guidelines for contributors
```

---

## Core Framework at a Glance

| Pillar | Core Mandate | Primary Outcome |
| :--- | :--- | :--- |
| **Space** | *Do not fill every available space.* | Interfaces feel breathable, calm, and structured. |
| **Color** | *60% Primary, 30% Secondary, 10% Accent.* | Scarcity drives focus; eliminates rainbow palettes. |
| **Hierarchy** | *Establish clear focal anchors.* | 2-second scannability from primary to tertiary elements. |
| **Simplicity** | *Less, but intentional.* | Elimination of unnecessary borders, shadows, and cards. |

---

## Contributing

We welcome community contributions, pattern additions, and guideline refinements. Please review [CONTRIBUTING.md](CONTRIBUTING.md) for details on formatting, testing, and Agent Skills specification adherence.

---

## License

This project is licensed under the terms of the MIT License. See [LICENSE](LICENSE) for details.

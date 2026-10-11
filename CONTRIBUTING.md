# Contributing to UI Visual Balance

Thank you for your interest in improving `ui-visual-balance`. This project follows the open [Agent Skills specification](https://agentskills.io/specification).

---

## Principles for Contributions

When submitting changes or new references, ensure your contributions adhere to these requirements:

1. **Agent Skills Specification Compliance**:
   - The primary entry point must remain `skills/ui-visual-balance/SKILL.md`.
   - YAML frontmatter must strictly include valid `name` and `description` fields.
   - Skill names and directories must use lowercase kebab-case (`ui-visual-balance`).
2. **Progressive Disclosure**:
   - Keep `SKILL.md` concise, actionable, and operational.
   - Place extensive explanations, component blueprints, and deep dives inside `references/`.
   - Do not bloat `SKILL.md` with multi-page narrative explanations.
3. **Framework Agnosticism**:
   - Do not introduce framework-locked dependencies (e.g., hardcoded CSS/Tailwind setups or library-specific primitives).
   - Guidelines must remain universal and applicable across web, native mobile, and design mockups.
4. **Link Integrity**:
   - All internal document links must use relative paths (e.g., `references/visual-principles.md`).
   - Verify that no relative links are broken before submitting.

---

## Pull Request Process

1. Fork the repository and create your feature branch:

   ```bash
   git checkout -b feature/refine-spacing-guidelines
   ```

2. Commit your changes with clear, descriptive commit messages.
3. Verify that all markdown formatting renders cleanly.
4. Submit a Pull Request targeting the `main` branch with an explanation of your improvements.

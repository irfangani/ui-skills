## Summary of Changes

* **Skill Name**: `skills/<skill-name>`
* **Description**: Brief explanation of the addition or refinement made.

---

## Agent Skills Specification Checklist

Before submitting this PR, verify that your changes adhere to the repository standards:

- [ ] **Entry Point**: Primary entry point is located at `skills/<skill-name>/SKILL.md`.
- [ ] **Frontmatter**: YAML frontmatter contains valid `name` (lowercase kebab-case matching folder) and concise `description`.
- [ ] **Progressive Disclosure**: `SKILL.md` is focused and operational. In-depth explanations and blueprints are placed in `references/`.
- [ ] **Framework Agnostic**: Guidelines remain universal (no framework-locked CSS dependencies or platform-specific hacks).
- [ ] **Link Integrity**: All internal relative links are valid and resolve correctly.
- [ ] **No Secrets or Binary Clutter**: No unwanted OS files (`.DS_Store`) or lockfiles included.

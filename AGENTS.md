# Shared project instructions

The canonical project rules live in `.cursor/rules/`, relative to the repository
root. This file is an adapter; keep project standards in the shared rulebook.

Before investigating or modifying the project:

1. Read `.cursor/rules/project-context.mdc` completely.
2. Inspect the frontmatter of every `.cursor/rules/*.mdc` file.
3. Read each rule completely when `alwaysApply` is true, its `globs` match a
   relevant file, or its description applies to the task. Before editing another
   area, load any additional applicable rules.
4. Check for nested `AGENTS.md` or `AGENTS.override.md` files governing the files
   you will work on, and read documentation required by the applicable rules.

Apply the shared rules within the tool's instruction hierarchy. When a material
conflict cannot be resolved from instruction priority or explicit scope, identify
it before proceeding with the affected work. Treat unfilled template fields as
missing information, not project requirements.

When a lasting project convention changes, update its owning rule rather than
copying it into this adapter or another agent entry point.

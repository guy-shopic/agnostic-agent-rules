# Shared agent rules starter

One rulebook under `.cursor/rules/`, with entry points for Codex and Claude.
The files contain no project-specific stack, source paths, or absolute paths.

## Install in another repository

1. Copy this folder's `AGENTS.md`, `CLAUDE.md`, and **hidden `.cursor/` directory**
   into the destination repository root. Merge existing entry points rather
   than overwriting their instructions.
2. Fill in `.cursor/rules/project-context.mdc`. Replace or remove every
   `<PLACEHOLDER>` and delete sections that do not apply. This is the only
   required project-specific file.
3. For additional rules, copy `templates/scoped-rule.mdc.template` into
   `.cursor/rules/<topic>.mdc`, then fill in its description, globs, and content.
   The template itself is not an active rule and need not be copied to the
   destination repository.
4. Start a new session in each tool and ask it to identify the shared rulebook
   and the rules applicable to a representative source file. Check its answer
   against the files you installed.

## Files

| File | Purpose |
| --- | --- |
| `AGENTS.md` | Codex entry point and explicit rule-loading protocol |
| `CLAUDE.md` | Claude entry point pointing to `AGENTS.md` |
| `.cursor/rules/project-context.mdc` | Always-on project context template and shared loading protocol for Cursor |
| `.cursor/rules/rule-authoring.mdc` | Portable guidance for maintaining the shared rulebook |
| `templates/scoped-rule.mdc.template` | Optional starter for an area-specific rule |

Cursor uses its native `.mdc` rules. Codex and Claude follow the same files
through their entry points. This is instruction-based sharing, not a plugin,
permission system, or guarantee that every agent will follow every instruction.

Keep standards in `.cursor/rules/`; the entry points only explain how to load
them. Keep task recipes in skills rather than duplicating standing rules there.
Skill installation and discovery depend on the tool and are outside this kit.

Rovo configuration is not included: the original setup maintains a separate
review-oriented copy of its rules. It is not part of the single-source loading
mechanism used here.

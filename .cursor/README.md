# Portable rules extracted from ShopWatch Portal

These are adapted copies, not verbatim copies. Every original rule contained
project-specific assumptions. The files below retain only guidance that can be
used without choosing a framework, language, directory layout, or cloud service.
No source repository rules were modified.

## Review of every source rule

| Source rule | Result |
| --- | --- |
| `agent-rules-and-skills.mdc` | Adapted: shared ownership, frontmatter, scoped loading, maintenance, and skills. Removed project-specific directories, examples, and mandatory Rovo setup. |
| `architecture-boundaries.mdc` | Excluded: application layers, storage ownership, write restrictions, caching, and deployment boundaries are specific architectural decisions. |
| `backend.mdc` | Excluded: chosen Python stack, framework, auth, settings, layers, and logging conventions. |
| `data-pipelines.mdc` | Excluded: particular cloud sources, importer layout, scheduling, and delivery contracts. |
| `database-migrations.mdc` | Excluded: particular database, ORM, migration tooling, and release workflow. |
| `deployment-tenancy.mdc` | Excluded: particular deployment model, CI, images, tenancy, runtime configuration, and CSP locations. |
| `documentation.mdc` | Adapted: canonical ownership, discoverability, links, privacy, and keeping docs current. Removed prescribed paths and registries. |
| `frontend.mdc` | Excluded: chosen frameworks, components, routing, data fetching, auth, localization, and configuration model. |
| `project-context.mdc` | Excluded: entirely project-specific context. Fill in a project-context template in each destination repository. |
| `rovo-maintenance.mdc` | Excluded: requires a particular review integration and mirrored-file arrangement. The general conditional synchronization principle is in `agent-rules-and-skills.mdc`. |
| `sensitive-logging.mdc` | Adapted: safe metadata and excluding secrets and private identifiers. Removed specific payload types, logging helpers, and claims about the logging pipeline. |
| `style-guide.mdc` | Adapted: following established conventions, focused edits, and sparse comments. Removed language-specific preferences and tool choices. |
| `testing-standards.mdc` | Excluded: specific test structure, mocking choices, tooling prohibitions, and CI commands. |
| `tooling-and-dependencies.mdc` | Adapted: reuse the stack, regenerate lockfiles, preserve checks, and respect scripting conventions. Removed package-manager and infrastructure choices. |

## Use with the sharing setup

Keep these files under `.cursor/rules/`. The destination's `AGENTS.md` and
`CLAUDE.md` provide loading instructions. These files supplement, rather than
replace, the destination's project context and area-specific rules.

The adapters expect `.cursor/rules/project-context.mdc`. Supply that file using
the project-context template before treating the setup as complete. These
portable rules intentionally do not supply project facts or validation commands.

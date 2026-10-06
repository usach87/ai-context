# AI Agent Instructions

<!-- Keep this file small: a map and global constraints, not a project manual. -->

## Project Overview

[Describe the project and its main responsibility in 2–5 sentences.]

## Project Map

- `[path]` — [responsibility]
- `[path]` — [responsibility]
- `[path]` — [responsibility]

More detail: `docs/project-map.md`.

## Common Commands

- Install: `[command]`
- Development: `[command]`
- Test: `[command]`
- Lint: `[command]`
- Typecheck/static analysis: `[command]`
- Build: `[command]`

Delete commands that do not apply.

## Context Navigation

Load detailed context only when relevant:

- Architecture → `docs/architecture.md`
- Repository map → `docs/project-map.md`
- Common workflows → `docs/workflows.md`
- Repeating task-specific instructions → `skills/`

If a domain/service has its own `AGENTS.md`, read it only when working in that area.

Do not load unrelated documentation preemptively.

## Working Rules

1. Start with the smallest relevant repository area.
2. Search before reading large files.
3. Prefer existing project patterns over inventing new ones.
4. Use golden/reference implementations when available.
5. Expand exploration only when evidence requires it.
6. Make the smallest coherent change that solves the task.
7. Validate with the smallest relevant check first.
8. Do not modify unrelated code.
9. Do not add dependencies unless required and allowed.
10. Treat generated/vendor files as read-only unless explicitly instructed otherwise.

## Golden Examples

| Task | Reference |
|---|---|
| [common task] | `[path]` |
| [common task] | `[path]` |
| [common task] | `[path]` |

## Important Constraints

- [constraint]
- [constraint]

Keep only constraints that materially affect implementation.

## Knowledge Capture

When significant exploration reveals stable, non-obvious knowledge, preserve it in the smallest appropriate place:

- global fact → this file, only if useful for most tasks;
- domain/service fact → local instructions or focused documentation;
- recurring workflow → `skills/`;
- architecture flow → `docs/architecture.md`;
- preferred implementation → golden example.

Do not document temporary debugging details or obvious code behavior.

## Context Hygiene

Remove or update obsolete architecture, completed migration instructions, dead paths, deprecated commands, duplicated rules, expired workarounds, and stale reference implementations.

Ask:

> Will this information change how an agent should perform a task today?

If not, it probably should not be active AI context.

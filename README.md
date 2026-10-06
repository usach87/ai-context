# AI Context

> Give AI less context. Give it better context.

A lightweight, tool-agnostic template for organizing codebases so AI coding agents can find the **minimum context required for a task**.

It is intentionally small and does not prescribe a language, framework, architecture, or AI vendor. Adapt it to frontend, backend, mobile, data, infrastructure, microservices, or monorepos.

## Five principles

1. **Minimize Permanent Context** — keep global instructions small.
2. **Progressive Context** — load project → domain/service → task → example → source.
3. **Reduce Exploration** — provide maps, entry points, and golden examples.
4. **Reuse Knowledge** — turn expensive discovery into reusable knowledge.
5. **Keep Context Clean** — remove obsolete, duplicated, and misleading context.

## Quick start

Copy into your repository:

```text
AGENTS.md
docs/
skills/
# optional
AI_CONTEXT_CHECKLIST.md
```

Then:

1. Replace `[placeholders]`.
2. Delete sections that do not apply.
3. Keep `AGENTS.md` short.
4. Fill `docs/project-map.md`.
5. Add 2–5 real golden examples.
6. Add local `AGENTS.md` files only where additional rules are useful.
7. Create skills only for recurring workflows.
8. Review `AI_CONTEXT_CHECKLIST.md`.

## Suggested structure

```text
your-project/
├── AGENTS.md
├── AI_CONTEXT_CHECKLIST.md
├── docs/
│   ├── architecture.md
│   ├── project-map.md
│   └── workflows.md
├── skills/
│   ├── README.md
│   └── example-task/
│       └── SKILL.md
└── ...
```

## Context loading model

```text
Task
  ↓
Minimal global context
  ↓
Relevant domain / service context
  ↓
Task-specific instructions
  ↓
Golden example
  ↓
Targeted search
  ↓
Minimum relevant source
  ↓
Change + targeted validation
```

Do not automatically load every file in `docs/` or `skills/`. These files exist to make relevant context easier to find, not to create a larger permanent prompt.

## Golden examples

A golden example is an existing implementation that represents the preferred project pattern.

| Task | Possible reference |
|---|---|
| API operation | `services/users/handlers/create-user/` |
| Database migration | `database/migrations/...` |
| Background job | `workers/example-job/` |
| Message consumer | `services/orders/consumers/example/` |
| UI feature | `apps/web/features/example/` |
| Infrastructure module | `infrastructure/services/example/` |

Prefer a real, maintained implementation over a long prose description when it communicates the pattern better.

## Knowledge capture

If an agent has to inspect many files to discover a stable architectural fact, consider documenting the result.

Good candidates include cross-service flows, non-obvious boundaries, recurring workflows, important entry points, and project-specific constraints.

Do not capture temporary debugging findings, obvious implementation details, duplicated canonical information, or speculation.

## Tool compatibility

`AGENTS.md` is the canonical template file here. If a tool expects another filename or format, adapt or generate that tool-specific entry point from the same source instead of maintaining conflicting copies.

## License

MIT. See `LICENSE`.

# Architecture

> Read only when the task requires cross-module, cross-service, data-flow, or system-level understanding.

Keep this focused on stable architecture, boundaries, and non-obvious flows.

## System Overview

[Brief description.]

## Main Components

| Component | Responsibility | Path |
|---|---|---|
| [component] | [responsibility] | `[path]` |
| [component] | [responsibility] | `[path]` |

## Important Flows

### [Flow name]

```text
[entry point]
    ↓
[component/service]
    ↓
[queue/storage/external API]
    ↓
[result/consumer]
```

**Relevant code**
- `[path]`
- `[path]`

**Important constraints**
- [constraint]

## Boundaries

- [Which component owns what?]
- [What must not be coupled directly?]
- [Where are contracts defined?]

## External Systems

| System | Purpose | Integration location |
|---|---|---|
| [system] | [purpose] | `[path]` |

## Architecture Decisions That Affect Current Work

Include only decisions that still constrain implementation today.

- [decision] — [current consequence]

Historical decisions belong in separate historical/ADR documentation, not active agent context.

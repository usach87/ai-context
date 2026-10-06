# Common Workflows

> Keep only recurring workflows. Move complex project-specific workflows into `skills/`.

## Adding or Changing a Feature

1. Identify the owning domain/service/application.
2. Read local instructions if they exist.
3. Find the closest maintained golden example.
4. Search for affected contracts and callers.
5. Implement the smallest coherent change.
6. Run targeted validation.
7. Expand validation only when justified.
8. Capture stable new knowledge if significant discovery was necessary.

Reference: `[path]`

## Adding an API Operation

Delete if not applicable.

1. Locate the owning API/module/service.
2. Follow the existing handler/routing pattern.
3. Reuse canonical validation/error/auth patterns.
4. Check affected contracts and clients.
5. Add focused tests.

Golden example: `[path]`

## Adding a Database Migration

Delete if not applicable.

1. Confirm the owning schema/database.
2. Follow migration naming and transaction rules.
3. Check compatibility requirements.
4. Update schema/model definitions when required.
5. Run the smallest relevant checks.

Golden example: `[path]`

## Adding an Event / Message Consumer

Delete if not applicable.

1. Locate the event contract.
2. Find the closest existing consumer.
3. Follow retry/idempotency/error-handling conventions.
4. Verify producer/consumer compatibility.
5. Add focused tests and observability where required.

Golden example: `[path]`

## Changing Infrastructure

Delete if not applicable.

1. Locate the owning infrastructure module.
2. Find a comparable deployed resource.
3. Avoid unrelated formatting/generated changes.
4. Validate configuration locally where possible.
5. Review the diff before broader checks.

Golden example: `[path]`

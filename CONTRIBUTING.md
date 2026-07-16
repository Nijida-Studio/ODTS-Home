# Contributing with ODTS

ODTS uses an issue-first, documentation- and test-first development workflow.

## Before implementation

1. Create or select a Task with exactly one Parent Item.
2. Confirm the Parent Item belongs to exactly one Epic.
3. Set the native ODTS subtype field and any optional planning fields used by the team.
4. Create the code skeleton: files, types, interfaces, signatures, and placeholders.
5. Add rudimentary documentation describing purpose, intended behavior, and relevant constraints.
6. Add tests for the intended behavior where technically possible. If this is not possible, document the reason and alternative validation.
7. Review this foundation before completing the implementation logic.

## During implementation

Keep the Task, code documentation, and tests synchronized with changes in behavior or design. Create a ToDo Task for meaningful deferred work instead of leaving it only in a source comment.

## Completion

A Task is complete when its result is implemented, its documentation is accurate, tests exist where possible, exceptions are explained, deferred work is tracked, and the required review has been completed.

See the human-readable [ODTS documentation snapshot](SPECIFICATION.md) for guidance. The authoritative current behavior is defined by [ODTS-Specification](https://github.com/Nijida-Studio/ODTS-Specification).

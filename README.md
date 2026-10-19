# The `aivara-se` template

The entry file every repository in this organisation adopts: the rules that are the same everywhere, and nothing that moves with the work.

## What is here

`AGENTS.md` is the donor entry file. A repository copies it to its root and fills its slots; it is the only copy of the convention, and it is adopted, never forked.

## What it deliberately leaves out

The state of the work, the shape of the system and the shape of the code belong to `PRODUCT.md`, `SYSTEMS.md` and `DESIGN.md` in the repository that has them. The entry file points at those documents and never repeats them, so adopting it is a one-time act and a change to the work never touches it.

## Adopting it

1. Copy `AGENTS.md` to the repository root. If one is already there, merge: keep its house rules, its check command, its check notes and its review targets, and take the rest from here.
2. Fill every `{{UPPER_SNAKE_CASE}}` slot: `{{REPO_PURPOSE}}`, `{{REPO_HOUSE_RULES}}`, `{{REPO_CHECK_COMMAND}}`, `{{REPO_CHECK_NOTES}}`, `{{DEFAULT_BRANCH}}`, `{{REVIEW_REQUEST_TARGETS}}`. No slot survives; an unfilled slot means the adoption is unfinished.
3. Move what the old entry file said about the current state or focus into `PRODUCT.md`, and what it said about serving, building and checking into `SYSTEMS.md`.
4. Delete any map of the tree the old file carried. A fact has one home, and a map that lists files goes stale with the next commit.

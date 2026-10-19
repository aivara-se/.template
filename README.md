# The `aivara-se` template

The entry file every repository in this organisation adopts: the rules that are the same everywhere, and nothing that moves with the work.

## Adopting it

1. Copy `AGENTS.md` to the repository root. If one is already there, merge: keep its house rules, check command, check notes and review targets, and take the rest from here.
2. Fill the six slots — `{{REPO_PURPOSE}}`, `{{REPO_HOUSE_RULES}}`, `{{REPO_CHECK_COMMAND}}`, `{{REPO_CHECK_NOTES}}`, `{{DEFAULT_BRANCH}}`, `{{REVIEW_REQUEST_TARGETS}}`. An unfilled slot means the adoption is unfinished.
3. Move what the old file said about the current state or focus into `PRODUCT.md`, and what it said about serving and checking into `SYSTEMS.md`.
4. Drop any map of the tree. It goes stale with the next commit.

The state of the work is `PRODUCT.md`'s, the shape of the system `SYSTEMS.md`'s. The entry file points at them and never repeats them, which is why adopting it is a one-time act.

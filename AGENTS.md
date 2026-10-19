# Agent Instructions

{{REPO_PURPOSE}}

This file is the `aivara-se` agent convention: the rules that are the same in every repository. Adopt it, do not fork it. What changes — the state of the work, the shape of the system — has a document of its own, named below, so this file changes only when the convention itself does.

## Where a fact lives

- `PRODUCT.md` — what the product is, who it serves, what it must not do, what the work is on now, and what would make it done.
- `SYSTEMS.md` — how it is served, built and checked, and the mechanisms a product promise leans on.
- `DESIGN.md` — the interface and the values it fixes, where the repository has a face.
- `docs/adrs/` — a decision per file, where the repository records one; a choice that is expensive to reverse is written down before the code that depends on it lands.
- `README.md` — how to run it locally.

A document is the only copy of what it says: link to it, never restate it. Nothing in this file describes the current state of the work. When the state changes, `PRODUCT.md` changes, and this file stays as it is.

## House rules

{{REPO_HOUSE_RULES}}

## Tooling

- **Bun is the runtime for scripts.** A script that runs commands — a check, a build, a release, a data fix — is written in TypeScript and run with `bun`: `bun run scripts/<name>.ts`. **Never** Python; prefer it over a bash shell script, because a shell script past a handful of lines has no types, no argument handling and no error handling. A one-line command typed at the prompt is not a script.
- **Never** add a second package manager, a second lockfile, a second formatter or a second test runner. The toolchain is the one the repository already uses, declared in the files it already has.
- **Never** report "tests pass", "it builds" or "verified" without the command and the tree it ran against.

## Skills

The organisation's skills are read from the `skills/` directory of the `aivara-se/.agents` checkout, once, for every agent; a repository carries no copy of them. Each is a procedure for one kind of work and declares its `when-to-use`: open the one that covers the work before starting it.

## Verify before pushing

```bash
{{REPO_CHECK_COMMAND}}
```

Run the whole sequence, not just its fast part, and read every result — the exit code of the last command says nothing about the first.

{{REPO_CHECK_NOTES}}

## Version Control

- **Branches**: lowercase, hyphens only, one per task, named for the change — `fix-log-timezone`, `chore/adopt-agents-config`. No uppercase, no underscores, no personal prefixes.
- **Commits**: Conventional Commits, lowercase, single line, no scopes — `type: short description`.
- **Never** commit to `{{DEFAULT_BRANCH}}` directly. **Never** force-push a branch another agent or person has seen.
- Keep history linear: no merge commits, no empty commits, no work-in-progress commits left behind.
- Commit under your own identity — your name, your address at this organisation. Never a generic agent, never another agent's identity.
- Remote work is always a branch plus a pull request. The pull request body says what changed, what was verified and how, and what was left out; request review from {{REVIEW_REQUEST_TARGETS}}. Leave the working tree clean: no scratch files, no editor backups, no `.env` you created.

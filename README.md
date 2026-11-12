# The `aivara-se` template

The files a new repository starts from. The entry file is not written here: it is `aivara-se/.github/docs/ENTRY.md`, and this repository carries the copy.

## Adopting it

1. Copy `AGENTS.md` to the repository root. It is the standard, byte for byte: do not edit it, and do not fill anything in.
2. Align the repository with the baseline in `.github/docs/SETTINGS.md`: rebase-only merges, auto-merge and delete-branch on, wiki and projects off, and the `Baseline` ruleset on the default branch.
3. Add the workflow with the first code, not at adoption. Copy `.prettierrc.json` and `.github/workflows/validate.yml`, then replace the placeholder step with the repository's gate. Put `bun fmt --no-script --check .` in that gate as well: nothing else in the copied workflow checks formatting. The job stays named `validate`, the required check: a placeholder left in place satisfies that check while checking nothing.
4. Keep the `agents` job. It has no inputs, and it fails when the copy differs from the standard.
5. What the repository is goes in `PRODUCT.md`; how it is built and checked in `SYSTEMS.md`. A rule that must differ per repository is `SYSTEMS.md`'s, so the entry file needs no edit. Decisions go in `docs/adrs/`, one file each; `000` arrives with this template and keeps its text.

A copy that differs fails the `agents` job. Change a rule in `aivara-se/.github/docs/ENTRY.md`, and every repository follows at its next merge.

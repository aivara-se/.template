# The `aivara-se` template

The files a new repository starts from. It is deliberately small: if a line does not prevent a collision or settle a decision, cut it.

## Adopting it

1. Keep the `AGENTS.md` file. It is the standard, byte for byte: do not edit it.
2. Align the repository settings with the baseline in `.github/docs/SETTINGS.md`.
3. Keep the `agents`, `docs` and `config` jobs in `.github/workflows/validate.yml`, and add the repository's own checks to the `validate` job.

A copy that differs fails the `agents` job. Change a rule in `aivara-se/.github/AGENTS.md`, and every repository follows at its next merge.

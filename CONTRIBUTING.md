# Contributing

Thank you for considering a contribution to Open Civic Data.

## Opening an issue

- Search the existing issues first.
- For a bug in the tooling, include the command you ran, the input file (or a minimal fictional version of it) and the output you got.
- For a schema change, describe the use case, the publisher or reuser it serves, and which existing standards (OCDS, Popolo, schema.org, Frictionless Data) you checked for an equivalent concept.

## Proposing a pull request

1. Open or comment on an issue before starting larger work, so the scope can be agreed first.
2. Create a branch from `main` and keep each pull request focused on one change.
3. Add or update tests and fixtures for every schema or code change.
4. Reference the issue in the pull request description (for example, `Closes #12`).
5. Do not commit real personal data. Example data must be fictional and marked as such.

## Architecture decisions

Structural decisions (schema versioning, identifiers, reuse of external standards, breaking changes, tooling choices) are recorded as Architecture Decision Records in `docs/adr/`, one decision per file, named `NNNN-short-title.md`, using the context / decision / status / consequences format.

## Code of Conduct

This project follows the UnitedOpen-Source [Code of Conduct](https://unitedopensource.org/code-of-conduct). By participating you agree to uphold it.

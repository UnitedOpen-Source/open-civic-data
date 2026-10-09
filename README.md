# Open Civic Data

Interoperable schemas for civic and public-interest information.

> **Note:** This project is not affiliated with the Open Civic Data project started by the Sunlight Foundation ([github.com/opencivicdata](https://github.com/opencivicdata), [documentation](https://open-civic-data.readthedocs.io/en/latest/)), which defines Open Civic Data Division Identifiers (OCD-IDs). Whether and how this project reuses OCD-IDs is an open decision tracked in the issue tracker.

## Why

Public-interest information such as the services a government offers, how it plans and spends its budget, and which bodies and office holders are responsible for what is usually published in formats that differ from one publisher to the next. Each reuser ends up writing a one-off parser, and comparing two cities or two agencies means reconciling their structures by hand.

Good standards already exist for parts of this problem: the [Open Contracting Data Standard](https://standard.open-contracting.org/latest/en/) for procurement, [Popolo](https://www.popoloproject.com/) for people, organizations and memberships, [schema.org GovernmentService](https://schema.org/GovernmentService) for describing services on the web, and the [Frictionless Data Package and Table Schema](https://datapackage.org/standard/table-schema/) specifications for tabular data. What is missing is a small, versioned, machine-checkable profile that ties them together for common civic datasets and comes with tooling that validates real files.

## What it is

- A set of [JSON Schema](https://json-schema.org/) documents and Frictionless Data Package profiles for a few civic domains, starting with a public service catalog, budget and expenditure, and public bodies and mandates.
- A profile that references existing standards instead of duplicating them: where Popolo, OCDS or schema.org already defines a concept, the schema points to it and maps to it.
- A Python command-line tool, `ocd`, intended to validate files against the schemas and convert CSV to JSON using Table Schema.
- Documentation for each schema, with fictional example datasets clearly marked as examples.

## What it is not

- Not a replacement for OCDS, Popolo, schema.org or Frictionless Data. If a concept is covered there, this project defers to it.
- Not a data portal, a hosted API or a dataset collection. It defines formats and tools; publishers keep their own data.
- Not tied to a single country's legal or administrative model. Country-specific fields belong in extensions, not in the core schemas.

## Planned scope for v0.1.0

The v0.1.0 milestone is meant to deliver a first usable schema and the tooling around it:

- Repository scaffolding with uv, ruff, pytest and CI.
- An ADR on schema versioning and governance (semantic versioning and a change process).
- An ADR on reusing OCD-IDs, Popolo and OCDS rather than reinventing identifiers and models.
- A first "public service" schema aligned with schema.org GovernmentService.
- The `ocd validate` command.
- A CSV to JSON converter driven by Table Schema.
- Fictional example datasets, labelled as examples.
- Reference documentation for each schema.
- Translated field labels in English, Brazilian Portuguese and Spanish.

## Principles

1. **Reuse before invention.** A new field or identifier is added only after checking that OCDS, Popolo, schema.org, Frictionless Data or OCD-IDs do not already cover it, and the check is recorded in the pull request.
2. **Every schema is testable.** Each schema ships with valid and invalid fixtures that run in CI.
3. **Versioned contracts.** Schemas follow semantic versioning; a breaking change requires a major version and an ADR.
4. **Plain files first.** Schemas, examples and documentation are plain JSON, CSV and Markdown that work without this project's tooling.
5. **Language-neutral data, translated labels.** Field names are stable English identifiers; human-readable labels and descriptions are translated separately.

## Getting involved

Look for issues labelled [`good first issue`](https://github.com/UnitedOpen-Source/open-civic-data/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22) and read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## License

[MIT](LICENSE)

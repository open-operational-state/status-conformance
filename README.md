# Status Conformance

Conformance definitions, fixtures, test taxonomy, and compatibility validation for the [Open Operational State](https://github.com/open-operational-state) standard.

## Overview

Conformance is a strategic asset, not an afterthought. This repository defines how implementations demonstrate compliance with the standard and how interoperability is validated.

## Contents

| Document / Directory | Purpose |
|---|---|
| [CONFORMANCE.md](CONFORMANCE.md) | Conformance philosophy, levels, and strategy |
| [TAXONOMY.md](TAXONOMY.md) | Fixture classification and test taxonomy |
| [fixtures/](fixtures/) | Test fixtures and sample payloads |
| [adapters/](adapters/) | Foreign format mapping validation |
| [compatibility/](compatibility/) | Compatibility matrices |
| [reports/](reports/) | Validation reports and artifacts |

## Related Repositories

| Repository | Purpose |
|---|---|
| [status-spec](https://github.com/open-operational-state/status-spec) | Technical specification (what conformance validates against) |
| [status-tooling](https://github.com/open-operational-state/status-tooling) | Reference tooling including the validator package |
| [governance](https://github.com/open-operational-state/governance) | Charter, scope, and terminology |

## Licensing

- **Code** (test runners, validators): [Apache 2.0](LICENSE)
- **Documentation-like fixtures** (sample payloads, examples): [CC BY 4.0](LICENSE-CC-BY-4.0)

## Project Rules

See [PROJECT_RULES.md](PROJECT_RULES.md) for repo-specific constraints.

# Adapter Validation

This directory contains validation material for adapters — components that translate native or legacy formats into the core model.

## Purpose

Adapter validation ensures that:

- Foreign format mappings produce correct core model output
- Lossiness is correctly classified and documented
- Adapter behavior is consistent and predictable
- Edge cases in format translation are covered

## What Belongs Here

- **Mapping validation tests** — verify that a given adapter correctly translates a known input to the expected core model output
- **Lossiness documentation** — describe what each adapter can and cannot represent
- **Format samples** — example payloads from real-world systems used as adapter inputs
- **Fidelity reports** — how much information is preserved across the adaptation

## Lossiness Classification

Adapters are classified by fidelity:

| Classification | Description |
|---|---|
| Lossless | All source information maps cleanly to the core model |
| Partially lossy | Some information cannot be represented; losses are documented |
| Heuristic | Mapping relies on inference or pattern matching |
| Inferred | Core model fields are populated from indirect evidence |

## Relationship to Other Repositories

- **[status-spec/spec/adapters.md](https://github.com/open-operational-state/status-spec/blob/main/spec/adapters.md)** defines adapter concepts
- **[status-tooling-js](https://github.com/open-operational-state/status-tooling-js)** implements adapter logic
- **This directory** validates that adapters conform to the specification

## Status

Adapter validation will be populated as adapters are defined and implemented.

# Test Taxonomy

This document defines the classification system for conformance fixtures and test cases.

## Purpose

A consistent taxonomy ensures that:

- Fixtures are organized predictably
- Test coverage can be measured systematically
- Contributors know where new fixtures belong
- Conformance reports can reference specific test categories

## Taxonomy Dimensions

Fixtures and tests are classified along the following dimensions:

### By Layer

Tests are organized by the architectural layer they validate:

| Layer | Directory Pattern | Description |
|---|---|---|
| Core Model | `fixtures/core/` | Core model semantic validation |
| Profiles | `fixtures/profiles/{name}/` | Profile-specific validation |
| Serializations | `fixtures/serializations/{name}/` | Wire format validation |
| Adapters | `adapters/{name}/` | Foreign format mapping validation |
| Discovery | `fixtures/discovery/` | Discovery mechanism validation |
| Capabilities | `fixtures/capabilities/` | Capabilities/negotiation validation |

### By Polarity

- **Positive** — valid inputs that must be accepted and correctly interpreted
- **Negative** — invalid inputs that must be rejected or flagged
- **Edge** — boundary cases that test limits of the specification

### By Fidelity (for Adapters)

- **Lossless** — the adapter can map all information faithfully
- **Partially lossy** — some information is lost or approximated
- **Heuristic** — the mapping relies on inference
- **Inferred** — core model fields are populated from indirect evidence

## Fixture Format

Each fixture should include:

- **Input** — the raw payload or scenario being tested
- **Expected output** — the expected core model representation (for adapters) or validation result
- **Metadata** — layer, polarity, profile, serialization, and any relevant notes
- **License** — whether the fixture is CC BY 4.0 (doc-like) or Apache 2.0 (code-like)

## Status

The taxonomy will be populated with concrete fixtures as the specification matures. This structure is established during scaffolding to prevent ad-hoc organization later.

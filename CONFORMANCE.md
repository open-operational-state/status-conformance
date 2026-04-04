# Conformance

## Philosophy

Conformance is a core ecosystem asset for Open Operational State. It is not an afterthought bolted on after the specification is complete — it is a strategic component that enables trust, interoperability, and quality across implementations.

Conformance results are determined exclusively by the **official test suites and fixtures in this repository**. Third-party interpretations of conformance are not authoritative.

## Why Conformance Matters

Conformance enables:

- **Trust** — consumers can verify that implementations behave as expected
- **Compatibility validation** — interoperability between targets and monitors can be tested
- **Quality control** — implementations have clear criteria to meet
- **Ecosystem credibility** — the standard demonstrates rigor and practical testability
- **Adoption confidence** — implementers know what "done" looks like

## Conformance Levels

Conformance is assessed at three tiers. Each tier builds on the previous one.

### Basic

A target achieves **Basic** conformance when:

- It serves a valid operational-state response in at least one recognized serialization (`application/health+json` or `application/status+json`)
- The response satisfies at least the **Liveness** profile requirements (Subject + Condition)
- The `condition` field uses a value from the appropriate condition vocabulary
- The `profiles` field is present and contains at least one valid profile identifier

### Standard

A target achieves **Standard** conformance when it meets Basic requirements and additionally:

- It satisfies the full requirements of at least one declared profile (all MUST-level concepts present)
- It serves a valid discovery document at `/.well-known/operational-state`
- Field names and structure match the declared serialization specification
- Condition values are valid for all declared profiles
- Timing fields use RFC 3339 format when present

### Extended

A target achieves **Extended** conformance when it meets Standard requirements and additionally:

- It supports multiple profiles (e.g., both Health and Liveness)
- It provides Link header-based discovery (`rel="operational-state"`)
- It serves a discovery document that accurately describes all available resources
- Component and dependency conditions use valid vocabulary values
- Provenance is explicitly declared (not inferred)
- Evidence is present for non-operational conditions (Health profile and above)

## What Conformance Validates

Conformance testing covers:

- **Structural validity** — does the response match the expected serialization format?
- **Semantic correctness** — do the values mean what the spec says they should mean?
- **Profile compliance** — does the implementation satisfy the requirements of a declared profile?
- **Discovery behavior** — can a conformant monitor discover and interpret the resource?
- **Adapter fidelity** — does an adapter produce correct core model output from a given input?

## Relationship to Other Repositories

- **[status-spec](https://github.com/open-operational-state/status-spec)** defines what conformance validates against
- **[status-tooling-js](https://github.com/open-operational-state/status-tooling-js)** will provide the `validator` package that implements conformance checks
- **This repository** defines the conformance model, fixtures, taxonomy, and reports

## Conformance Is Not Certification

Conformance testing provides evidence of compliance. It does not constitute formal certification or endorsement. The conformance framework is a tool for implementers, not a gatekeeping mechanism.

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

Conformance levels will be defined as the specification matures. They are expected to follow a tiered structure:

### Anticipated Tiers

1. **Basic** — minimal viable conformance (e.g., a valid operational-state response in at least one serialization)
2. **Standard** — full compliance with a specific profile and serialization
3. **Extended** — support for discovery, capabilities, and multiple profiles/serializations

Exact tier definitions depend on the specification reaching sufficient maturity. Premature level definitions risk constraining spec evolution.

## What Conformance Validates

Conformance testing covers:

- **Structural validity** — does the response match the expected serialization format?
- **Semantic correctness** — do the values mean what the spec says they should mean?
- **Profile compliance** — does the implementation satisfy the requirements of a declared profile?
- **Discovery behavior** — can a conformant monitor discover and interpret the resource?
- **Adapter fidelity** — does an adapter produce correct core model output from a given input?

## Relationship to Other Repositories

- **[status-spec](https://github.com/open-operational-state/status-spec)** defines what conformance validates against
- **[status-tooling](https://github.com/open-operational-state/status-tooling)** provides the `validator` package that implements conformance checks
- **This repository** defines the conformance model, fixtures, taxonomy, and reports

## Conformance Is Not Certification

Conformance testing provides evidence of compliance. It does not constitute formal certification or endorsement. The conformance framework is a tool for implementers, not a gatekeeping mechanism.

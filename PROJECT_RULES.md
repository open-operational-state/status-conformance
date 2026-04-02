# Status Conformance — Project Rules

This document supplements the [canonical org-wide PROJECT_RULES.md](https://github.com/open-operational-state/.github/blob/main/PROJECT_RULES.md).

---

## Repo-Specific Constraints

- Code in this repository (test runners, validators) is licensed under **Apache 2.0**.
- Documentation-like fixtures are licensed under **CC BY 4.0** (see `LICENSE-CC-BY-4.0`).
- TypeScript is permitted for test runners and validation tooling.
- Conformance definitions must align with the specification in `status-spec` — do not introduce conformance levels that contradict or exceed the spec.
- Adapter validation tests belong in `adapters/`.
- Do not embed vendor-specific logic in conformance tooling.

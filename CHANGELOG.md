# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).


## [0.1.1] — 2026-04-03

### Added
- `fixtures/profiles/health/edge-no-timing.json` — edge case fixture for health profile without timing. Validates as valid with a warning, reflecting real-world endpoints.

## [0.1.0] — 2026-04-02

### Added
- Initial fixture set covering core model validation and profile conformance.
- Positive and negative fixtures for condition values, profiles, and required fields.
- Fixture metadata schema with `_metadata` fields: `description`, `layer`, `profile`, `polarity`, `fidelity`, `license`.
- Test taxonomy documentation.

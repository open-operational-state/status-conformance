# Fixtures

This directory contains test fixtures for conformance validation.

## Organization

Fixtures are organized by architectural layer and further classified by the [test taxonomy](../TAXONOMY.md).

```
fixtures/
├── core/              # Core model validation fixtures
├── profiles/          # Profile-specific fixtures
│   └── {profile}/
├── serializations/    # Wire format fixtures
│   └── {format}/
├── discovery/         # Discovery mechanism fixtures
└── capabilities/      # Capabilities/negotiation fixtures
```

## Fixture Structure

Each fixture should include:

- Input payload or scenario
- Expected output or validation result
- Metadata (layer, polarity, profile, serialization)

See [TAXONOMY.md](../TAXONOMY.md) for classification details.

## Licensing

- Documentation-like fixtures (examples, sample payloads): [CC BY 4.0](../LICENSE-CC-BY-4.0)
- Code-like fixtures (intended for direct use in tests): [Apache 2.0](../LICENSE)

## Status

Fixtures will be created as the specification progresses. This directory is intentionally empty during the scaffolding phase.

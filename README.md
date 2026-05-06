# vector-mesh-clock-hub

`vector-mesh-clock-hub` is a SQL project in distributed systems. Its focus is to implement an SQL distributed systems project for clock policy evaluation, using deny and allow fixtures and explainable decision traces.

## Why It Exists

This is intentionally local and self-contained so it can be inspected without credentials, services, or seeded history.

## Vector Mesh Clock Hub Review Notes

The first comparison I would make is `replica lag` against `quorum health` because it shows where the rule is most opinionated.

## Features

- `fixtures/domain_review.csv` adds cases for quorum health and lease drift.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/vector-mesh-clock-walkthrough.md` walks through the case spread.
- The SQL code includes a review path for `replica lag` and `quorum health`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Architecture Notes

The fixture data drives the tests. The code stays thin, while `metadata/domain-review.json` and `config/review-profile.json` explain what each case is meant to protect.

The SQL checks add a separate view over the domain review fixture.

## Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Tests

The verifier is intentionally local. It should fail if the fixture score math, lane assignment, or language-specific test drifts.

## Limitations And Roadmap

This remains a local project with deterministic fixtures. It does not depend on credentials, hosted services, or live data. Future work should add richer malformed inputs before widening the public API.

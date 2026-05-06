# Review Journal

The repository goal stays the same: implement an SQL distributed systems project for clock policy evaluation, using deny and allow fixtures and explainable decision traces. This note explains the added review angle.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its distributed systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `quorum health`, score 84, lane `hold`
- `stress`: `lease drift`, score 179, lane `ship`
- `edge`: `replica lag`, score 199, lane `ship`
- `recovery`: `membership churn`, score 184, lane `ship`
- `stale`: `quorum health`, score 179, lane `ship`

## Note

The repository should be understandable without pretending it is larger than it is.

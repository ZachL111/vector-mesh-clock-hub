# Vector Mesh Clock Hub Walkthrough

I use this file as a small checklist before changing the SQL implementation.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | quorum health | 84 | hold |
| stress | lease drift | 179 | ship |
| edge | replica lag | 199 | ship |
| recovery | membership churn | 184 | ship |
| stale | quorum health | 179 | ship |

Start with `edge` and `baseline`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

The next useful expansion would be a malformed fixture around lease drift and membership churn.

# Vector Mesh Clock Hub Failure Table

| Case | Focus | Expected Lane |
| --- | --- | --- |
| g001 | quorum health | hold |
| g002 | lease drift | ship |
| g003 | replica lag | hold |
| g004 | membership churn | ship |
| g005 | quorum health | hold |
| g006 | lease drift | watch |
| g007 | replica lag | ship |
| g008 | membership churn | hold |
| g009 | quorum health | watch |
| g010 | lease drift | watch |
| g011 | replica lag | watch |
| g012 | membership churn | ship |

Use this table when a verifier failure is hard to read from the raw CSV.

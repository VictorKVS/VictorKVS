# Repository Classification — Batch 03

Cutoff policy: repositories older than the active 3-day window may be reviewed, but inactivity alone never authorizes destructive changes.

| Repository | Last push observed | Evidence | Classification | Action |
|---|---:|---|---|---|
| `MVP` | 2025-11-28 | Python implementation tree for gateway/router/security/observability plus protocol/policy docs; current branch has broken imports/entrypoint and skeleton tests | `SHOWCASE` / `PROTOTYPE` | Keep public; expose evidence-gated Universal Agent page; do not claim verified MVP yet |
| `mq-diploma` | 2025-03-31 | Fork of `netology-code/mq-diploma` | `LEARNING` | Preserve as learning history; remove from visual foreground later |
| `html-homeworks` | 2021-08-25 | Fork; repository description explicitly identifies HTML course homework | `LEARNING` | Preserve as learning history; remove from visual foreground later |

## Notes

### Universal Agent / `MVP`
This repository is not a merge/archive target. It contains meaningful architecture and implementation evidence and should remain in the product layer while its reproducibility gaps are repaired. Its public maturity label is deliberately below MVP until the evidence gate passes.

### Learning forks
`mq-diploma` and `html-homeworks` are useful progression evidence but should not compete visually with current product/knowledge engineering. No deletion or archive mutation was performed in this batch.

## Protected exclusions

The batch made no changes to:

- `PX00`;
- `KNOWLEDGE_CORE`;
- `KNOWLEDGE_MASTER`;
- future/reserved KB repositories;
- recently active project repositories.

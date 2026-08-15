# Classification Batch 20

Date: 2026-08-15
Scope: safe legacy classification only. No repository deletion, merge, rename, move, or GitHub archive action was performed.

## Policy guardrails

This pass preserves the fixed repository policy:

- `PX00` — do not modify, rename, merge, archive, move, or restructure.
- Active and future knowledge-base repositories — do not move, merge, or archive.
- Recent active work — do not normalize in place.
- Legacy repositories are classified before any future disposition decision.

## Classified repository

### `VictorKVS/mq-diploma`

**Disposition:** `LEARNING / EXTERNAL COURSE FORK`

Evidence:

- GitHub metadata reports `fork: true`.
- Parent/source repository is `netology-code/mq-diploma`.
- The README explicitly describes a diploma project for the course «Адаптивная и мобильная вёрстка» and contains implementation requirements supplied for that course.
- The repository surface is therefore learning evidence/reference material, not a current VictorKVS product or MVP truth source.
- The user fork has no recent active product-development signal that would justify treating it as protected recent work.

Decision:

- Keep the repository intact.
- Do not delete or physically archive it in this pass.
- Do not promote it into the product/showcase layer.
- Treat it as learning provenance when interpreting the public GitHub account.

## Result

The classification reduces the chance that a large course diploma fork is mistaken for a current engineering product while preserving the full learning history.

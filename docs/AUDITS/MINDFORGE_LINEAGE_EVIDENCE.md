# MindForge lineage evidence audit

## Scope

Repositories reviewed in this pass:

- `VictorKVS/MindForge`
- `VictorKVS/MindForge-v2.0x`
- previously reviewed `VictorKVS/MindForge-Studio`

`PX00` is referenced only for architectural positioning and was not modified.

## Evidence summary

### MindForge

- Last visible commit in the reviewed history: 2025-09-16.
- Historical repository with repository-maintenance commits and an earlier MindForge implementation lineage.
- Suitable as preserved lineage/history, not as the canonical public product surface.

Working disposition: **ARCHIVE / LINEAGE**.

### MindForge-v2.0x

- Last visible commit: 2025-11-11.
- Default branch is `develop`.
- Contains substantial architecture/product specification assets:
  - `architecture/ARCH_MindForge_v2.yaml`
  - `architecture/README_architecture.md`
  - `engineering/engineering_spec_*`
  - `product/PRD_MindForge_v2.md`
  - `product/feature_map.yaml`
  - DevSecOps and release workflows.
- The current `src/core` implementation files are only tiny placeholder/stub-sized modules, so the repository does **not** support a claim of a complete industrial AI lifecycle platform today.
- README currently contains only the product title, which also makes the repository easy to over-interpret.

Working disposition: **MERGE-CANDIDATE / ARCHITECTURE-SPEC PREDECESSOR**.

No merge is authorized yet. The unique architecture/product specifications should first be compared against `MindForge-Studio` and any canonical MindForge documentation before deciding whether to migrate, preserve, or archive them.

### MindForge-Studio

Previously reviewed as **SHOWCASE / PARTIAL PRODUCT IMPLEMENTATION** because concrete implementation and test assets exist, while full clean-host/CI reproducibility is still gated.

## Canonical public model

For the portfolio surface, use the following interpretation:

`MindForge lineage` → engineering / MVP-factory concept

`MindForge-Studio` → current inspectable partial product implementation

`PX00` → protected advanced autonomous engineering-intelligence evolution

`MindForge-v2.0x` → architecture/specification predecessor and merge candidate, not a shipped platform claim

`MindForge` → historical lineage repository

## Safety decision

No source repository was renamed, archived, merged, deleted or rewritten in this pass.

## Next gate

Before any physical consolidation:

1. compare unique architecture/spec documents from `MindForge-v2.0x` with `MindForge-Studio`;
2. identify which documents remain technically unique and current;
3. migrate only verified unique material into the canonical documentation layer;
4. preserve provenance/history;
5. only then decide whether the predecessors become archived repositories.

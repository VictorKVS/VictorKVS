# Engineering Showcase Index

This index is the working truth model for the public portfolio. Statuses are intentionally conservative and are upgraded only after repository-level evidence review.

| Repository / line | Domain | Current presentation status | Normalization action |
|---|---|---|---|
| `PX00` | Autonomous Engineering Intelligence | **PROTECTED ACTIVE CORE / ADVANCED MINDFORGE EVOLUTION** | Show architecturally; do not rename, merge, archive, move or restructure |
| `KNOWLEDGE_CORE` | Knowledge / Security | **ACTIVE KNOWLEDGE SYSTEM / PROTECTED DURING KB BUILD** | Continue evidence-driven population; do not simplify domain structure prematurely |
| future KB repositories | Knowledge Engineering | **RESERVED / FUTURE KB** | Leave untouched until knowledge-domain boundaries stabilize |
| `SecGraph` | Cybersecurity | PRODUCT CONCEPT + IMPLEMENTATION REPO | Verify executable scope, tests and current MVP boundary before labelling MVP |
| `OSINT_deepseek` | OSINT / Intelligence | ACTIVE DEVELOPMENT | Normalize README, architecture, evidence and demo path without disturbing active work |
| `MindForge-Studio` | AI / Engineering Factory | **SHOWCASE / PARTIAL PRODUCT IMPLEMENTATION** | Use as current inspectable MindForge product surface; require clean-host/CI evidence for stronger maturity |
| `MindForge` | AI / Engineering Factory | **ARCHIVE / LINEAGE** | Preserve as historical MindForge lineage; do not use as canonical product surface |
| `MindForge-v2.0x` | AI / Architecture | **MERGE-CANDIDATE / ARCHITECTURE-SPEC PREDECESSOR** | Preserve unique PRD/architecture/spec material; compare before any migration; current src/core is stub-sized |
| `META-FOUNDRY` | Meta Engineering | PLATFORM VISION | Connect vision to concrete products and avoid presenting unshipped components as complete |
| `MVP` | Agent Infrastructure | MVP SPEC / PROTOTYPE | Verify runnable Universal Agent Gateway implementation and choose canonical product identity later |
| `Librarian-AI` | Knowledge / AI | PROTOTYPE CANDIDATE | Compare with `librarian_ai` only after active/KB reservation checks |
| `devsafe` | Cybersecurity / DevSecOps | **SHOWCASE CANDIDATE / PARTIAL IMPLEMENTATION** | Concrete core modules and test assets verified; require clean-host end-to-end proof before MVP promotion |
| `SecureMaze` | Cybersecurity | PLACEHOLDER / EARLY | Do not feature until content exists |
| `AI_Neural_Networks` | AI Learning / Engineering | STRUCTURED LEARNING TRACK | Supporting engineering evidence, not core flagship |
| `-DevSecOps-Engineer-Profile` | Historical professional profile | LEGACY PROFILE | Preserve as history; profile landing page is `VictorKVS/VictorKVS` |

## MindForge lineage truth model

Public positioning now uses this evidence-backed sequence:

`MindForge (historical lineage) -> MindForge-v2.0x (architecture/spec predecessor) -> MindForge-Studio (inspectable partial product) -> PX00 (protected advanced autonomous evolution)`

This sequence expresses conceptual evolution, not a physical repository merge and not a claim that every planned capability is shipped. See `docs/AUDITS/MINDFORGE_LINEAGE_EVIDENCE.md`.

## Protected classes

### `PROTECTED / ACTIVE CORE`
Repository is architecturally visible but excluded from cleanup mutations. Current member: `PX00`.

### `RESERVED / FUTURE KB`
Potential knowledge-base repositories are excluded from cleanup, merging and renaming while the multi-domain knowledge corpus is being built. They will be placed later when their final domain ownership is known.

### Recent active work
Repositories changed during the active window are not cleanup targets. Inactivity is only a filter for review; it does not authorize destructive changes.

## Candidate processing for older repositories

An older, non-protected, non-KB repository is reviewed and assigned exactly one working disposition:

- `SHOWCASE` — deserves product-facing normalization;
- `LEARNING` — useful learning history, moved out of the visual foreground;
- `ARCHIVE` — historical project retained for provenance;
- `MERGE-CANDIDATE` — probable duplicate/superseded line; no merge until canonical content is verified.

## Portfolio truth gate

A repository enters **Featured Engineering** only when the profile can truthfully answer:

- What problem does it solve?
- What works today?
- How can someone reproduce or inspect it?
- What is the architecture?
- What evidence exists: tests, CI, benchmarks, source provenance or demo?
- What does *not* work yet?

Until those answers exist, status remains `RESEARCH`, `PROTOTYPE`, `KNOWLEDGE`, `LEARNING`, `PLACEHOLDER` or another conservative label rather than `MVP`.

## Target showcase structure

1. `PX00` — protected advanced MindForge evolution / autonomous engineering intelligence
2. `KNOWLEDGE_CORE` — evidence-backed knowledge infrastructure
3. `SecGraph` — security product line after MVP evidence gate
4. `OSINT_deepseek` — OSINT/intelligence engineering
5. `MindForge-Studio` — current inspectable MindForge engineering/MVP-factory product surface
6. `devsafe` — developer safety / DevSecOps product candidate after end-to-end proof
7. canonical Universal Agent implementation after audit
8. canonical Librarian AI implementation after audit
9. `META-FOUNDRY` — ecosystem/meta-engineering layer
10. future verified MVP products generated by the ecosystem

The showcase will expand as the knowledge bases and MVP products mature; it is not frozen to today's repository boundaries.

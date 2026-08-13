# Repository Classification Register

This register drives portfolio normalization. It is intentionally non-destructive.

## Policy

- `PX00` — **PROTECTED / ACTIVE CORE**. Never rename, merge, archive, move or restructure during portfolio cleanup.
- Active and future knowledge-base repositories — **RESERVED / FUTURE KB**. Do not consolidate while domain boundaries are evolving.
- Repositories with recent active work remain untouched.
- Inactivity older than three days makes a repository eligible for **review only**; it does not authorize deletion or archival.
- Every reviewed repository receives one disposition: `SHOWCASE`, `LEARNING`, `ARCHIVE`, or `MERGE-CANDIDATE`.

## Verified first batch

| Repository | Evidence | Classification | Action |
|---|---|---|---|
| `Flask_FastAPI` | Description identifies Flask/FastAPI lectures and seminars; last repository update 2023-07-08 | `LEARNING` | Preserve; remove from flagship foreground |
| `Flask` | Description identifies Seminar 1 / introduction to Flask; old repository line | `LEARNING` | Preserve as learning history |
| `Pyton` | Description explicitly says `ДЗ GB`; last push 2024-03-19 | `LEARNING` | Preserve; candidate for later learning-index grouping |

## AI-agent lineage review

| Repository | Evidence | Classification | Action |
|---|---|---|---|
| `BotFabrika` | Last visible commit 2025-05-03. Repository contains project-installer code, a large YAML structure specification and `ProjectsBotArchitect_AI`; README is effectively empty. | `ARCHIVE` | Preserve as an early agent-factory implementation/specification line; do not present as a current product. |
| `BotFerm` | Last visible commit 2025-05-03. Core installer/YAML/directory objects have the same blob/tree SHAs as `BotFabrika`, while README claims a broader complete MVP that is not supported by the inspected repository surface. | `MERGE-CANDIDATE` | Preserve without merging. Treat as a duplicate/superseded agent-factory presentation until unique content is proven. Do not advertise the README's `MVP complete` claim. |

### Agent-lineage conclusion

`BotFabrika` and `BotFerm` are best treated as historical predecessors of the later MindForge/agent-factory direction rather than as separate current products. Their shared repository objects strongly indicate common ancestry/content, but no physical merge or archival action is authorized by this classification alone.

## Protected / reserved

| Repository / class | Classification | Action |
|---|---|---|
| `PX00` | `PROTECTED / ACTIVE CORE / SHOWCASE` | Architectural reference only; no repository mutation |
| `KNOWLEDGE_CORE` | `ACTIVE KNOWLEDGE SYSTEM` | Continue KB build; exclude from cleanup |
| `KNOWLEDGE_MASTER` | `RESERVED KNOWLEDGE` | Exclude from cleanup pending final knowledge architecture |
| future KB candidates | `RESERVED / FUTURE KB` | Leave in place until domain ownership stabilizes |

## Classification quality gate

Before `ARCHIVE` or `MERGE-CANDIDATE` is assigned, inspect enough repository evidence to answer:

1. Is it historical or still a dependency of an active project?
2. Is it a future knowledge-base boundary?
3. Does another repository demonstrably supersede it?
4. Is there unique code, evidence or history worth preserving?
5. Would changing its state break links, demos or automation?

No destructive operation follows automatically from classification.

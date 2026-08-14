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

## Backend learning track

The numbered `DZ` repositories are a curriculum progression, not separate products. The stronger later exercises remain useful supporting engineering evidence while staying classified as `LEARNING`.

| Repository range | Verified direction | Classification | Action |
|---|---|---|---|
| `dz14_html_css_resume` → `DZ19_Getting_Started_with_Models` | HTML/CSS and Django foundations: views, templates, forms and models | `LEARNING` | Group into Engineering Journey |
| `DZ20_Queries_in_Django_ORM` → `DZ_25_Django_web_api` | ORM, CRUD, filtering/sorting and REST/API progression; `DZ_23_I_REST_API` explicitly identifies itself as lesson 23 and course work while showing JWT/RBAC/DRF practice | `LEARNING` | Keep as supporting backend/security evidence, not flagship products |
| `DZ_26_PostgreSQL_PG4` → `DZ_30_SQLAlchemy` | PostgreSQL, SQLAlchemy and FastAPI progression | `LEARNING` | Keep as supporting data/backend evidence |
| `DZ_31_Basic_linux_Commands` → `DZ_36_Web_Socket` | Linux, Nginx, Docker, Gunicorn/WSGI/ASGI and WebSocket progression; last visible work in this segment is 2026-07-26 | `LEARNING` | Keep as supporting deployment/runtime evidence |

### Learning-track conclusion

Public presentation should collapse these repositories into one trajectory rather than present 20+ separate product cards:

`HTML/CSS → Django → ORM/CRUD/API → JWT/RBAC → PostgreSQL/SQLAlchemy → FastAPI → Linux/Nginx/Docker → Gunicorn/ASGI → WebSocket`

No course repository is promoted to MVP solely because its README uses product or enterprise language.

## Product/spec/profile review

| Repository | Evidence | Classification | Action |
|---|---|---|---|
| `PRODUCT_SPEC_UniversalAgent` | Last visible commit 2025-11-25. Contains substantive Universal Agent product specification, MVP architecture, capability/policy model, roadmap and architecture posters; it is primarily specification/governance material rather than the current implementation repository. | `MERGE-CANDIDATE` | Preserve as specification provenance. Later migrate unique validated product/architecture material into the canonical Universal Agent documentation only after comparison; do not physically merge yet. |
| `PRODUCT_SPEC_UniversalAgent-v2.0` | Public repository is empty (`size: 0`). | `ARCHIVE` | Preserve as historical version placeholder; exclude from product foreground. |
| `AI-Product-Architect` | Public repository is empty (`size: 0`). | `ARCHIVE` | Preserve as role/product-direction placeholder; exclude from public product layer. |
| `AI-Trainer-Professional` | Last visible commit 2025-11-25. README states it contains solutions to two mandatory AI-trainer test tasks, each with algorithm description and test data. | `LEARNING` | Preserve as professional/algorithmic exercise evidence; place in learning/journey layer rather than Featured Engineering. |
| `OSINT_Python_Go_Security_Automation` | Public repository is empty (`size: 0`). | `ARCHIVE` | Preserve placeholder/history; do not confuse with the active `OSINT_deepseek` product line. |

### Universal Agent lineage conclusion

The Universal Agent material now separates cleanly into:

1. `PRODUCT_SPEC_UniversalAgent` — product/architecture specification provenance;
2. `PRODUCT_SPEC_UniversalAgent-v2.0` — empty historical placeholder;
3. `MVP` — current inspectable implementation/prototype line used by the public evidence page.

The specification repository is not a second product. It is a `MERGE-CANDIDATE` only in the documentation/provenance sense, and no physical merge is authorized until unique content and link dependencies are checked.

## AI-agent lineage review

| Repository | Evidence | Classification | Action |
|---|---|---|---|
| `BotFabrika` | Last visible commit 2025-05-03. Repository contains project-installer code, a large YAML structure specification and `ProjectsBotArchitect_AI`; README is effectively empty. | `ARCHIVE` | Preserve as an early agent-factory implementation/specification line; do not present as a current product. |
| `BotFerm` | Last visible commit 2025-05-03. Core installer/YAML/directory objects have the same blob/tree SHAs as `BotFabrika`, while README claims a broader complete MVP that is not supported by the inspected repository surface. | `MERGE-CANDIDATE` | Preserve without merging. Treat as a duplicate/superseded agent-factory presentation until unique content is proven. Do not advertise the README's `MVP complete` claim. |
| `mindforge-ai-telegram-bot` | Last visible commit 2026-01-07. Repository contains Docker assets, demo, source/test directories and multiple architecture schemas. README claims enterprise-grade zero-trust/multi-agent capabilities, but current evidence is mixed: some top-level tests are empty, and a tracked `.env` file is present in the public repository. | `SHOWCASE` | Keep out of Featured Engineering until secret/config hygiene is reviewed and a clean-host test run proves the supported boundary. Treat broad README claims as unverified until then. |
| `spaceai-agent-platform` | Last visible commit 2025-12-22. Repository surface is primarily architecture, policy, contracts, audit and partner-facing documentation; README itself is only a title. | `ARCHIVE` | Preserve as architecture/product-strategy lineage. Do not present as shipped platform without runnable implementation evidence. |
| `agent-ecosystem-crkfl` | Public repository is empty (`size: 0`) with no inspectable implementation or evidence. | `ARCHIVE` | Preserve placeholder/history; exclude from product foreground. |

### Agent-lineage conclusion

The old agent repositories now separate into three useful historical layers:

1. `BotFabrika` / `BotFerm` — early agent-factory lineage;
2. `spaceai-agent-platform` / `agent-ecosystem-crkfl` — architecture/placeholder lineage;
3. `mindforge-ai-telegram-bot` — the strongest old inspectable implementation candidate, but blocked from promotion by evidence and repository-hygiene gaps.

They are predecessors/supporting branches of the later MindForge/PX00 direction, not peer production products. No physical merge or archive mutation is authorized by this register.

## Architecture predecessor review

| Repository | Evidence | Classification | Action |
|---|---|---|---|
| `NAM` | Last visible commit 2025-12-06. Current repository contains a minimal README, `NAM_shema.md`, architecture docs and API specification. The schema describes a much larger intended `src/`, `kb/`, security and policy tree than is actually present in the inspected repository surface. | `ARCHIVE` | Preserve as architecture/specification lineage. Do not present the proposed tree as implemented functionality. |
| `AURORA-Intelligence-Platform-` | Repository is currently empty; no inspectable files or implementation evidence. | `ARCHIVE` | Preserve as historical naming/product-direction placeholder; exclude from product foreground. |
| `H-Mindforge-industrial-ai-suite` | Repository is currently empty; no inspectable files or implementation evidence. | `ARCHIVE` | Preserve as historical MindForge product-direction placeholder; do not use as evidence for current MindForge/PX00 capability. |
| `MindForge-Factory-Website` | Last visible commits are 2026-01-23. Repository contains a legacy GitHub Pages/Jekyll-style site and documentation that calls itself the official MindForge Factory showcase and lists broad factory capabilities/projects, while the same document leaves implementation choices and multiple product lines as planned/in-progress. | `ARCHIVE` | Preserve as historical website/product-positioning lineage. Canonical public truth surface is now `VictorKVS/VictorKVS`; do not treat legacy website claims as shipped capability evidence. |

### Architecture-lineage conclusion

These repositories are useful as provenance for the evolution of the engineering-intelligence architecture, but they are not current products. Public maturity remains tied to inspectable implementation and reproducible evidence rather than repository names, historical websites or proposed directory structures.

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
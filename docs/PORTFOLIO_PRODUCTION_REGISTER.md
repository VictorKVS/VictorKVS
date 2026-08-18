# Portfolio Production Register

**Owner:** Viktor Kulichenko (`VictorKVS`)  
**Audit date:** 18 August 2026  
**Inventory:** 108 repositories  
**Purpose:** one evidence-backed register of products, active development,
architecture/specification work, learning history and archive candidates.

## How the percentage is calculated

The number is readiness of the **current declared milestone**, not completion of
an unlimited vision:

| Gate | Weight |
|---|---:|
| Scope and acceptance criteria | 10% |
| Architecture, API and data model | 15% |
| Working primary scenario | 25% |
| Automated tests and regression | 20% |
| Clean installation / reproducible run | 15% |
| README, demo and screenshots | 10% |
| Security, release and monitoring gate | 5% |

Percentages are raised only by inspectable evidence. `Roadmap`, repository name
and README claims are not shipped functionality.

## Active production portfolio

| Repository | Role | Status | Readiness | What is proven | Next gate |
|---|---|---|---:|---|---|
| [father-quant-lab](https://github.com/VictorKVS/father-quant-lab) | Evidence-based backtest and paper-trading lab | Research MVP | **82%** | Package, CLI, 18 test files, evidence and strict MODELLED/PAPER/LIVE gates | Historical real-data and paper validation |
| [OSINT_deepseek](https://github.com/VictorKVS/OSINT_deepseek) | OSINT evidence supplier | Verified DEV / M5 active | **78%** | Frozen DEV runner, extensive tests, CI, provenance and traceability | Production MTProto, secrets, monitoring and Knowledge Gate |
| [Vibe-coding](https://github.com/VictorKVS/Vibe-coding) | Vibe Coding coursework and MVP laboratory | MVP candidate | **75%** | GitHub Pages workflow; BOOK·CRAFT React MVP, local LLM, recovery and UI tests | Publish BOOK·CRAFT MEDIA backend and screen recording |
| [FATHER-Engineering-Competency-Lab](https://github.com/VictorKVS/FATHER-Engineering-Competency-Lab) | Engineering competency factory | Working learning MVP | **74%** | Python/Pong case, package, tests, evidence, benchmarks and experiments | Validate C++ and Go as separate tracks |
| [FATHER-Automation-Control-Center](https://github.com/VictorKVS/FATHER-Automation-Control-Center) | Portfolio and task-stream control center | Operating MVP | **66%** | Registry, capacity scripts, tests, generated reports and day protocols | Automated live refresh of all project metrics |
| [devsafe](https://github.com/VictorKVS/devsafe) | Windows developer safety and backup automation | DEV MVP | **62%** | Core modules, CLI, guardrail tests and documentation | Clean Windows install and one-click demonstration |
| [KNOWLEDGE_CORE](https://github.com/VictorKVS/KNOWLEDGE_CORE) | Evidence-driven knowledge and Security KB | Knowledge MVP | **57%** | Legislation, controls, applicability, provenance, threats, roles, deadlines, validators and fixtures | Measured corpus coverage and runnable graph/RAG service |
| [MindForge-Studio](https://github.com/VictorKVS/MindForge-Studio) | Local visual AI studio | Creative laboratory | **55%** | Forge/Comfy adapters, pipelines and smoke/stability/VRAM test assets | Consolidated reproducible UI and pipeline |
| [Librarian-AI](https://github.com/VictorKVS/Librarian-AI) | Document-to-knowledge agent | Advanced prototype | **55%** | Extraction, graphs, LLM routing, databases, Web/Telegram, Docker and CI assets | Clean install and fresh end-to-end tests |
| [KNOWLEDGE_MASTER](https://github.com/VictorKVS/KNOWLEDGE_MASTER) | Knowledge factory and governed LLM orchestration | DEV prototype | **54%** | Adapters, API, decisions, governance, intake, validation, tests and playbooks | Reproducible bounded end-to-end scenario |
| [mindforge-ai-telegram-bot](https://github.com/VictorKVS/mindforge-ai-telegram-bot) | Telegram AI / UAG / RAG lineage | **SECURITY HOLD** | **50%** | Substantial code and test/spec surface | Revoke possible secrets, remove tracked `.env` from HEAD/history, rerun tests |
| [MindForge](https://github.com/VictorKVS/MindForge) | Knowledge and agent core predecessor | Early technical MVP | **45%** | Core, health API, ingest/preview/summary and tests | Clarify safe malware fixture and reproducible demo |
| [MVP](https://github.com/VictorKVS/MVP) | Universal Agent implementation line | Partial prototype | **40%** | Routing, JWT/RBAC, SQL/provider and observability evidence | Clean end-to-end gateway run |
| [Sokrat](https://github.com/VictorKVS/Sokrat) | Research orchestration | Research prototype | **35%** | Concrete code/test structure and historical integration evidence | Fresh clean-host verification |
| [META-FOUNDRY](https://github.com/VictorKVS/META-FOUNDRY) | Meta-engineering standards portal | Documentation framework | **35%** | Standards, schemas, workflows and Pages assets | Measurable implementation path |
| [librarian_ai](https://github.com/VictorKVS/librarian_ai) | Librarian Mini Core | Prototype / predecessor | **35%** | Async pipeline, loaders, embeddings and API/DB skeleton | Tests, CI and canonical merge decision |
| [PRODUCT_SPEC_UniversalAgent](https://github.com/VictorKVS/PRODUCT_SPEC_UniversalAgent) | Universal Agent product specification | Pre-implementation | **27%** | Structured vision, requirements, use cases, governance and architecture | Connect specification to canonical runtime |
| [gpt-agent](https://github.com/VictorKVS/gpt-agent) | Information-security document corpus | Knowledge corpus | **20%** | Large PDF/DOCX/TXT evidence collection | Ingestion, provenance, permissions and RAG pipeline |
| [MindForge-v2.0x](https://github.com/VictorKVS/MindForge-v2.0x) | Industrial AI architecture predecessor | Architecture R&D | **20%** | Product YAML, architecture and DevSecOps/release workflows | Implement the declared runtime boundary |
| [father-media-lab](https://github.com/VictorKVS/father-media-lab) | Evidence-driven image/video factory | L0 inventory/governance | **15%** | Model inventory, deterministic prototype, passports and tests | Prove the first local SDXL generation path |
| [AI_Neural_Networks](https://github.com/VictorKVS/AI_Neural_Networks) | Neural-network curriculum | Learning track started | **12%** | First notebooks in a planned 28-topic path | Complete and verify the foundational block |
| [SecGraph](https://github.com/VictorKVS/SecGraph) | Security intelligence / regulatory graph | Concept / specification | **10%** | Product and KB specifications | Runnable graph, API, tests and demo |
| [Developer-of-AI-agents](https://github.com/VictorKVS/Developer-of-AI-agents) | Universal-agent training platform | Concept / technical brief | **5%** | Architecture narrative | First runnable vertical slice |
| `PX00` | Autonomous Engineering Intelligence | Protected active core | **milestone only** | Architectural role is public; internals protected from portfolio cleanup | Score the current named milestone, never the infinite vision |

## Architecture, governance and standards

These are valuable provenance or design repositories, but are not advertised as
finished software products:

- `META-FOUNDRY`, `PRODUCT_SPEC_UniversalAgent`,
  `PRODUCT_SPEC_UniversalAgent-v2.0`, `KNOWLEDGE_MASTER`, `KNOWLEDGE_CORE`,
  `mf-std-001-compliance-pack`, `mindforge-polygon-framework`, `NAM`,
  `spaceai-agent-platform`, `agent-ecosystem-crkfl`, `AURORA-Intelligence-Platform-`,
  `H-Mindforge-industrial-ai-suite`, `MindForge-Factory-Website`, `PX00`.

## Creative and agent lineage

- Canonical active surfaces: `MindForge-Studio`, `Librarian-AI`, `Vibe-coding`,
  `father-media-lab`.
- Predecessors or alternate cores: `MindForge`, `MindForge-v2.0x`,
  `librarian_ai`, `BotFabrika`, `BotFerm`, `mindforge-ai-telegram-bot`,
  `gpt-agent`, `MVP`, `Sokrat`, `-art_studio_orders_bot`, `VisionToFigma`,
  `ai-companion-prompt-engineering`, `ES-Agent-SiteManager`.
- `mindforge-ai-telegram-bot` remains on **SECURITY HOLD** until its tracked
  `.env` and Git history are remediated and any exposed credentials are rotated.

## Security and OSINT lineage

- Active/candidate: `OSINT_deepseek`, `SecGraph`, `devsafe`, `KNOWLEDGE_CORE`,
  `father-quant-lab`.
- Specification/history: `OSINT_Python_Go_Security_Automation`,
  `osint-fraud-go-python-toolkit`, `SecureMaze`, `-olygon`,
  `mindforge-polygon-framework`, `-DevSecOps-Engineer-Profile`,
  `hacking-books`, `hackerspace-blueprint`.

## Engineering Journey — learning repositories

These repositories prove the training path but do not compete with products on
the first screen:

- Foundations: `Flask`, `Flask_FastAPI`, `diving-into-python`, `Pyton`,
  `git_workouts`, `ETL-`, `Knut1`, `TABL_MENDELEVA`, `js-game`, `files_serialization`.
- Web/backend path: `dz14_html_css_resume`, `z15-sait_django-`, `DZ16_Views_URLs`,
  `DZ17_Templates-`, `DZ18_Working_with_forms`, `DZ19_Getting_Started_with_Models`,
  `DZ20_Queries_in_Django_ORM`, `Filtering-and-sorting`,
  `DZ21_Filtering_and_sorting`, `DZ22_CRUD_and_-aggregate_operations`,
  `DZ_22_I_REST_API`, `DZ_23_I_REST_API`, `DZ_24_Django_-REST_-Framework`,
  `DZ_25_Django_web_api`, `DZ_26_PostgreSQL_PG4`,
  `DZ_27_SQL_ORM_SQLAlchemy`, `DZ_28_Alchemy`, `DZ_29_FastAPI`,
  `DZ_30_SQLAlchemy`, `DZ_31_Basic_linux_Commands`,
  `DZ_32_Configuring_-Nginx`, `DZ_33_Docker`,
  `DZ_34_Django.-Wsgi-gunicorn-nginx`, `DZ_354_Django.-Wsgi-gunicorn-nginx_2`,
  `DZ_35_Django.-Wsgi-gunicorn-nginx_2`, `DZ_36_Web_Socket`.
- Course collections: `html-homeworks`, `mq-homeworks`, `hj-homeworks`,
  `aqa-homeworks`, `scada-4-homeworks`, `mq-diploma`, `and2-code`, `iOS`,
  `guides`, `294-book`, `Learn-Model-Context-Protocol-with-Python`,
  `DZ_1_Introduction_to_Vibe_coding_and_-the_first_assistant`,
  `DZ_1_Introduction_to_Vibe_Telegrame`, `AI-Trainer-Professional`,
  `AI_Neural_Networks`.

## Historical, empty or archive-review candidates

No destructive action is authorized by this register. These repositories stay
preserved but are removed from the product foreground until unique value or an
active dependency is demonstrated:

`https-github.com-your-username-botarchitect-ai`,
`PRODUCT_SPEC_UniversalAgent-v2.0`, `MindForge-Engineer-Profile`,
`OSINT_Python_Go_Security_Automation`, `AI-Product-Architect`,
`H-Mindforge-industrial-ai-suite`, `agent-ecosystem-crkfl`,
`ai-companion-prompt-engineering`, `SecureMaze`, `AURORA-Intelligence-Platform-`,
`-art_studio_orders_bot`, `-olygon`, `VisionToFigma`, `ETL-`, `Knut1`,
`MindForge-Factory-Website`, `BotFabrika`, `BotFerm`, `spaceai-agent-platform`,
`NAM`, `sait_pit`, `shop_pit`, `pit_ochibki`, `usir-1`, `brary_manager_project`,
`PX00` is explicitly excluded from this archive class despite its special
handling.

## Update protocol

1. Re-run the repository inventory.
2. Recalculate only projects whose evidence changed.
3. Record evidence and date; do not change percentages from optimism.
4. Move a project to a higher maturity class only after its next gate passes.
5. Keep private repositories and secrets out of the public register.
6. Synchronize this register, profile README, `status.html` and FATHER Control
   Center dashboard.

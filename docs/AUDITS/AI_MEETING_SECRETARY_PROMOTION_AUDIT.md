# AI Meeting Secretary — MVP Promotion Audit

Date: 2026-08-15

Status: **MVP-CANDIDATE / ACTIVE-SOURCE / EVIDENCE-GATED**

Source inspected read-only: `VictorKVS/Vibe-coding/DZ_5_Integrations_files,_Sheets,_external_APIs`

## Policy boundary

The source repository is recent active work. This audit does **not** authorize moving, renaming, merging, archiving or normalizing the source in place. Productization must happen later as a separate product instance after the active learning/source line stabilizes.

`PX00`, `KNOWLEDGE_CORE`, `KNOWLEDGE_MASTER` and future knowledge-base repositories are architectural references only and are not changed by this promotion path.

## Problem

Meeting and interview workflows commonly require several manual steps: collect media, transcribe it, extract decisions/tasks/owners, publish structured results, create a human-readable protocol and answer follow-up questions. The candidate already combines these stages in one Telegram-oriented workflow.

## Current inspectable capabilities

The inspected source surface contains:

- Telegram application orchestration (`src/app.py`);
- configuration and secret loading (`src/config.py`);
- document processing (`src/documents.py`);
- file-type handling (`src/filetype.py`);
- image normalization (`src/images.py`);
- ingestion boundary (`src/ingestion.py`);
- media handling (`src/media.py`);
- data models (`src/models.py`);
- progress reporting (`src/progress.py`);
- routing and additional service modules in `src/`;
- a one-cell Colab launcher;
- runtime dependencies for Telegram, OpenAI, Google Sheets/auth, PDF, image and Office-document processing.

Current flow represented by the source/inventory:

`Telegram → file/video/link → normalization/ingestion → transcription → AI analysis → tasks/owners → Google Sheets → PDF protocol → follow-up questions`

This is implementation evidence, **not** a claim of production readiness.

## Dependency surface

`requirements.txt` currently declares broad lower-bound ranges including:

- `aiogram >=3.20,<4`;
- `aiohttp >=3.10`;
- `openai >=1.100`;
- `gspread >=6.2` and `google-auth >=2.40`;
- `reportlab >=4.4`;
- `pillow >=11`, `pymupdf >=1.26`;
- `python-docx`, `openpyxl`, `python-pptx`;
- `dateparser` and `gdown`.

For a standalone MVP, reproducibility should be strengthened with a lock/constraint strategy and a documented supported Python version.

## Secret and configuration boundary

The current configuration is explicitly Colab-oriented. `Settings.from_colab()` expects:

- Telegram bot token;
- OpenAI API key;
- AssemblyAI API key;
- Google service-account JSON;
- Google Sheets ID.

Secrets are read through Colab userdata rather than committed in source, which is preferable to hard-coded credentials. However, a standalone MVP still needs a provider-neutral configuration boundary (`.env`/secret manager), startup validation, credential-scope documentation and rotation guidance.

## Persistence and privacy observations

The current configuration creates local runtime paths for downloads, normalized media, transcripts and protocols. This means the future standalone product needs an explicit retention model rather than relying on implicit local persistence.

Before MVP promotion, define:

1. what raw media is stored;
2. what transcript/protocol data is stored;
3. default retention periods;
4. deletion/cleanup behavior;
5. access control and file permissions;
6. whether data is sent to external AI/transcription providers;
7. user-facing disclosure/consent expectations for recorded meetings.

## Evidence gaps

The inspected DZ5 top-level surface does not currently expose a dedicated `tests/` directory. Therefore no claim is made here about an automated test baseline.

The following evidence is still required:

- clean-environment installation;
- deterministic unit tests for parsing/normalization/business rules;
- integration tests with provider calls mocked or sandboxed;
- failure-path tests for unavailable Telegram/OpenAI/AssemblyAI/Google services;
- timeout/retry behavior;
- large-file and unsupported-file limits;
- malformed/corrupted media handling;
- duplicate-event/idempotency behavior;
- Unicode/PDF layout tests;
- Google Sheets schema/idempotency tests;
- secret scanning and dependency/security checks;
- explicit evidence that sample assets contain no sensitive real-world data.

## Target standalone boundary

The course repository should remain learning provenance. A future product instance should use a boundary similar to:

```text
ai-meeting-secretary/
├── src/
│   ├── bot/
│   ├── ingestion/
│   ├── transcription/
│   ├── analysis/
│   ├── outputs/
│   └── config/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── fixtures/
├── docs/
│   ├── architecture.md
│   ├── security.md
│   └── evidence.md
├── examples/
├── .env.example
├── pyproject.toml
└── README.md
```

## Promotion gates

### Gate 0 — current state

**PASS for MVP-CANDIDATE.** There is enough concrete implementation surface to justify continued productization work.

### Gate 1 — reproducible developer build

Required:

- supported Python version;
- deterministic dependency install;
- provider-neutral local configuration;
- example configuration without secrets;
- clean-start instructions;
- one verified end-to-end happy path.

### Gate 2 — automated evidence

Required:

- unit test suite;
- integration fixtures/mocks;
- CI run;
- dependency/security checks;
- documented test results tied to a commit.

### Gate 3 — privacy and failure safety

Required:

- retention/deletion policy;
- external-provider data-flow documentation;
- least-privilege credential model;
- timeout/retry/error behavior;
- safe handling of malformed/untrusted files;
- user-visible failure messages without secret leakage.

### Gate 4 — Verified MVP

Promotion to **VERIFIED MVP** is allowed only after Gates 1–3 have evidence attached to the standalone product repository. Roadmap items remain roadmap items until verified.

## Ecosystem relationship

- **MindForge** — productization process / MVP factory lineage.
- **PX00** — protected advanced autonomous-engineering line; architectural relationship only.
- **KNOWLEDGE_CORE** — possible future evidence/knowledge integration point; no migration or consolidation implied.
- **MVP Lab** — controlled bridge from Vibe/learning implementation to standalone reproducible product.

## Recommended next action

Keep `Vibe-coding` unchanged. When the active DZ5 line stabilizes, create a separate `ai-meeting-secretary` product instance from a reviewed snapshot, then satisfy Gate 1 before adding any stronger public maturity label.

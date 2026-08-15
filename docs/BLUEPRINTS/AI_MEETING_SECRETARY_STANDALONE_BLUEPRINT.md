# AI Meeting Secretary — Standalone MVP Blueprint

Date: 2026-08-15
Status: **DESIGN READY / IMPLEMENTATION NOT YET EXTRACTED**

This blueprint defines the future standalone product boundary for the AI Meeting Secretary candidate currently evidenced inside the active `VictorKVS/Vibe-coding` source line.

It does **not** authorize changing, moving, renaming, merging or archiving the active source repository. Product extraction should happen only as a separate repository or reviewed snapshot when the source line is stable.

## Product problem

Meeting and interview workflows often require repetitive manual work across media ingestion, transcription, structured analysis, task/owner extraction, protocol generation, tabular export and follow-up questions. The candidate already demonstrates these stages in one Telegram-oriented workflow.

## MVP boundary

The first standalone MVP should prove one reliable end-to-end path:

`Telegram upload → normalized media/document → transcription → structured AI analysis → tasks/owners → PDF protocol + optional Google Sheets row → user confirmation`

Everything outside this path remains optional until separately evidenced.

## Proposed repository structure

```text
ai-meeting-secretary/
├── src/
│   └── meeting_secretary/
│       ├── bot/
│       ├── ingestion/
│       ├── transcription/
│       ├── analysis/
│       ├── outputs/
│       ├── storage/
│       └── config/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── fixtures/
├── docs/
│   ├── architecture.md
│   ├── security.md
│   ├── privacy.md
│   └── evidence.md
├── examples/
├── .env.example
├── pyproject.toml
├── README.md
└── LICENSE
```

## Architecture contracts

### 1. Ingestion

Input contract:
- Telegram file/document/video/audio metadata;
- local or temporary file handle;
- declared content type and size.

Output contract:
- normalized internal asset descriptor;
- validated MIME/type;
- bounded size/duration metadata;
- deterministic cleanup ownership.

### 2. Transcription provider

Provider interface should be isolated from orchestration:

```python
class TranscriptionProvider(Protocol):
    async def transcribe(self, asset: MediaAsset) -> Transcript: ...
```

AssemblyAI can remain the first implementation, but orchestration should not depend on provider-specific response objects.

### 3. Analysis provider

```python
class AnalysisProvider(Protocol):
    async def analyze(self, transcript: Transcript) -> MeetingAnalysis: ...
```

The output model should explicitly separate:
- summary;
- decisions;
- tasks;
- owners;
- deadlines;
- unresolved questions;
- confidence/evidence references where feasible.

### 4. Output adapters

Each output channel should be independent:
- PDF protocol;
- Google Sheets adapter;
- Telegram response;
- future knowledge/evidence export.

Failure of an optional output must not invalidate a successfully produced transcript and analysis unless the user explicitly requests transactional behavior.

## Configuration model

The standalone product should replace Colab-specific secret loading with a provider-neutral configuration boundary.

Minimum configuration groups:
- `TELEGRAM_*`;
- `OPENAI_*`;
- `TRANSCRIPTION_*`;
- `GOOGLE_*`;
- `STORAGE_*`;
- `LIMITS_*`;
- `RETENTION_*`.

Required properties:
- `.env.example` contains names only, never credentials;
- startup validation fails fast on missing mandatory settings;
- optional providers can be disabled explicitly;
- credentials are never logged;
- service-account scopes are documented;
- file and message limits are configurable.

## Dependency and runtime baseline

Gate 1 should select and document one supported Python version, initially recommended as Python 3.12 unless source compatibility tests prove otherwise.

The standalone instance should use `pyproject.toml` plus a deterministic lock/constraints mechanism. Broad lower-bound-only requirements are insufficient evidence for reproducibility.

## Minimal test matrix

### Unit
- supported/unsupported file detection;
- size and duration limits;
- normalization routing;
- transcript model validation;
- task/owner/deadline parsing;
- PDF-safe Unicode content;
- configuration validation;
- retention timestamp logic.

### Integration with mocks/sandboxes
- Telegram event → ingestion;
- ingestion → transcription provider;
- transcript → analysis provider;
- analysis → PDF;
- analysis → Google Sheets;
- provider timeout and retry behavior;
- duplicate Telegram update/idempotency.

### Security/privacy
- secret scanning;
- dependency audit;
- malicious or malformed file fixtures;
- filename/path traversal rejection;
- bounded temporary storage;
- cleanup after success and failure;
- logs contain no secrets or raw sensitive payloads by default.

## Data lifecycle

The standalone MVP must explicitly define four storage classes:

1. raw uploaded media;
2. normalized temporary media;
3. transcript and structured analysis;
4. generated outputs such as PDF or Sheets records.

For each class document:
- location;
- encryption expectations;
- access permissions;
- default retention;
- deletion trigger;
- external-provider transfer;
- recovery/backup policy, if any.

Default principle: retain the minimum data necessary for the requested result.

## Evidence package for Gate 1

Gate 1 can be marked PASS only when a commit in the standalone product repository carries:

1. supported Python version;
2. deterministic install instructions;
3. `.env.example` and provider-neutral configuration;
4. clean-start README;
5. one verified end-to-end happy-path transcript/protocol run using non-sensitive sample data;
6. an evidence document with command, environment and result tied to the commit SHA.

This does not yet imply production readiness or Gate 2/3 completion.

## README contract for the standalone product

The product README should contain, in this order:

1. Problem
2. Current capabilities
3. Architecture
4. Quick start
5. Configuration
6. Evidence
7. Security & privacy boundary
8. Limitations
9. Roadmap
10. Ecosystem relationship

Roadmap features must never appear under Current capabilities until verified.

## Ecosystem relationship

- **MindForge** — productization and MVP-factory lineage.
- **PX00** — protected advanced engineering-intelligence core; architecture relationship only.
- **KNOWLEDGE_CORE** — potential future evidence/knowledge sink; no migration or consolidation is implied.
- **MVP Lab** — promotion authority for this product line.

## Promotion sequence

`ACTIVE VIBE SOURCE → reviewed snapshot → standalone repository → Gate 1 reproducibility → Gate 2 automated evidence → Gate 3 privacy/failure safety → VERIFIED MVP → SHOWCASE`

Until a standalone repository exists and Gate 1 evidence is attached, public status remains **MVP-CANDIDATE / Gate 0 passed**.

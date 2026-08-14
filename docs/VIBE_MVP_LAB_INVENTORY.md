# Vibe Coding → MVP Lab Inventory

Date: 2026-08-15

Purpose: identify product seeds in recent Vibe Coding work **without mutating active repositories**. This is a portfolio/read-only inventory, not a migration plan.

## Policy boundary

- `VictorKVS/Vibe-coding` is recent active work and remains untouched.
- No files are moved out of the active repository in this pass.
- A learning artifact becomes an MVP candidate only after an independent reproducible boundary, tests, security review and evidence are established.
- Roadmap or course wording is never treated as shipped capability.

## Current source surface

The active `Vibe-coding` repository contains at least:

- `DZ/` — learning progression;
- `DZ_4_Menus_buttons_dialog_scripts/` — Telegram interaction/menu/dialog work;
- `DZ_5_Integrations_files,_Sheets,_external_APIs/` — integrated AI Secretary work;
- `assets/` — supporting material.

Latest inspected commits on 2026-08-09 include integrated AI Secretary code, transcription/AI/Sheets/PDF services, secret configuration for Colab, MIME-aware ingestion, Telegram progress management and a one-cell Colab launcher.

## Candidate register

| Candidate | Source | Current evidence | Lab status | Promotion gate |
|---|---|---|---|---|
| AI Meeting Secretary | `Vibe-coding/DZ_5_Integrations_files,_Sheets,_external_APIs` | Telegram workflow; audio/video ingestion; large-file links; audio extraction; transcription; summary/tasks/owners; Google Sheets; PDF protocol; questions over last processed record; runtime dependencies; `src/`; Colab launcher | `MVP-CANDIDATE / ACTIVE-SOURCE` | independent clean run, test suite, failure-path checks, data-retention/privacy review, provider fallback/timeout handling, reproducible secrets setup |
| Telegram Interaction Kit | `Vibe-coding/DZ_4_Menus_buttons_dialog_scripts` | menu/button/dialog learning surface is inspectable in repository structure | `COMPONENT-CANDIDATE / ACTIVE-SOURCE` | extract reusable interface boundary only after active course work stabilizes; add tests and API contract |
| File & Media Ingestion Adapter | DZ5 implementation lineage | MIME-aware ingestion and image/media normalization are visible in recent commits | `COMPONENT-CANDIDATE / ACTIVE-SOURCE` | prove supported file types, size/error limits, malicious-file handling and deterministic tests |
| Transcription Adapter | DZ5 implementation lineage | explicit transcription service and transcript persistence flow | `COMPONENT-CANDIDATE / ACTIVE-SOURCE` | provider abstraction, timeout/retry/error contract, privacy/retention controls, deterministic fixture tests |
| PDF Protocol Generator | DZ5 implementation lineage | PDF meeting protocol generation is part of the current stated flow | `COMPONENT-CANDIDATE / ACTIVE-SOURCE` | stable schema, Unicode/layout tests, deterministic output checks |
| Sheets Result Adapter | DZ5 implementation lineage | Google Sheets output is part of current stated flow | `COMPONENT-CANDIDATE / ACTIVE-SOURCE` | explicit schema, auth/permission model, idempotency and retry tests |

## First MVP extraction target

**AI Meeting Secretary** is the strongest current candidate because the source already spans an end-to-end user flow:

`Telegram → file/video/link → transcription → AI analysis → tasks/owners → Google Sheets → PDF protocol → follow-up questions`

This is **not yet promoted to Verified MVP**. The active source is a course/Vibe Coding project, and the next productization step should create a separate product instance only after the source work stabilizes.

## Planned productization boundary

When promotion is authorized, use this target shape rather than renaming the course repository:

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

## Relationship to ecosystem

- **MindForge** — product/MVP factory and reusable engineering process.
- **PX00** — protected advanced engineering-intelligence direction; referenced architecturally only, never modified by MVP Lab cleanup.
- **KNOWLEDGE_CORE** — future evidence/knowledge integration point; no migration or consolidation is implied.
- **MVP Lab** — controlled bridge from learning/prototype evidence to standalone reproducible products.

## Promotion model

`VIBE-LEARNING → VIBE-PROTOTYPE → MVP-CANDIDATE → VERIFIED MVP → SHOWCASE`

A candidate advances only when evidence supports the new maturity label.

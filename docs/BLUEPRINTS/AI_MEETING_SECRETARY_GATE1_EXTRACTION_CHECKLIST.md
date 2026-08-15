# AI Meeting Secretary — Gate 1 Extraction Checklist

Date: 2026-08-15
Status: **READY FOR FUTURE EXTRACTION / SOURCE MUST REMAIN UNCHANGED**

This checklist operationalizes Gate 1 for the AI Meeting Secretary MVP candidate. It is intentionally stored in the portfolio repository and does not authorize mutation of the active `VictorKVS/Vibe-coding` source repository.

## Objective

Create a future standalone `ai-meeting-secretary` product instance that can be installed and exercised independently without converting the active learning/experiment repository in place.

Gate 1 proves **reproducibility only**. It does not prove production readiness, security completeness or privacy compliance.

## 1. Source snapshot eligibility

A reviewed source snapshot may be used only when all of the following are true:

- the selected files are tied to an explicit source commit SHA;
- no uncommitted local state is assumed;
- no secrets, tokens, service-account JSON, cookies or personal data are copied;
- generated outputs, notebooks, caches and temporary media are excluded unless deliberately converted into synthetic fixtures;
- provenance is recorded for every copied or adapted module;
- extraction happens into a separate repository or reviewed staging tree;
- the original `Vibe-coding` repository is not renamed, moved, merged, archived or normalized in place.

## 2. Allowed extraction scope

Candidate code may be adapted from the currently evidenced functional areas:

- Telegram interaction/orchestration;
- file and media ingestion;
- transcription adapter;
- LLM analysis adapter;
- task/owner/deadline models;
- PDF protocol generation;
- Google Sheets output adapter;
- follow-up question workflow.

Only code required for the first MVP happy path should be extracted. Course scaffolding, unrelated exercises and experimental branches remain outside the product boundary.

## 3. Explicitly forbidden transfer

Do not carry into the standalone repository:

- real `.env` files;
- API keys or Colab secrets;
- Google service-account credentials;
- Telegram bot tokens;
- AssemblyAI/OpenAI credentials;
- real meeting recordings or transcripts;
- personal or medical data;
- generated PDFs containing real content;
- ad-hoc local paths or notebook-only assumptions;
- unrelated course tasks;
- historical files that are not needed by the MVP path.

## 4. First standalone commit contract

The first product commit should contain at minimum:

```text
ai-meeting-secretary/
├── src/meeting_secretary/
├── tests/
├── docs/
│   ├── architecture.md
│   ├── evidence.md
│   └── provenance.md
├── examples/
├── .env.example
├── .gitignore
├── pyproject.toml
├── README.md
└── LICENSE
```

`provenance.md` must record:

- source repository;
- source commit SHA;
- extracted/adapted paths;
- extraction date;
- known semantic changes;
- excluded sensitive/non-product files.

## 5. Configuration conversion

Before Gate 1 can pass:

- Colab-specific secret access is removed from orchestration;
- configuration is loaded through a provider-neutral application boundary;
- mandatory and optional settings are separated;
- startup validation fails clearly on missing required settings;
- `.env.example` contains variable names and safe placeholders only;
- secrets are never logged;
- Google Sheets integration can be disabled without breaking the core transcript/PDF path.

## 6. Reproducibility baseline

A single supported environment must be declared. Initial target:

- Python 3.12, subject to compatibility verification;
- deterministic dependency resolution;
- documented clean-environment installation;
- one command to run automated tests;
- one command to start the bot/application;
- one non-sensitive sample input path.

If Python 3.12 is not compatible with the extracted source, the supported version must be changed based on evidence rather than assumption.

## 7. Minimum happy-path evidence

Gate 1 requires one reproducible path:

`synthetic sample → ingestion → transcription/provider stub or approved sandbox → structured analysis → PDF protocol`

Google Sheets is optional for Gate 1 and must not block the core path.

Evidence must record:

- standalone repository commit SHA;
- OS/runtime;
- Python version;
- install command;
- execution/test command;
- sample identifier;
- observed result;
- known limitations.

## 8. Minimum automated checks

Before Gate 1 is promoted from DESIGNED to PASS, the standalone repository should have at least:

- configuration validation test;
- supported/unsupported input routing test;
- transcript/analysis model test;
- PDF generation test using synthetic Unicode text;
- optional-output failure isolation test;
- secret scan;
- dependency vulnerability scan or documented equivalent.

These checks are a Gate 1 baseline only. Broader integration, provider timeout/retry, malicious-file handling, idempotency and privacy lifecycle tests remain Gate 2/3 work unless implemented earlier.

## 9. Evidence naming convention

Recommended evidence record:

```text
docs/evidence/gate1-<YYYYMMDD>-<shortsha>.md
```

The record should state one of:

- `PASS` — clean installation and happy path reproduced;
- `FAIL` — attempted and failed, with cause;
- `PARTIAL` — evidence incomplete; promotion prohibited.

Never convert `PARTIAL` into a public maturity claim.

## 10. Gate 1 decision rule

Gate 1 becomes **PASS** only when all are true:

1. standalone product repository exists;
2. provenance ties it to a reviewed source commit;
3. secrets and real user data are absent;
4. provider-neutral configuration works;
5. deterministic installation is documented;
6. automated baseline checks pass;
7. one clean happy-path execution is evidenced against a specific commit SHA.

Until then public status remains:

**MVP-CANDIDATE / Gate 0 passed / Gate 1 designed**.

## Relationship to the ecosystem

- **MindForge** — defines the productization/factory lineage.
- **PX00** — protected engineering-intelligence core; no source mutation or dependency is implied.
- **KNOWLEDGE_CORE** — future evidence/knowledge integration point only.
- **MVP Lab** — owns the promotion decision and public maturity label.

## Next evidence artifact after extraction

The next artifact should be produced inside the standalone product repository, not here:

`docs/evidence/gate1-<date>-<sha>.md`

That file, together with tests and a reproducible clean run, is the boundary between **DESIGNED** and **PASS**.
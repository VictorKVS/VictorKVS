# AI Meeting Secretary — Gate 1 CI/Test Contract

Date: 2026-08-15
Status: **DESIGN CONTRACT / NO MATURITY CLAIM**

This contract defines the minimum CI and test surface required before a future standalone `ai-meeting-secretary` instance may claim Gate 1 PASS. It does not modify or authorize changes to `VictorKVS/Vibe-coding`.

## Required CI jobs

A standalone candidate must run these jobs on pull requests and the default branch:

1. `quality` — dependency install from a deterministic lock, import/compile check, unit tests.
2. `config-contract` — required/optional configuration validation with no Colab-specific secret dependency.
3. `synthetic-happy-path` — synthetic media/document fixture through ingestion, transcription stub, structured analysis and PDF generation.
4. `secret-scan` — repository/history scan for credentials and service-account material.
5. `dependency-scan` — dependency vulnerability scan with results retained as evidence.

## Minimum test matrix

| Area | Required proof |
|---|---|
| configuration | missing required setting fails clearly; optional Sheets integration can be disabled |
| ingestion | supported input routes correctly; unsupported input fails safely |
| transcription boundary | provider adapter can be replaced by deterministic stub |
| analysis model | structured result validates against an explicit schema/model |
| PDF | synthetic Unicode content generates a readable non-empty artifact |
| failure isolation | optional output/provider failure does not corrupt the core result |
| secrets | logs and fixtures contain no live credentials or personal data |
| reproducibility | clean environment can install, test and execute the synthetic path twice |

## Evidence retention

For every Gate 1 candidate commit record:

- standalone commit SHA and reviewed source SHA;
- Python/runtime version;
- dependency lock identifier/hash;
- CI run URL or immutable run identifier;
- test summary and failing-test count;
- secret-scan result;
- dependency-scan result;
- synthetic input identifier and output artifact hash;
- deviations or waivers, if any.

The record must be completed using `AI_MEETING_SECRETARY_GATE1_EVIDENCE_TEMPLATE.md`.

## Promotion rule

Gate 1 remains **DESIGNED / NOT IMPLEMENTED** until the standalone repository exists and all mandatory jobs pass against the same reviewed commit. A green CI badge alone is insufficient: provenance, sensitive-data exclusion and the reproducible synthetic path must also be evidenced.

Gate 1 PASS does not imply production readiness, privacy completeness, operational monitoring, or Gate 2/3 completion.

## Ecosystem boundary

- `VictorKVS/Vibe-coding`: protected recent-active source; read-only for this productization process.
- MindForge: product-factory lineage only.
- PX00: protected core; no mutation or dependency claim.
- KNOWLEDGE_CORE: future evidence/knowledge integration point only.
- MVP Lab: owns public maturity labels.

# Legacy AI-Agent Lineage Evidence Audit

## Scope

Reviewed historical AI-agent repositories without modifying their contents. PX00 and knowledge-base repositories were excluded from mutation.

## `mindforge-ai-telegram-bot`

**Current portfolio disposition:** `SHOWCASE`, promotion blocked.

Observed evidence:

- last visible commit: 2026-01-07;
- repository includes Docker assets, demo material, architecture schemas, source/test structure and GitHub workflow metadata;
- README describes a Telegram UI, security pipeline, UAG, multi-agent layer, retrieval and knowledge integration;
- test tree contains domain folders for agents/API/bot/LLM/spec, but some top-level test files are empty;
- public repository root contains a tracked `.env` file while `.env.example` is empty.

Interpretation:

There is enough implementation surface to keep this repository in the engineering story, but not enough clean reproducibility evidence to support the broad enterprise-grade claims in the README. The tracked configuration file is a repository-hygiene/security blocker and must be reviewed without exposing any contained values.

Promotion gate:

1. secret/config hygiene review;
2. non-secret example configuration;
3. clean-host installation/run proof;
4. executable test inventory with pass/fail evidence;
5. bounded capability statement that separates implemented features from roadmap/architecture;
6. negative security tests for the supported security claims.

## `spaceai-agent-platform`

**Current portfolio disposition:** `ARCHIVE`.

Observed evidence:

- last visible commit: 2025-12-22;
- root contains `audit/`, `connectors/`, `contracts/`, `docs/`, `policies/` and an architecture schema;
- recent historical commits are predominantly documentation, security-claim, roadmap, pricing, UX and partner/demo material;
- README contains only the project title.

Interpretation:

This is useful architecture/product-strategy lineage, but the inspected repository surface does not justify a shipped platform claim. It should remain preserved and linked only from lineage/history documentation.

## `agent-ecosystem-crkfl`

**Current portfolio disposition:** `ARCHIVE`.

Observed evidence:

- repository metadata reports `size: 0`;
- no inspectable implementation/evidence surface.

Interpretation:

Treat as a historical placeholder only. It should not appear in the public product layer.

## Portfolio decision

Historical AI-agent work should be presented as a lineage rather than several parallel products:

`BotFabrika / BotFerm → SpaceAI / Telegram-agent experiments → MindForge lineage → PX00`

This is an architectural/history relationship only. No physical repository merge is implied, and PX00 remains protected from cleanup mutations.

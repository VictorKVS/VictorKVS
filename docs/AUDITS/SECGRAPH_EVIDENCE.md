# SecGraph evidence audit

Audit date: 2026-08-13

## Portfolio status

`SHOWCASE / PRODUCT CONCEPT / IMPLEMENTATION INCOMPLETE`

## Verified repository evidence

- Product README exists.
- `docs/001_kb_core_spec.md` defines the intended KB Core data model, audit requirements and readiness criteria.
- `docs/002_kb_core_tests.md` exists as a test specification.
- `backend/requirements.txt` exists.
- The inspected `backend` tree contains a committed `.venv` directory.

## Evidence gaps

The inspected source tree did not provide enough evidence to claim a runnable MVP. Before promotion, verify:

- runnable application source;
- database schema and migrations;
- implemented node/edge/audit-log model;
- API endpoints;
- executable automated tests;
- clean reproducible setup;
- one end-to-end security-audit or knowledge-graph scenario.

## Repository hygiene risk

A virtual environment is currently stored inside the repository tree. It should not be removed blindly. First verify that no unique files or local-only project artifacts depend on it, then replace it with reproducible dependency/setup instructions.

## Architecture relationship

SecGraph belongs to the product layer and should consume evidence from the protected knowledge layer. PX00 remains a protected active core and is not modified as part of SecGraph normalization.

## Decision

Keep SecGraph visible on the public showcase, but label it conservatively until executable evidence closes the gaps above. Roadmap items remain roadmap items, not shipped-functionality claims.

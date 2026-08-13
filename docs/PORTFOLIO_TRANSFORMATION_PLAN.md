# GitHub Engineering Showcase Transformation Plan

## Goal
Transform the VictorKVS GitHub account from a chronological collection of learning repositories, experiments and product ideas into a coherent engineering showcase built around real MVPs, architecture, evidence and reproducible engineering work.

## Principle
The showcase must distinguish clearly between:

- **FLAGSHIP** — actively developed engineering product or platform with architecture/evidence.
- **MVP** — working minimum product with a defined use case and validation path.
- **PROTOTYPE** — implementation exists but product/operational completeness is limited.
- **RESEARCH** — hypothesis, design exploration or knowledge work.
- **KNOWLEDGE** — curated evidence/knowledge corpus used by products and agents.
- **LEARNING ARCHIVE** — coursework, exercises and historical learning artifacts.
- **ARCHIVE CANDIDATE** — duplicate, empty, superseded or poorly named repository pending manual confirmation before archival.

No repository is deleted solely for presentation reasons. Historical work is preserved and de-emphasized instead.

## Target visitor experience
Within 60 seconds a visitor should understand:

1. What engineering problems Viktor works on.
2. Which products are real and where their maturity stands.
3. How AI, security, knowledge engineering and software engineering connect.
4. Which repositories contain working code versus research/specification.
5. What evidence supports claims: tests, CI, architecture, benchmarks, source provenance and demos.

## Showcase domains

### 1. AI Platforms & Agents
Candidate canonical repositories:
- MindForge
- MindForge-Studio
- PRODUCT_SPEC_UniversalAgent / successor to be selected
- spaceai-agent-platform
- Librarian-AI / librarian_ai canonicalization required
- AI-Trainer-Professional

### 2. Cybersecurity
Candidate canonical repositories:
- SecGraph
- KNOWLEDGE_CORE (Security Knowledge product inside the canonical KB)
- devsafe
- SecureMaze
- mf-std-001-compliance-pack

### 3. OSINT & Intelligence
Candidate canonical repositories:
- OSINT_deepseek
- OSINT_Python_Go_Security_Automation
- osint-fraud-go-python-toolkit

### 4. Knowledge Engineering
Candidate canonical repositories:
- KNOWLEDGE_CORE
- KNOWLEDGE_MASTER (relationship/supersession to be decided)
- Librarian-AI

### 5. Engineering Factory / Meta Systems
Candidate canonical repositories:
- META-FOUNDRY
- MindForge-Factory-Website
- mindforge-polygon-framework
- H-Mindforge-industrial-ai-suite

### 6. Learning & Historical Work
Examples:
- DZ_* repositories
- html-homeworks
- mq-homeworks
- aqa-homeworks
- hj-homeworks
- git_workouts
- diving-into-python
- older isolated Flask/Python/Django exercises

These remain accessible but do not occupy flagship presentation space.

## Standard README contract for flagship/MVP repositories
Every flagship or MVP should progressively expose:

1. **One-line product statement**
2. **Problem**
3. **What works now**
4. **Maturity** (`FLAGSHIP/MVP/PROTOTYPE/RESEARCH/KNOWLEDGE`)
5. **Architecture**
6. **Demo / screenshots / example run** where available
7. **Quick start**
8. **Engineering decisions / ADRs**
9. **Security model** where relevant
10. **Tests and CI evidence**
11. **Limitations / known gaps**
12. **Roadmap**
13. **Related ecosystem repositories**
14. **Agent-readable metadata** (`.ai/manifest.yaml`) where justified

## MVP evidence contract
A project should not be labelled MVP merely because a README says so. Minimum evidence should include as applicable:

- executable path or reproducible demo;
- explicit current feature boundary;
- tests or validation evidence;
- architecture summary;
- known limitations;
- current status date;
- CI/build status where CI exists.

## Canonicalization backlog
Likely duplicate/supersession families requiring inspection before any archive action:

- `Librarian-AI` vs `librarian_ai`
- `MindForge` vs `MindForge-v2.0x`
- `PRODUCT_SPEC_UniversalAgent` vs `PRODUCT_SPEC_UniversalAgent-v2.0`
- `-olygon` vs `mindforge-polygon-framework`
- similarly named Django WSGI/nginx exercises

Poorly named repositories requiring review rather than immediate deletion:

- `https-github.com-your-username-botarchitect-ai`
- repositories with accidental leading `-`
- empty repositories with product-like names

## Transformation phases

### Phase A — Inventory and truth model
- classify every repository;
- identify canonical vs duplicate/superseded repositories;
- record public/private, empty/non-empty, active/stale and documentation status;
- prohibit unsupported maturity claims.

### Phase B — Profile landing page
- present 6–8 strongest engineering products only;
- use concise maturity labels;
- link architecture map and product index;
- keep skills secondary to evidence.

### Phase C — Flagship normalization
Normalize README and evidence contract for canonical projects in this order:
1. KNOWLEDGE_CORE
2. SecGraph
3. OSINT_deepseek
4. MindForge-Studio / MindForge canonical choice
5. Universal Agent canonical choice
6. Librarian canonical choice
7. META-FOUNDRY

### Phase D — Product evidence
For each selected MVP:
- reproducible quick start;
- test/CI evidence;
- screenshot/demo if meaningful;
- architecture diagram;
- current maturity and limitations;
- release/roadmap discipline.

### Phase E — De-noise profile
- classify old coursework as learning archive;
- archive only after explicit canonical/supersession decision;
- fix descriptions/topics where connector/API support permits;
- pin only flagship products on the public profile.

### Phase F — Final adversarial review
Review the GitHub profile from four perspectives:
- recruiter / hiring manager;
- senior architect / CTO;
- security engineer / auditor;
- potential client / technical partner.

A claim that cannot be demonstrated from the repository is weakened or removed.

## Definition of done
The account becomes a coherent portfolio when:

- flagship repositories are easy to identify;
- MVP status is evidence-backed;
- learning history no longer dominates visual perception;
- duplicated product identities are resolved;
- each flagship communicates problem, implementation, architecture, evidence and limitations;
- the profile shows one connected engineering ecosystem rather than unrelated repositories.

# GitHub Pages publication gate

## Current state

The portfolio repository already contains a static site surface:

- `index.html`
- `architecture.html`
- `journey.html`
- `status.html`
- `products/`
- `404.html`
- `.nojekyll`

The repository content is therefore prepared for static publication from the repository root.

## Truth constraint

A live GitHub Pages URL must **not** be advertised until GitHub confirms that Pages is enabled for this repository.

At the last verification pass, the repository Pages API endpoint returned `404 Not Found`. This is treated as an infrastructure/publication blocker, not as evidence that the static site content is incomplete.

## Intended publication source

- Repository: `VictorKVS/VictorKVS`
- Branch: `main`
- Source directory: repository root (`/`)
- Static mode: `.nojekyll`

## Publication acceptance gate

Publication is considered complete only when all conditions below are true:

1. GitHub Pages is enabled for the repository.
2. The configured source is `main` / repository root.
3. GitHub returns a concrete Pages site URL.
4. The live `index.html` loads successfully.
5. Navigation works for Architecture, Products, Engineering Journey and Status.
6. Product/evidence pages return HTTP 200 and do not expose roadmap items as shipped capabilities.
7. `404.html` is served for invalid site paths.
8. No protected repository is changed merely to satisfy the public site.

## Protected boundaries

Publication work must not modify or restructure:

- `PX00`
- `KNOWLEDGE_CORE`
- `KNOWLEDGE_MASTER`
- reserved/future knowledge-base repositories
- recent active development repositories unless their owners explicitly make them part of the publication change

## After publication

Once a live URL exists, update:

- profile `README.md`
- `.ai/manifest.yaml`
- `status.html`

with the confirmed canonical site URL and the date of publication verification.

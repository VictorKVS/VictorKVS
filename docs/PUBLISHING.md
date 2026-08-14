# GitHub Pages publication gate

## Current state

The portfolio repository already contains the static public surface:

- `index.html`
- `architecture.html`
- `journey.html`
- `status.html`
- `products/`
- `404.html`
- `.nojekyll`

A dedicated deployment workflow now exists at `.github/workflows/pages.yml`. It assembles only the public HTML surface into `_site`, uploads it with `actions/upload-pages-artifact`, and deploys it with `actions/deploy-pages`.

## Truth constraint

A live GitHub Pages URL must **not** be advertised until GitHub confirms that Pages is enabled for this repository and a deployment succeeds.

At the latest verification pass, `GET /repos/VictorKVS/VictorKVS/pages` still returned `404 Not Found`. The Actions runs endpoint also returned no recorded runs. This is treated as an infrastructure/publication blocker, not as evidence that the static site content is incomplete.

## Intended publication source

- Repository: `VictorKVS/VictorKVS`
- Branch: `main`
- Publishing mechanism: GitHub Actions
- Workflow: `.github/workflows/pages.yml`
- Public artifact: `_site`
- Static mode: `.nojekyll`

The workflow intentionally publishes only the public site files and `products/`; internal portfolio audit documents under `docs/` are not copied into the Pages artifact.

## One-time repository setting still required

GitHub's official Pages documentation requires custom GitHub Actions workflows to be enabled as the Pages publishing source for the repository. The current connector can write the workflow but cannot change that repository setting.

Required one-time setting in GitHub UI:

`Repository → Settings → Pages → Build and deployment → Source: GitHub Actions`

After that setting is enabled, the prepared workflow can be run manually or triggered by a qualifying push to `main`.

## Publication acceptance gate

Publication is considered complete only when all conditions below are true:

1. GitHub Pages is enabled for the repository with GitHub Actions as the publishing source.
2. `.github/workflows/pages.yml` completes successfully.
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

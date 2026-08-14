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

A dedicated deployment workflow exists at `.github/workflows/pages.yml`. It assembles only the public HTML surface into `_site`, uploads it with `actions/upload-pages-artifact`, and deploys it with `actions/deploy-pages`.

## Truth constraint

A live GitHub Pages URL must **not** be advertised until GitHub confirms that Pages is enabled for this repository and a deployment succeeds.

## Verified blocker — 2026-08-14

Two deployment attempts were executed. The second run used `actions/configure-pages@v5` with `enablement: true`, but GitHub rejected creation of the Pages site with:

`Resource not accessible by integration`

The workflow token had `Pages: write`, but the integration is still not permitted to perform the one-time repository-level Pages enablement. This proves that the remaining blocker is repository configuration/authorization, not the static site content.

To avoid creating a red Actions run on every site-content push while this setting is missing, the Pages workflow is now intentionally **manual-only** (`workflow_dispatch`). Automatic `enablement: true` has been removed. Once Pages is enabled in repository settings, the same workflow can be run manually and should proceed through Configure Pages → artifact build → deploy.

## Intended publication source

- Repository: `VictorKVS/VictorKVS`
- Branch: `main`
- Publishing mechanism: GitHub Actions
- Workflow: `.github/workflows/pages.yml`
- Public artifact: `_site`
- Static mode: `.nojekyll`

The workflow intentionally publishes only the public site files and `products/`; internal portfolio audit documents under `docs/` are not copied into the Pages artifact.

## One-time repository setting required

In GitHub UI open:

`VictorKVS/VictorKVS → Settings → Pages → Build and deployment → Source: GitHub Actions`

This is the only repository-level action that the current GitHub integration cannot perform on its own.

After that setting is enabled:

1. Open `Actions` in `VictorKVS/VictorKVS`.
2. Select `Deploy engineering showcase to GitHub Pages`.
3. Run the workflow on `main`.
4. Confirm the build and deploy jobs are green.
5. Record the concrete Pages URL returned by GitHub.

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

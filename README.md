![Docs](https://github.com/BharatAddress/docs-site/actions/workflows/pages.yml/badge.svg)

# Bharat Address Docs Site

MkDocs site that stitches the project together for non-developers.

Local preview:
```bash
pip install mkdocs mkdocs-material
mkdocs serve
```

CI publish to https://bharataddress.github.io

This repo builds with MkDocs and deploys the generated `site/` to the org GitHub Pages repository `BharatAddress/bharataddress.github.io` via a GitHub Actions workflow.

Setup (one-time by repo admin):
- Create a fine-scoped classic token or PAT with `repo` permission and add it as a repository secret in this `docs-site` repo named `ORG_PAGES_TOKEN`.
- Ensure the org Pages repo exists: `BharatAddress/bharataddress.github.io` (already created).

Deployment flow:
- On push to `main`, the workflow `Deploy Docs to Org Pages` runs:
  - Installs MkDocs dependencies from `requirements.txt`
  - Builds site with `mkdocs build --strict`
  - Publishes `site/` to `BharatAddress/bharataddress.github.io` `main` branch using `peaceiris/actions-gh-pages`.

Local build:
```bash
pip install -r requirements.txt
mkdocs build --strict
open site/index.html
```

## Contributor Guide

- Central guidelines: https://github.com/BharatAddress/.github/blob/main/AGENTS.md

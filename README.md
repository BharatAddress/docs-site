![Docs](https://github.com/BharatAddress/docs-site/actions/workflows/pages.yml/badge.svg)

# Bharat Address Docs Site

MkDocs site that stitches the project together for non-developers.

## At a glance
| Item | Details |
| --- | --- |
| Stack | MkDocs + mkdocs-material |
| Publish | https://bharataddress.github.io |
| Output | Deployed to `BharatAddress/bharataddress.github.io` |

## Local preview
```bash
pip install mkdocs mkdocs-material
mkdocs serve
```

## Local build
```bash
pip install -r requirements.txt
mkdocs build --strict
open site/index.html
```

## Deployment flow
- On push to `main`, the workflow `Deploy Docs to Org Pages` runs.
- Builds with `mkdocs build --strict`.
- Publishes `site/` to `BharatAddress/bharataddress.github.io` via `peaceiris/actions-gh-pages`.

## Repo layout
- `mkdocs.yml`: site configuration.
- `docs/`: documentation content.
- `requirements.txt`: MkDocs deps for CI.

## Who should use this
- Writers and editors maintaining the public docs.
- Maintainers validating doc builds.

## Links
- Public site: https://bharataddress.github.io
- Specs: https://github.com/BharatAddress/specs

## License
See `LICENSE`.

## Contributing
- Keep docs small and focused.
- Validate links locally before merging.
- Central guidelines: https://github.com/BharatAddress/.github/blob/main/AGENTS.md

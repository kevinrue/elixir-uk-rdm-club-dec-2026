# ELIXIR-UK RDM Club — December 2026

Quarto website scaffold for four notebooks presenting precomputed results.

## Render locally

Install [Quarto](https://quarto.org/) and run:

```sh
quarto render
```

The rendered website is written to `docs/`. Preview it locally with
`quarto preview`.

## Publish on GitHub Pages

The workflow in `.github/workflows/publish.yml` renders and deploys the site
when changes are pushed to `main`. Notebook execution is frozen with
`freeze: true`; commit locally generated `_freeze/` results whenever notebook
content changes. In the repository settings, set **Pages → Build and deployment
→ Source** to **GitHub Actions**.

Edit `index.qmd` and the four files in `notebooks/`. Put saved inputs in
`data/` and figures in `figures/`. Run notebooks locally and commit their
`_freeze/` outputs when results need updating. The GitHub Pages build renders
the committed results without executing notebook code.

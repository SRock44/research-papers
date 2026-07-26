# Research Papers

[![Build Papers](https://github.com/SRock44/research-papers/actions/workflows/build.yml/badge.svg)](https://github.com/SRock44/research-papers/actions/workflows/build.yml)

A running collection of my computer-science research papers — written in
LaTeX, published here as I finish them, source and PDF both. Think of it as
a research blog with a build system.

## Papers

| Date | Paper | Summary |
|---|---|---|
| 2026-07 | [Calibrated Ensemble Learning for Outcome Prediction](papers/calibrated-ensemble-learning-for-outcome-prediction/) ([PDF](papers/calibrated-ensemble-learning-for-outcome-prediction/paper.pdf)) | The modeling strategy, full mathematics, and measured results behind a live, gradient-boosted ensemble for binary outcome prediction: an Elo-based strength prior, recency weighting, a stacked XGBoost/LightGBM/CatBoost ensemble with a learned meta-learner, variance-preserving isotonic calibration, and a feature pipeline that rescales its sample-size assumptions across datasets of very different sizes. |

New papers are added to `papers/` as they're finished — see individual
paper directories for abstracts, build instructions, and citation info.

## Repo structure

```
papers/
  <paper-slug>/
    paper.tex     — self-contained LaTeX source (IEEEtran, inline figures, inline bibliography)
    paper.pdf     — compiled PDF
    README.md     — abstract, build instructions, citation
```

Every paper is a single, self-contained `.tex` file — no external image
assets, figures are drawn with TikZ/pgfplots and the bibliography is inline
— so each one builds with nothing but a standard LaTeX distribution.

## Building a paper locally

```bash
cd papers/<paper-slug>
pdflatex paper.tex
pdflatex paper.tex   # run twice to resolve references/citations
```

Requires a LaTeX distribution with `IEEEtran` and `pgfplots` (TeX Live
`full`, or MiKTeX with on-the-fly package installation). A GitHub Actions
workflow ([.github/workflows/build.yml](.github/workflows/build.yml))
compiles every paper on each push to catch build breaks automatically.

## License

Paper text and figures are © Sean Rockwitz, licensed under
[CC BY 4.0](LICENSE) unless a paper states otherwise.

## Contact

Sean Rockwitz — [sean@rockwitz.com](mailto:sean@rockwitz.com) · [GitHub](https://github.com/SRock44)

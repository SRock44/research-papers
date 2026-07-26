# Calibrated Ensemble Learning for Outcome Prediction

**Sean Rockwitz** · Independent Research · July 2026
[Read the PDF](paper.pdf) · [LaTeX source](paper.tex)

## Abstract

This paper presents the modeling strategy, the underlying mathematics, and
the measured results behind a live, gradient-boosted ensemble system for
binary outcome prediction. The strategy combines an Elo-based strength
prior, exponential recency weighting, a three-learner stacked ensemble
(XGBoost, LightGBM, CatBoost) with a learned logistic meta-learner, isotonic
probability calibration with a variance-preserving blend step, and a
domain-adapted feature pipeline that rescales its sample-size assumptions
to fit datasets of very different sizes. We give the full mathematical
treatment behind each design choice: the regularized split-gain criterion
that governs how boosted trees grow, the effective-sample-size argument
behind our recency weighting, the optimizer's-curse argument behind how we
size hyperparameter search spaces, the stacking objective that lets the
ensemble automatically weight its base learners, and the isotonic
calibration and blending equations that keep predicted probabilities both
accurate and informative. We then report results: across our three most
mature models, log-loss ranges from 0.6418 to 0.6624 and Brier score from
0.2179 to 0.2348, and our newest, smallest-data model currently posts the
lowest log-loss of the three (0.6418) alongside 86.7% accuracy on its
highest-confidence predictions (n = 1,520). We conclude that a
domain-adapted feature strategy, grounded in the same shrinkage and
effective-sample-size mathematics used throughout the rest of the
pipeline, is what closes the gap between a smaller dataset and a larger
one.

**Index terms:** gradient boosting, stacked generalization, probability
calibration, hyperparameter optimization, ensemble learning, model
evaluation

## Building

```bash
pdflatex paper.tex
pdflatex paper.tex   # run twice to resolve references
```

Single self-contained file — `IEEEtran` conference class, TikZ/pgfplots
figures, inline bibliography. No external assets required.

## Citation

```bibtex
@unpublished{rockwitz2026calibrated,
  author = {Sean Rockwitz},
  title  = {Calibrated Ensemble Learning for Outcome Prediction},
  year   = {2026},
  note   = {Independent research},
  url    = {https://github.com/SRock44/research-papers/blob/main/papers/calibrated-ensemble-learning-for-outcome-prediction/paper.pdf}
}
```

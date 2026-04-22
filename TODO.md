# LLM-EFA Public Release TODO

This document tracks the public release plan for the **LLM-EFA** repository.
It is written for reviewers, researchers, and users who want to understand what is already public, what will be released next, and what is intentionally deferred until paper acceptance.

> Current policy: to avoid discrepancies with the anonymous review process and unpublished intellectual property, the full model implementation and complete training pipeline will be released after paper acceptance. Before that, we will progressively release the artifacts needed to make the project transparent and as reproducible as possible.

---

## Release strategy

The repository will be opened in stages instead of uploading everything at once.
This is intentional.

- **Stage 1:** repository structure, status statement, public roadmap, and documentation skeletons.
- **Stage 2:** public data documentation, download scripts, preprocessing pipeline, and sample inputs.
- **Stage 3:** paper-aligned results artifacts, metric scripts, and reproducibility configs.
- **Stage 4:** inference/demo utilities and more complete experiment organization.
- **Stage 5 (post-acceptance):** full model implementation, training code, and complete experiment pipeline.

---

## A. Immediate repository credibility tasks

These are the first tasks that should be completed so the repository looks active, structured, and review-friendly.

- [ ] Keep `README.md` concise and explicit about current release status.
- [ ] Maintain this `TODO.md` as the public progress tracker.
- [ ] Add a clear top-level folder structure: `data/`, `configs/`, `scripts/`, `results/`, `docs/`.
- [ ] Add placeholder `README.md` files inside key folders so users know what will appear there.
- [ ] Add a short changelog or update section to record newly released artifacts.
- [ ] Add `LICENSE` and choose an open-source license appropriate for the planned release.
- [ ] Add `CITATION.cff` with paper title, authors, and citation placeholder.

---

## B. Public data artifacts

The first substantial release should focus on data transparency rather than the private model code.

- [ ] Add `data/README.md` describing all input sources used by the public pipeline.
- [ ] Document each data source with:
  - source name
  - access link or acquisition method
  - variable list
  - units
  - temporal granularity
  - timezone
  - geographic coverage
- [ ] Provide weather-data ingestion instructions or scripts.
- [ ] Provide load-demand data ingestion instructions or scripts for public datasets.
- [ ] State clearly which datasets can be redistributed and which must be downloaded by users themselves.
- [ ] Add a small sample dataset for quick sanity checks.
- [ ] Document train/validation/test temporal splits used in public experiments.

---

## C. Preprocessing and feature construction

This stage is especially important for credibility because it shows how raw public signals are converted into model-ready inputs.

- [ ] Release a baseline preprocessing script for weather and load data.
- [ ] Add configurable feature construction modules, including common calendar and lag features where applicable.
- [ ] Document missing-value handling.
- [ ] Document outlier handling and normalization policies.
- [ ] Save processed artifacts in a stable and documented format.
- [ ] Provide one end-to-end script that converts raw public data into processed inputs.

---

## D. Paper result artifacts (pre-acceptance priority)

Before the full model code is public, the repository should still expose enough paper-facing artifacts to show that results are organized and traceable.

- [ ] Release the key tables reported in the paper in machine-readable form.
- [ ] Release the key figures from the paper in `results/figures/`.
- [ ] Add metadata explaining which script/config produced each released table or figure.
- [ ] Add metric computation scripts for MAE, MSE, MAPE, and any other reported metrics.
- [ ] Add the evaluation protocol used for abrupt-change and stable-period analysis.
- [ ] Document any reproduction caveats and the expected variance across runs.

---

## E. Reproducibility assets

These items should let external users reproduce at least the public part of the pipeline even before full training code is available.

- [ ] Release experiment configs for dataset splits, horizons, random seeds, and evaluation settings.
- [ ] Add a script to reproduce the paper's public figures/tables from released result files.
- [ ] Add a minimal evaluation example using sample data.
- [ ] Provide `requirements.txt` or `environment.yml`.
- [ ] Pin major dependency versions.
- [ ] Add a `reproduce.md` guide describing the exact order of commands.

---

## F. User-facing usability tasks

A repository that is technically public but hard to understand is still vulnerable to skepticism, so these tasks matter.

- [ ] Add a quickstart guide for first-time users.
- [ ] Add an FAQ covering common setup and reproducibility questions.
- [ ] Add examples showing how to plug in new public weather/load datasets.
- [ ] Add a repository map so users understand where data, configs, scripts, and results live.
- [ ] Add issue templates for bug reports and reproducibility questions.

---

## G. Post-acceptance release tasks

These items are intentionally deferred until paper acceptance.

- [ ] Release the full LLM-EFA model implementation.
- [ ] Release the full training pipeline.
- [ ] Release inference scripts and runnable examples.
- [ ] Release paper-aligned experiment presets.
- [ ] Release checkpoint usage instructions or model-card documentation, if applicable.
- [ ] Release complete ablation and comparison experiment code where feasible.

---

## H. Suggested execution order

If releasing incrementally, the recommended order is:

1. Clean repository structure and public roadmap.
2. Data documentation and download scripts.
3. Preprocessing pipeline and sample data.
4. Paper result files, metric scripts, and configs.
5. Quickstart and reproducibility guide.
6. Full model/training release after acceptance.

---

## Definition of done

This repository will be considered meaningfully public when the following are true:

- [ ] External users can understand the exact current release scope from the README.
- [ ] External users can obtain or reconstruct the public input data.
- [ ] External users can run at least the public preprocessing and evaluation pipeline.
- [ ] Core paper results are traceable to released configs, scripts, and result artifacts.
- [ ] Deferred items are explicitly identified rather than silently missing.

---

## Near-term practical next steps

To make visible progress quickly, the next concrete additions should be:

- [ ] `data/README.md`
- [ ] `results/README.md`
- [ ] `configs/README.md`
- [ ] `scripts/README.md`
- [ ] one public weather-data download/preprocessing script
- [ ] one sample result table or figure from the paper
- [ ] one environment file

These early artifacts already make the repository look substantially more serious and reduce the risk of being perceived as placeholder-only open source.

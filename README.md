# LLM-EFA

Large Language Models for Short-Term Electricity Demand Forecasting under Abrupt Changes

## Status

This repository is the public repository for the submitted **LLM-EFA** paper.

To keep the release process clear and manageable, materials will be released **progressively**.

## Scope of public release

This repository is intended to release materials that can be shared without exposing sensitive data.

Planned public materials include:

- repository documentation and release notes
- weather data sources and access instructions
- non-sensitive preprocessing or utility scripts
- evaluation scripts and metric definitions
- selected paper-aligned figures, tables, and result artifacts

## Data availability

The **target electricity demand data** used in this project will **not** be released publicly, because it involves **private and sensitive information**.

Only materials that do not disclose private demand data will be made public, such as:

- public weather data sources
- weather data access links or scripts
- documentation of the overall pipeline
- selected reproducibility-related utilities that do not depend on private raw targets

## Repository structure

- `data/`: public data notes and weather-data access information
- `results/`: selected figures, tables, and released result artifacts
- `configs/`: public configuration files where appropriate
- `scripts/`: released utility, preprocessing, or evaluation scripts
- `docs/`: supplementary notes
- `TODO.md`: public release checklist

## Roadmap

See [`TODO.md`](./TODO.md) for the current public release checklist.

## Note

This repository does **not** provide the private electricity demand target data.
Released contents will be limited to materials that are compatible with privacy constraints and the paper release plan.

## LLM-EFA Public TODO

This checklist tracks the public materials planned for this repository.

> Note: private electricity demand target data will not be released.

### Current checklist

#### Repository basics

- [ ] Keep `README.md` updated with the current public release scope
- [ ] Maintain a simple public release checklist in this file
- [ ] Organize the repository into clear folders such as `data/`, `results/`, `configs/`, and `scripts/`

#### Public data documentation

- [ ] Add documentation for public weather data sources
- [ ] Add weather data access links or download instructions
- [ ] Clarify which data are public and which are private

#### Public scripts and utilities

- [ ] Release non-sensitive utility or preprocessing scripts where possible
- [ ] Release evaluation scripts for the reported metrics
- [ ] Add minimal example files or placeholders when appropriate

#### Paper-facing artifacts

- [ ] Release selected figures or tables related to the paper
- [ ] Add brief notes describing released result artifacts

#### Deferred or restricted items

- [ ] Keep private electricity demand target data excluded from public release
- [ ] Release additional code only when it is compatible with privacy constraints and the paper release plan

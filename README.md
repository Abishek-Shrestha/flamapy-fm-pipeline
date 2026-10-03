# Feature Model Analysis with Flamapy

A Python pipeline for analysing feature models and extracting
structural properties and anomaly labels, as a foundation for
machine-learning-based defect and anomaly detection in
variability-intensive systems.

## What this does

Using the Flamapy framework, this pipeline:
- Loads feature models (UVL format)
- Checks satisfiability
- Counts configurations and core features
- Detects anomalies (dead features, false-optional features)
- Assembles the results into a labelled dataset (CSV)

It processes multiple models in one pass and handles malformed
models gracefully.

## Motivation

Feature models describe the variability of configurable systems.
Detecting anomalies (dead features, false-optional features,
misconfigurations) is traditionally done with exact formal methods.
This project builds the labelled data needed to explore a
machine-learning approach to predicting such anomalies — extending
my MSc work on imbalance-aware defect detection into the domain of
variability-intensive systems.

## Files

- `feature_model_analysis.ipynb` — the analysis notebook
- `*.uvl` — the feature models analysed
- `feature_model_analysis.csv` — the resulting labelled dataset

## Tools

- Flamapy 2.6.0
- Python 3.11, Pandas

## Results (sample)

| model | configurations | core features | dead | false-optional |
|-------|---------------|---------------|------|----------------|
| SmartWatch | 54 | 3 | 0 | 0 |
| Xiaomi SmartBand | 21 | 12 | 0 | 0 |
| Data VIZ | 8 | 4 | 0 | 0 |
| Pizza | 228 | 4 | 0 | 0 |

## Author

Abishek Shrestha

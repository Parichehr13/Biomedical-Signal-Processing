# Biomedical Signal Processing

This repository contains coursework and experiments in biomedical signal processing and machine learning.

## Repository Structure

- `CODES2.pdf`
  Assignment/reference document.

- `Sampling/`
  - `Sampling.ipynb`
  - `REPORT.md`
  - `figures/`

- `Windowing/`
  - `Windowing.ipynb`
  - `REPORT.md`
  - `figures/`

- `Filtering/`
  - `Filtering.ipynb`
  - `ecgiddb_person02_rec1.csv`
  - `REPORT.md`
  - `figures/`

- `Classification/`
  Classification notebooks and `REPORT.md`.

- `Regression/`
  Regression notebooks and `REPORT.md`.

- `figures/`
  Auto-generated figures for classification/regression notebooks.

## Notebook Map

### Classification

- `Classification/classification_cross_validation_comparison.ipynb`
- `Classification/classification_fixed_vs_nested_cv.ipynb`
- `Classification/classification_logistic_auc_evaluation.ipynb`
- `Classification/classification_nested_cross_validation_pipeline.ipynb`
- `Classification/REPORT.md`

### Regression

- `Regression/regression_holdout_validation.ipynb`
- `Regression/regression_repeated_kfold_cv.ipynb`
- `Regression/regression_nested_holdout_model_selection.ipynb`
- `Regression/regression_nested_cross_validation_polynomial.ipynb`
- `Regression/REPORT.md`

## Quick Start

1. Create and activate a Python environment.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
4. Run notebooks in sequence:
   `Sampling/Sampling.ipynb` -> `Windowing/Windowing.ipynb` -> `Filtering/Filtering.ipynb` -> `Classification/` -> `Regression/`.

## Reproducibility Notes

- ML notebooks use fixed seeds where applicable.
- Use relative data paths from each notebook location.
- Execute notebooks from a clean kernel for consistent outputs.

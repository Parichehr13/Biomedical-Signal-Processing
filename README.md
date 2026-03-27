# Biomedical Signal Processing

This repository contains coursework and experiments in biomedical signal processing and machine learning.

## Repository Structure

- `CODES2.pdf`
  Assignment/reference document.

- `DSP/`
  - `Sampling/Sampling.ipynb`
  - `Sampling/REPORT.md`
  - `Sampling/figures/`
  - `Windowing/Windowing.ipynb`
  - `Windowing/REPORT.md`
  - `Windowing/figures/`
  - `Filtering/Filtering.ipynb`
  - `Filtering/ecgiddb_person02_rec1.csv`
  - `Filtering/REPORT.md`
  - `Filtering/figures/`

- `ML/`
  - `Classification/` notebooks and `REPORT.md`
  - `Regression/` notebooks and `REPORT.md`
  - `figures/` generated figures for ML notebooks

## Notebook Map

### DSP

- `DSP/Sampling/Sampling.ipynb`
- `DSP/Windowing/Windowing.ipynb`
- `DSP/Filtering/Filtering.ipynb`

### ML Classification

- `ML/Classification/classification_cross_validation_comparison.ipynb`
- `ML/Classification/classification_fixed_vs_nested_cv.ipynb`
- `ML/Classification/classification_logistic_auc_evaluation.ipynb`
- `ML/Classification/classification_nested_cross_validation_pipeline.ipynb`
- `ML/Classification/REPORT.md`

### ML Regression

- `ML/Regression/regression_holdout_validation.ipynb`
- `ML/Regression/regression_repeated_kfold_cv.ipynb`
- `ML/Regression/regression_nested_holdout_model_selection.ipynb`
- `ML/Regression/regression_nested_cross_validation_polynomial.ipynb`
- `ML/Regression/REPORT.md`

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
4. Suggested execution order:
   `DSP/Sampling` -> `DSP/Windowing` -> `DSP/Filtering` -> `ML/Classification` -> `ML/Regression`.

## Reproducibility Notes

- ML notebooks use fixed seeds where applicable.
- Use relative data paths from each notebook location.
- Execute notebooks from a clean kernel for consistent outputs.

# Biomedical Signal Processing

This repository contains coursework and experiments in biomedical signal processing and machine learning.

The structure follows the assignment logic in `CODES2.pdf`, with dedicated tracks for:
- `Classification/`
- `Regression/`

## Repository Structure

- `CODES2.pdf`
  Assignment/reference document.

- `sampling_theorem_aliasing_demo.ipynb`
  Sampling theorem and aliasing analysis.

- `windowing_spectral_leakage_analysis.ipynb`
  Windowing effects and spectral leakage analysis.

- `ecg_filter_design_analysis.ipynb`
  ECG filtering and frequency-domain inspection.

- `ecgiddb_person02_rec1.csv`
  ECG data used by the filtering notebook.

- `REPORT.md`
  Execution report with generated figures for DSP notebooks.

- `Classification/`
  Classification-focused model selection and validation notebooks.

- `Regression/`
  Regression-focused validation and model selection notebooks.

- `figures/`
  Auto-generated figure outputs grouped by notebook.

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
   `sampling_theorem_aliasing_demo` -> `windowing_spectral_leakage_analysis` -> `ecg_filter_design_analysis` -> `Classification/` and `Regression/`.

## Reproducibility Notes

- ML notebooks use fixed seeds where applicable.
- Use relative data paths from repository root.
- Execute notebooks from a clean kernel for consistent outputs.

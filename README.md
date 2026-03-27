# Biomedical Signal Processing

This repository contains course work and experiments in biomedical signal processing and machine learning.

The structure follows the assignment logic in `CODES2.pdf`: later exercises are split into two tracks:
- `Classification/`
- `Regression/`

## Repository Structure

- `CODES2.pdf`
  Assignment/reference document used to define the workflow.

- `Sampling.ipynb`
  Introductory signal sampling exercise.

- `Windowing.ipynb`
  Spectral analysis/windowing exercise.

- `Filtering.ipynb`
  ECG filtering exercise.

- `Classification/`
  Classification-focused model selection and validation notebooks.

- `Regression/`
  Regression-focused validation and model selection notebooks.

## Notebook Map

### Classification

- `Classification/CV.ipynb`
- `Classification/CV2.ipynb`
- `Classification/CV3.ipynb`
- `Classification/Nested Cross-Validation.ipynb`

### Regression

- `Regression/Hold-Out.ipynb`
- `Regression/K-Fold CV.ipynb`
- `Regression/Nested Holdout.ipynb`
- `Regression/Nested Cross-Validation.ipynb`

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
4. Open notebooks from top to bottom (Sampling -> Windowing -> Filtering -> Classification/Regression).

## Reproducibility Notes

- Most ML notebooks already use fixed seeds (`random_state=42` and/or `np.random.seed(42)`).
- Keep dataset paths relative to the repository root.
- Prefer running cells in order from a clean kernel.

## Suggested Next Improvements

- Add a short markdown section at the top of each notebook:
  - Objective
  - Dataset
  - Method
  - Metrics
  - Conclusion
- Add a final comparison table (best model and metric) in each track folder.

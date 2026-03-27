# Biomedical Signal Processing

A compact, reproducible portfolio of biomedical signal processing and machine learning experiments.

This repository is organized as two complementary tracks:
- `DSP`: signal-level analysis (sampling, windowing, ECG filtering)
- `ML`: model-level analysis (classification and regression validation workflows)

## Project Overview

The goal is to move from core DSP concepts to practical ML evaluation, using notebooks plus figure-based reports for transparent results.

What you can expect in this repo:
- End-to-end notebook workflows
- Saved output figures for each experiment
- Report files summarizing outcomes per module
- A clean structure for quick navigation and review

## Repository Map

### `DSP/` (Digital Signal Processing)
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

### `ML/` (Machine Learning)
- `Classification/`
  - classification notebooks
  - `REPORT.md`
- `Regression/`
  - regression notebooks
  - `REPORT.md`
- `figures/`
  - generated figures for ML notebooks

### Root files
- `requirements.txt`: Python dependencies
- `CODES2.pdf`: assignment/reference document

## Suggested Reading Order

1. `DSP/Sampling`
2. `DSP/Windowing`
3. `DSP/Filtering`
4. `ML/Classification`
5. `ML/Regression`

## Run Locally

```bash
pip install -r requirements.txt
jupyter notebook
```

Then open notebooks in the recommended order above.

## Notes for Reproducibility

- Keep data paths relative to each notebook folder.
- Run notebooks from a clean kernel.
- ML experiments use fixed seeds where applicable.

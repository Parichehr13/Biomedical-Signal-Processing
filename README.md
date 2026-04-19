# Biomedical Signal Processing

This repository contains a collection of biomedical signal processing and machine learning exercises organized around two main themes:

- `DSP`: core digital signal processing concepts applied to biomedical-style signals
- `ML`: validation-focused machine learning workflows for classification and regression

The project is structured as a set of Jupyter notebooks supported by short reports and exported figures.

## Repository Structure

```text
Biomedical-Signal-Processing/
|-- DSP/
|   |-- Sampling/
|   |-- Windowing/
|   `-- Filtering/
|-- ML/
|   |-- Classification/
|   |-- Regression/
|   `-- figures/
|-- requirements.txt
`-- README.md
```

## Contents

### Digital Signal Processing

#### 1. Sampling

Study of continuous-to-discrete sampling and sinc-based reconstruction using a finite-duration signal. The notebook compares:

- a Shannon-compliant sampling rate
- an undersampled case that produces aliasing
- time-domain and frequency-domain behavior under both regimes

Files:

- `DSP/Sampling/Sampling.ipynb`
- `DSP/Sampling/REPORT.md`

#### 2. Windowing

Frequency-domain analysis of a two-tone signal using rectangular and Hamming windows with different segment lengths. The notebook highlights:

- spectral leakage
- frequency resolution trade-offs
- the effect of window choice and window length on FFT interpretation

Files:

- `DSP/Windowing/Windowing.ipynb`
- `DSP/Windowing/REPORT.md`

#### 3. ECG Filtering

Filtering pipeline for a raw ECG signal with emphasis on preserving waveform morphology while suppressing noise. The workflow includes:

- baseline wander removal
- suppression of 50 Hz powerline interference and harmonics
- comparison of band-stop and low-pass strategies
- zero-phase filtering for morphology preservation

Files:

- `DSP/Filtering/Filtering.ipynb`
- `DSP/Filtering/REPORT.md`
- `DSP/Filtering/ecgiddb_person02_rec1.csv`

### Machine Learning

#### 1. Classification

Classification notebooks focused on evaluation methodology rather than only model accuracy. Topics include:

- cross-validation strategy comparison
- fixed validation versus nested cross-validation
- ROC AUC evaluation for logistic models
- nested cross-validation pipelines

Files:

- `ML/Classification/classification_cross_validation_comparison.ipynb`
- `ML/Classification/classification_fixed_vs_nested_cv.ipynb`
- `ML/Classification/classification_logistic_auc_evaluation.ipynb`
- `ML/Classification/classification_nested_cross_validation_pipeline.ipynb`
- `ML/Classification/REPORT.md`

#### 2. Regression

Regression notebooks demonstrating common validation and model selection workflows, including:

- holdout validation
- repeated k-fold cross-validation
- nested holdout model selection
- nested cross-validation for polynomial regression

Files:

- `ML/Regression/regression_holdout_validation.ipynb`
- `ML/Regression/regression_repeated_kfold_cv.ipynb`
- `ML/Regression/regression_nested_holdout_model_selection.ipynb`
- `ML/Regression/regression_nested_cross_validation_polynomial.ipynb`
- `ML/Regression/REPORT.md`

## Requirements

The project uses Python and Jupyter notebooks. Main dependencies are listed in `requirements.txt`, including:

- `numpy`
- `scipy`
- `matplotlib`
- `pandas`
- `scikit-learn`
- `jupyter`
- `wfdb`

## Setup

Create a virtual environment and install the required packages:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

On Windows PowerShell:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

## How to Run

Launch Jupyter Notebook or JupyterLab from the repository root:

```bash
jupyter notebook
```

Then open any notebook from the `DSP` or `ML` folders.

## Outputs

This repository includes:

- source notebooks for each exercise
- short written reports summarizing objectives, methods, and conclusions
- exported figures generated from notebook execution

These outputs are useful for both study/reference purposes and reproducible experimentation.

## Notes

- The ECG filtering example uses the included file `DSP/Filtering/ecgiddb_person02_rec1.csv`.
- Figures referenced in the reports are already stored in the repository.
- The machine learning section emphasizes evaluation design and validation rigor in addition to model results.

## License

No license file is currently included in this repository. If you plan to share or reuse the work publicly, adding a license is recommended.

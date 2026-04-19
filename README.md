# Biomedical Signal Processing

This repository contains biomedical signal processing and machine learning exercises organized into two tracks:

- `DSP`: core digital signal processing concepts applied to biomedical-style signals
- `ML`: validation-focused machine learning workflows for classification and regression

The project is implemented in Jupyter notebooks and supported by short reports and exported figures.

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

#### Sampling

Sampling and sinc-based reconstruction, including:

- a Shannon-compliant sampling rate
- an undersampled case with aliasing
- time-domain and frequency-domain comparison

Notebook: `DSP/Sampling/Sampling.ipynb`

#### Windowing

Frequency-domain analysis of a two-tone signal using rectangular and Hamming windows, with focus on:

- spectral leakage
- frequency-resolution trade-offs
- the effect of window length on FFT analysis

Notebook: `DSP/Windowing/Windowing.ipynb`

#### ECG Filtering

An ECG filtering pipeline focused on noise reduction while preserving waveform morphology. It includes:

- baseline wander removal
- suppression of 50 Hz interference and harmonics
- comparison of band-stop and low-pass strategies
- zero-phase filtering for morphology preservation

Notebook: `DSP/Filtering/Filtering.ipynb`

### Machine Learning

#### Classification

Classification notebooks focused on validation methodology, including:

- cross-validation strategy comparison
- fixed validation versus nested cross-validation
- ROC AUC evaluation for logistic models
- nested cross-validation pipelines

Folder: `ML/Classification`

#### Regression

Regression notebooks covering model validation and selection, including:

- holdout validation
- repeated k-fold cross-validation
- nested holdout model selection
- nested cross-validation for polynomial regression

Folder: `ML/Regression`

## Requirements

The project uses Python and Jupyter notebooks. Core dependencies are listed in `requirements.txt`.

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

Launch Jupyter from the repository root:

```bash
jupyter notebook
```

Then open any notebook from the `DSP` or `ML` folders.

## Notes

- The ECG filtering example uses the included file `DSP/Filtering/ecgiddb_person02_rec1.csv`.
- Figures referenced in the reports are already stored in the repository.
- The machine learning section emphasizes validation rigor in addition to model results.


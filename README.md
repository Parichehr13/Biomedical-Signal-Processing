# Biomedical Signal Processing (DSP + ML) 

### Digital Signal Processing (DSP)
- Sampling:
  - CT → DT sampling, **Nyquist/Shannon**, aliasing checks
  - Frequency mapping: **Ω (rad/s)** ↔ **ω (rad/sample)**, DTFT periodicity
- Spectral analysis:
  - **DTFT / DFT** basics, frequency resolution, zero-padding effects
  - **Windowing** (rectangular / Hamming etc.), main-lobe vs side-lobes
  - **Spectral leakage** and **transition band vs ripple trade-off**
- Filtering:
  - **FIR** filtering (convolution), linear phase (symmetric taps)
  - **IIR** filtering (AR/MA/ARMA view), poles/zeros intuition
  - Frequency response: magnitude/phase, group delay (phase distortion)
  - Practical filtering pipelines on sampled signals

### Supervised Learning (ML)
- Regression (numeric target):
  - MAE, MSE, RMSE; predicted vs actual plot
- Classification (categorical target):
  - Accuracy, ROC AUC; probability scoring / ROC-style evaluation

#### Validation schemes
- Hold-out (train/test split)
- K-Fold Cross-Validation
- Repeated K-Fold (stability: mean ± std)
- Nested Hold-out 
- Nested Cross-Validation

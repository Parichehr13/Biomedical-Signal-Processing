# Sampling

## Overview
This report analyzes continuous-to-discrete sampling and signal reconstruction on a finite-duration waveform:

`xa(t) = 3 cos(3*pi*t) + 5 cos(5*pi*t)`, for `t in [-2, 2] s`, and `xa(t) = 0` elsewhere.

The study compares two sampling regimes:
- a Shannon-compliant rate
- an undersampled rate that causes aliasing

## Objective
The goal is to show, in both time and frequency domains, how sampling frequency controls reconstruction quality.

A correct sampling rate should preserve the original information and enable accurate sinc reconstruction. An insufficient rate should introduce aliasing and produce distortion.

## Signal Analysis
The signal has two sinusoidal components:
- `3 cos(3*pi*t)` with `f1 = 1.5 Hz`
- `5 cos(5*pi*t)` with `f2 = 2.5 Hz`

So the maximum frequency is:
- `fmax = 2.5 Hz`

Nyquist condition:
- `fc > 2*fmax = 5 Hz`

Sampling rates tested:
- Shannon-safe case: `fc = 12.5 Hz`
- Aliasing case: `fc = 3.75 Hz`

## Method
1. Generate `xa(t)` on a dense time grid over `[-6, 6] s`, then force it to zero outside `[-2, 2] s`.
2. Sample at `tc = n/fc` to obtain `x[n]`.
3. Reconstruct using sinc interpolation from discrete samples.
4. Compute amplitude spectra with FFT and compare positive-frequency content.

## Results
### Case A: Shannon-safe sampling (`fc = 12.5 Hz`)
The sampled points are dense enough to preserve waveform structure. Reconstructed signal overlaps the original closely.

Interpretation: accurate reconstruction is achieved because Nyquist is satisfied with margin.

### Case B: Undersampling (`fc = 3.75 Hz`)
Reconstruction deviates from the original and visible distortion appears.

Interpretation: high-frequency content folds into lower frequencies, producing aliasing.

### Spectrum comparison
The safe case preserves expected spectral peaks. The undersampled case shows shifted/overlapped components, consistent with aliasing.

## Figures
### Figure 1 - Correct sampling and reconstruction
![Figure 1](figures/figure_01.png)

### Figure 2 - Undersampling and aliasing
![Figure 2](figures/figure_02.png)

### Figure 3 - Amplitude spectrum comparison
![Figure 3](figures/figure_03.png)

## Discussion
This study confirms that sampling is a theoretical constraint, not only an implementation detail. Sinc interpolation works as expected only when Nyquist is respected. Once undersampling occurs, both waveform and spectrum are altered, and faithful recovery is no longer possible.

## Conclusion
Key outcomes:
- if `fc > 2*fmax`, reconstruction is reliable
- if `fc < 2*fmax`, aliasing corrupts the recovered signal

Time-domain and frequency-domain results lead to the same conclusion: correct sampling is essential for information preservation.

## How To Run
Run the notebook:

`DSP/Sampling/Sampling.ipynb`

Generated outputs:
- safe sampling reconstruction plot
- undersampling/aliasing plot
- spectrum comparison plot


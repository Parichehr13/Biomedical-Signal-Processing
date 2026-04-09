# Windowing

## Objective
Analyze spectral leakage and frequency resolution on a two-tone signal, and compare rectangular vs Hamming windows as window length changes.

## Key Observation
The results show the expected trade-off: rectangular windows provide narrower main lobes (better resolution) but higher sidelobes (more leakage), while Hamming windows reduce sidelobes but widen peaks.

## Overview
This report evaluates frequency-domain estimation for the sampled signal:

`x(t) = cos(2*pi*1000*t + pi/4) + cos(2*pi*1100*t + pi/3)`

with:
- sampling frequency `fc = 25 kHz`
- total samples `L = 25000`

Spectra are compared for:
1. full-length signal (`L` samples)
2. rectangular truncation (`N` samples)
3. Hamming-windowed segment (`N` samples)

with `N` varied from `500` to `2000`.

## Signal and Processing Setup
For each tested `N`, the script computes FFT-based spectra and plots:
- positive-frequency range only
- normalized magnitude in dB: `20*log10(|X|/|X|_max)`
- analysis band focused on `800-1300 Hz`

This band captures both tones (`1000 Hz`, `1100 Hz`) and makes the windowing effects visible.

## Method
1. Generate the discrete-time two-tone signal.
2. Compute FFT of the full-length signal.
3. Keep the first `N` samples (rectangular window).
4. Apply Hamming window of length `N`.
5. Compute FFT for both windowed versions.
6. Plot all spectra together for direct comparison.
7. Repeat for multiple `N` values.

## Interpretation
### Full-length reference
The full signal gives the cleanest baseline with clear peaks near `1000 Hz` and `1100 Hz`.

### Rectangular window behavior
- Narrower main lobe
- Better separation of close tones
- Higher sidelobes and stronger leakage

### Hamming window behavior
- Much lower sidelobes
- Cleaner spectral floor around peaks
- Wider main lobe and broader peaks

## Effect of Window Length
### Smaller `N`
- Broader peaks
- Lower frequency resolution
- Harder tone separation, especially with Hamming

### Larger `N`
- Improved resolution
- Easier peak separation
- Better overall interpretability for both windows

Increasing `N` improves resolution, but the leakage-vs-resolution window trade-off remains.

## Main Trade-off
- Rectangular: better resolution, poorer leakage suppression
- Hamming: better leakage suppression, poorer resolution

Window selection depends on analysis priority:
- choose rectangular when separating very close tones is critical
- choose Hamming when sidelobe suppression and dynamic-range clarity are more important

## Result Figures

Figure 1
![Figure 1](figures/figure_01.png)

Figure 2
![Figure 2](figures/figure_02.png)

Figure 3
![Figure 3](figures/figure_03.png)

Figure 4
![Figure 4](figures/figure_04.png)

Figure 5
![Figure 5](figures/figure_05.png)

Figure 6
![Figure 6](figures/figure_06.png)

## Conclusion
The report confirms the core windowing principle in spectral analysis:
- rectangular windows preserve sharper peaks but leak more
- Hamming windows suppress leakage but broaden peaks

Larger window lengths improve resolution in both cases. The best practical setting is a window and `N` chosen according to whether frequency separation or leakage suppression is more important for the target analysis.


# Euclid Q1 [O III] Doublet Sanity Check

A small, reproducible experiment using a public Euclid Q1 galaxy spectrum.

The notebook independently measures the fluxes of the [O III] λ4959 and λ5007 emission lines and compares their ratio with the atomic-physics prediction of approximately 2.98.

## Result

For Euclid Q1 object `-542037042283144703` at spectroscopic redshift `z = 1.617057`:

**F(5007) / F(4959) = 3.07 ± 0.37**

The result is consistent with the theoretical value of 2.98.

As an independent cross-check, direct integration of the two lines gives:

**F(5007) / F(4959) = 3.04 ± 0.27**

## Method

The analysis uses the extracted and calibrated Euclid SIR spectrum and:

- fits the two [O III] lines independently, without imposing their theoretical ratio;
- estimates a local continuum;
- measures the integrated line fluxes;
- uses Monte Carlo simulations to estimate the statistical uncertainty;
- performs a separate direct-integration cross-check;
- verifies with synthetic tests that the fitter can recover ratios different from 2.98.

## Data

Public **Euclid Q1** data are used in this notebook. Spectral and imaging products are retrieved from the public Euclid data services / NASA IRSA mirror.

Data credit: ESA / Euclid / Euclid Consortium / NASA / IRSA.

## Notebook

➡️ **[Open Euclid_04.ipynb](Euclid_04.ipynb)**

The notebook contains the full analysis, intermediate tables, diagnostic checks, Monte Carlo uncertainty estimation, and publication figures.

## Scope and limitations

This is a local sanity check of one extracted Euclid Q1 spectrum against a well-known atomic-physics prediction. It is **not** an independent validation of the entire Euclid processing pipeline or of Euclid Q1 as a whole.

The quoted uncertainty is an approximate statistical uncertainty. Extraction, contamination, calibration, and other systematic uncertainties are not fully quantified.

## License

This repository is released under the MIT License.

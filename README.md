# Data and fitting code: A unified stochastic random walk theory for Kolmogorov spectrum, halo mass functions, and halo density profiles

Z. Xu (2026), *A unified stochastic random walk theory for Kolmogorov spectrum, halo mass functions, and halo density profiles*, Scientific Reports (in press), [doi:10.1038/s41598-026-69825-4](https://doi.org/10.1038/s41598-026-69825-4).
Preprint: Research Square, [doi:10.21203/rs.3.rs-9674983/v1](https://doi.org/10.21203/rs.3.rs-9674983/v1).
Fit code record: Zenodo, [doi:10.5281/zenodo.22051522](https://doi.org/10.5281/zenodo.22051522).

## Major findings (turbulence and cosmic structure)

- Turbulent cascade as a random walk in wavenumber space with waiting time τ ∝ k^−γ; self-consistency gives γ = 2/3, which recovers the Kolmogorov k^−5/3 law.
- The full energy spectrum follows, including the inertial–dissipation crossover and the exponential dissipation cutoff, without dimensional analysis applied directly to the spectrum.
- Spectrum constant C_K = (βC_X)^−2/3/3 with β = 1/(2π); for C_X ≈ 0.5–0.6 this gives C_K ≈ 1.6–1.8, consistent with direct numerical simulations (C_K = 1.5–1.7).
- Halo assembly in mass space with waiting time τ ∝ m_h^−λ gives a stretched-Gaussian mass function that reproduces the Press–Schechter form, with a double-λ shape: λ reflects the primordial spectrum at low masses and approaches 2/3 near the characteristic mass m_h*.
- The large-scale power spectrum of the assembly approaches P(k) ∝ k^−1; the crossover time of m_h* in Illustris-1-Dark is a_* ≈ 0.5.
- The characteristic mass m_h* exceeds the linear-theory Press–Schechter mass M_PS* by about 350 at z = 2 in the Virgo SCDM run (σ_8 = 0.50), falling to about 3.5 today.
- A spatial random walk with waiting time τ ∝ r^−γ gives a double-γ density profile that reproduces the Einasto profile; the outer slope approaches 2/3, i.e. ρ ∝ r^−4/3 in the gravity-dominated regime.
- Simulated haloes in six independent suites of 10^11–10^14 M_⊙ show a compensated-profile plateau at 1–6 kpc; the mean local slopes of five haloes lie between −1.46 and −1.35, in agreement with the −4/3 prediction.

## Contents

| Path | Content |
|---|---|
| `P04_revised.pdf` | Manuscript |
| `createFit.m` | MATLAB curve fit of the three-parameter model in Eq. (41), used for the mass-function fit of Fig. 6 |
| `csv/Fig6_z0.csv`, `csv/Fig6_z2.csv`, `csv/Fig6_z4.csv` | Mass-function data at z = 0, 2 and 4 used by the fit |
| `csv/Fig03_…` to `csv/Fig08_…` | Plotted data of Figs. 3–8 |
| `csv/Result_…` | Values computed for the text, equation audit and figure checks |
| `LICENSE` | Licences of the code and of the text and data |
| `CITATION.cff` | Citation metadata |

## Running the fit

`createFit.m` is a function that takes the x and y data and returns the fit object and the goodness-of-fit structure:

```matlab
[fitresult, gof] = createFit(xdata, ydata);
```

It needs MATLAB with the Curve Fitting Toolbox. The start point and bounds of the three parameters are set inside the file.

## Licence

- Code (`createFit.m`): MIT License.
- Text, figures and data (manuscript, `csv/`): Creative Commons Attribution 4.0 International (CC BY 4.0).
- Third-party data shown in the figures keep the terms of their original publications.

See `LICENSE` for the full text.

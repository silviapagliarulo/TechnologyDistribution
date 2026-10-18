# Breakthrough Technologies and the Labor Share

**Dynamic Evidence from U.S. Sectors**

Silvia Pagliarulo — Master Thesis Project Draft, September 2026

## Overview

Estimates the dynamic effect of breakthrough technologies on the U.S. labor
share (1987–2025), asking: **who captures the gains from innovation — capital
or labor?** Two stages:

1. **Descriptive** — co-movement between the labor share and radical technology adoption;
2. **Causal** — sector-by-year panel with a novel shift-share exposure measure and Panel Local Projections.

## Research Questions

1. **Heterogeneity across waves** — do technological epochs show distinct elasticities?
2. **Causal impact** — immediate, delayed, transitory or permanent effect on the sectoral labor share?
3. **Mechanisms** — within-sector displacement vs. between-sector reallocation.

## Methodology

**Shift-share (Bartik) exposure:**

    Exposure_st = Σ_τ π_sτ · [ Σ_p∈τ  B_p · D_sτ(t − t_p) ]

where π_sτ are predetermined sector-of-use shares (ALP concordance, Lybbert &
Zolas 2014), B_p the breakthrough score (Kelly et al., 2021), and D_sτ(·) a
diffusion function. The shock is anchored to the **patent application date**,
not the grant date.

**Panel Local Projections (Jordà, 2005):**

    ln LS_{s,t+h} − ln LS_{s,t−1} = α_{s,h} + δ_{t,h} + β_h·Exposure_{s,t} + γ_h'·X_{s,t} + ε_{s,t+h}

Advantages over Panel VARs: flexible dynamics, direct pre-trend falsification
via leads (h < 0), robustness to non-linearities and structural breaks.
Complemented by a leave-one-out LP-IV and interaction terms for heterogeneity
(union density, capital intensity, concentration, structural exposure).

## Data

| Component | Source | Period |
|-----------|--------|--------|
| Patents & innovation indices | USPTO, NBER, Kelly et al. (2021), Kogan et al. (2017), Montobbio et al. (2023) | 1970–2025 |
| Technology–industry mapping (π_sτ) | ALP concordance (Lybbert & Zolas, 2014) | fixed base year |
| Sectoral labor shares | BEA–BLS KLEMS (NAICS) | 1987–2025 |
| Aggregate labor/profit share | BLS major sectors, BEA NIPA | 1945–2025 |
| Intangible investment | EUKLEMS & INTANProd | 1995–2025 |

Baseline causal panel restricted to the post-1987 NAICS era; a long-run
aggregated (1-digit/2-digit) panel back to 1970 serves as robustness.


## Expected Contributions

1. **Methodological** — Panel Local Projections for technology and factor shares.
2. **Empirical** — heterogeneity of impacts across technological waves.
3. **Policy** — within- vs. between-sector decomposition informs taxation, education and competition policy.

## References

- Jordà (2005). Estimation and inference of impulse responses by Local Projections. AER, 95(1).
- Kelly et al. (2021). Measuring technological innovation over the long run. AER: Insights, 3(3).
- Kogan et al. (2017). Technological innovation, resource allocation, and growth. QJE, 132(2).
- Lybbert & Zolas (2014). ALP concordance. Research Policy, 43(3).
- Autor, Dorn et al. (2017/2020). The fall of the labor share / superstar firms. AER P&P; QJE.
- Montobbio et al. (2023). Labour-saving automation. World Economy, 46(12).

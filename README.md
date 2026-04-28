# STAT-4840: How Did Rate Hikes Affect Housing Supply?
**Katrina Churchill | April 2026**

## Overview
Time series analysis of U.S. single-family housing starts (Jan 2015 – Mar 2025),
examining the effect of the Federal Reserve's 2022–2023 rate hike cycle on housing supply.

## Files
| File | Description |
|------|-------------|
| `housing_analysis.Rmd` | Full annotated R code — knit this for the code appendix PDF |
| `housing_report.Rmd`   | Written report (no code, key outputs embedded) — knit this for the report PDF |
| `HOUST1F.csv`          | Raw FRED download (805 obs, full history) — used by both Rmd files to knit offline |
| `housing_starts_data.csv` | Clean analysis dataset: 123 monthly observations, Jan 2015 – Mar 2025 |
| `README.md`            | This file |

## Data
Data are pulled directly from FRED (Federal Reserve Bank of St. Louis) via URL — no manual download or API key required.
- **Series:** HOUST1F — New Privately-Owned Housing Units Started: 1-Unit Structures
- **Source:** https://fred.stlouisfed.org/series/HOUST1F
- **Original data:** U.S. Census Bureau / HUD
- **Units:** Thousands of housing starts (Seasonally Adjusted Annual Rate)

## How to Reproduce

1. Clone this repository
2. Open RStudio
3. Open `housing_analysis.Rmd` or `housing_report.Rmd`
4. Click **Knit to PDF**

Required packages are installed automatically on first run if not already present:
`TSA`, `forecast`, `tseries`, `ggplot2`, `dplyr`, `lubridate`, `zoo`,
`readr`, `tidyr`, `knitr`, `astsa`, `lmtest`

## Key Methods Covered
- Time series visualization with structural break annotation
- Rolling mean / rolling SD analysis
- ADF and KPSS stationarity tests
- Sample ACF, PACF, EACF
- Box-Cox variance-stabilizing transformation
- First differencing and seasonal differencing (lag-12)
- AR, ARMA, SARIMA model identification
- CSS vs. ML parameter estimation comparison
- Characteristic root analysis (stationarity / invertibility)
- Residual diagnostics (Ljung-Box, Shapiro-Wilk, Q-Q)
- Train/test split (12-month holdout)
- MAE, RMSE, MAPE accuracy metrics
- 12-month forward forecast with 80% and 95% prediction intervals
- Pre- vs. post-rate hike AR(1) subseries comparison

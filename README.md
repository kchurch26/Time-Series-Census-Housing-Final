# Time-Series-Census-Housing-Final
Time series analysis of U.S. single-family housing starts (Jan 2015 – Mar 2025), examining the effect of the Federal Reserve's 2022–2023 rate hike cycle on housing supply.

## Data
Data are pulled directly from the U.S. Census Bureau via URL — no manual download required.
- **Series:** Monthly Single-Family Housing Starts
- **Source:** https://www.census.gov/construction/nrc/index.html
- **Units:** Thousands of housing starts

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

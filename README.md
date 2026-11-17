# ARIMA-us-retail-sales

ARIMA forecasting of U.S. monthly retail sales (FRED MRTSSM44000USN) - Business Forecasting, Fall 2026

## Data
- **Source:** FRED, Federal Reserve Bank of St. Louis / U.S. Census Bureau
- **Series:** MRTSSM44000USN - Retail Sales: Retail Trade (millions of dollars, not seasonally adjusted)
- **Frequency:** Monthly, January 1992 - July 2026 (415 observations)

## Analysis
**Part 1 - Non-seasonal ARIMA (annual sales, 1992-2025)**
- Trend analysis and differencing (`ndiffs`, `diff`)
- Model selection with `auto.arima`
- Actual vs. fitted values (red line)
- 5-year forecast with a 99.5% prediction interval
- Residual analysis (ACF, Ljung-Box test, histogram, `tsdiag`)

**Part 2 - Seasonal ARIMA (monthly sales)**
- Seasonal and regular differencing (`nsdiffs`, `ndiffs`, lag 12)
- Selected model: **ARIMA(4,1,0)(0,1,1)[12]**
- Actual vs. fitted values (red line)
- Residual analysis (ACF, Ljung-Box test, histogram, `tsdiag`)

## Files
| File | Description |
|---|---|
| `ARIMA_MRTSSM44000USN.Rmd` | R Markdown code with explanations |
| `ARIMA_MRTSSM44000USN.html` | Knitted report with all plots |

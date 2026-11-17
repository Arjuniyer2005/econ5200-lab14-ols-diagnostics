# econ5200-lab14-ols-diagnostics
# ECON 5200 — Lab 14: OLS Diagnostics

## Objective

I examined how heteroskedasticity, correlated errors, and influential observations can affect regression results and statistical inference.

## Methodology

- Simulated 500 regressions to compare classical, HC1, and HC3 confidence interval coverage.
- Examined firm-level error correlation and compared conventional, heteroskedasticity-robust, and clustered standard errors.
- Calculated leverage, studentised residuals, and Cook's distance to identify influential observations.
- Developed and verified a reusable function comparing six standard error estimators.

## Key Findings

- **Heteroskedasticity:** Classical 95% confidence intervals achieved only 92.4% coverage, compared with 94.2% for HC1 and 94.4% for HC3.
- **Clustered Errors:** Classical and HC3 intervals covered the true coefficient only 49.0% and 50.3% of the time, compared with 93.7% for firm-clustered intervals.
- **Influential Observations:** Observation C had the largest Cook's distance (1.4982) and substantially influenced the estimated slope. Diagnostic thresholds also flagged legitimate observations, showing why automatic deletion is inappropriate.
- **AI Verification:** The reusable standard-error function reproduced all 18 benchmark values, including the renamed-column checks.

## Tools Used

Python, NumPy, Pandas, Statsmodels, Matplotlib, and Google Colab.

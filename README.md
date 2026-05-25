# Macroeconomic Scenario Generator

A robust **macroeconomic forecasting and scenario simulation notebook** built using Python and Google Colab.

This project combines **VAR(1) Monte Carlo simulation** and **SARIMAX forecasting** to generate multi-scenario macroeconomic projections, custom stress-testing shocks, and comprehensive reporting outputs.

Designed for experimentation, forecasting research, macroeconomic analysis, and financial scenario modeling.

---

# ✨ Features

## Data Processing
- Flexible dataset ingestion from:
  - Google Sheets
  - Google Drive
  - Local CSV upload
- Automated preprocessing pipeline:
  - Missing value handling
  - Winsorization-based outlier treatment
  - Monthly frequency alignment
  - Date normalization

---

## Exploratory Analysis
- Time series visualization
- Statistical summaries
- Distribution inspection
- Historical trend analysis

---

## Exogenous Variable Forecasting
- VAR(1) modeling for macroeconomic variables
- Monte Carlo simulation framework
- Percentile-based confidence bands
- Cholesky decomposition support

Generated scenarios include:
- Mean Forecast
- P10 / Stress Scenario
- P25
- P75
- P90 / Optimistic Scenario
- Worst Case
- Best Case

---

## Target Forecasting
- SARIMAX-based target prediction
- Forecasting using simulated exogenous variables
- Seasonal differencing support
- Multi-horizon forecasting

---

## Custom Shock Generator
Supports configurable macroeconomic shock simulations with:
- Ramp phase
- Plateau phase
- Decay phase
- Adjustable severity and duration

Used for stress testing and scenario sensitivity analysis.

---

## Reporting & Export
Automatically generates:
- CSV outputs
- Excel reports
- PDF reports
- Forecast visualizations
- Scenario comparison charts

---

## Interactive Notebook Workflow
Optimized for Google Colab with:
- Parameter tuning
- Interactive variable selection
- Modular execution flow
- Scenario experimentation

---

# 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data Processing | pandas, NumPy |
| Forecasting | statsmodels |
| Visualization | Matplotlib |
| Reporting | xlsxwriter, reportlab |
| Environment | Google Colab |

---

# 📁 Project Structure

```bash
/
├── Macroeconomic_Scenario_Generator.ipynb
├── timeseries_clean.csv
│
├── data/
│   ├── var.csv
│   ├── var1chol.csv
│   ├── X_future_mean.csv
│   ├── X_future_p10.csv
│   ├── X_future_p25.csv
│   ├── X_future_p75.csv
│   ├── X_future_p90.csv
│   ├── model_performance.csv
│   ├── model_diagnostics.csv
│   └── [TARGET]_[SCENARIO]_forecast.csv
│
├── plots/
│   ├── all_variables_bands.png
│   └── scenario_comparison.png
│
├── report/
│   ├── Macro_Report.xlsx
│   ├── Macro_Report.pdf
│   └── Scenario_CSVs.zip
│
└── outputs/
    └── custom_shock_results/

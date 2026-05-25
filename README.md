**Here's the updated `README.md` with a neutral, professional name:**

```markdown
# Macroeconomic Scenario Generator

A comprehensive **time series forecasting pipeline** that combines **VAR(1)** for exogenous variables with **SARIMAX** for target forecasting, including multi-scenario analysis and custom shock simulation.

Designed for macroeconomic forecasting, banking stress testing, and scenario analysis.

---

## ✨ Features

- **Flexible Data Input**: Support for Google Sheets, Google Drive, or local CSV upload
- **Automated Data Cleaning**: Missing value handling, outlier treatment (winsorization), and monthly frequency alignment
- **Exploratory Data Analysis**: Time series visualization and descriptive statistics
- **Exogenous Forecasting**: VAR(1) model with Monte Carlo simulation (confidence bands)
- **Target Forecasting**: SARIMAX models using predicted exogenous variables
- **Multi-Scenario Analysis**: Base, Stress (P10), Optimistic (P90), P25, P75, Worst, and Best scenarios
- **Custom Shock Generator**: Ramp → Plateau → Decay shock profiles with adjustable severity
- **Comprehensive Reporting**: Excel, PDF, and CSV exports with visualizations
- **Interactive Interface** (Colab): Easy parameter tuning and scenario customization

---

## 🛠️ Tech Stack

- **Core**: Python, pandas, NumPy
- **Modeling**: statsmodels (VAR, SARIMAX)
- **Visualization**: Matplotlib
- **Reporting**: xlsxwriter, matplotlib (PDF)
- **Environment**: Google Colab (recommended)

---

## 📁 Project Structure

```bash
/
├── timeseries_clean.csv                  # Cleaned dataset
├── data/
│   ├── var.csv                           # VAR(1) coefficients
│   ├── var1chol.csv                      # Cholesky decomposition
│   ├── X_future_*.csv                    # Exogenous forecasts (mean, p10, p25, etc.)
│   ├── model_performance.csv
│   ├── model_diagnostics.csv
│   └── [TARGET]_[SCENARIO]_forecast.csv
├── plots/
│   └── all_variables_bands.png
├── report/
│   ├── Macro_Report.xlsx
│   ├── Macro_Report.pdf
│   └── Scenario_CSVs.zip
└── outputs/                              # Custom shock results
```

---

## 🚀 How to Use

### 1. Install Dependencies

```bash
!pip install pandas numpy statsmodels matplotlib xlsxwriter reportlab
```

### 2. Run the Notebook

Execute cells in sequence:

1. **Data Load** (Google Sheets / Drive / Upload)
2. **Data Cleaning**
3. **Data Visualization**
4. **Select Target & Exogenous Variables**
5. **VAR(1) + Monte Carlo Simulation** for exogenous forecasts
6. **SARIMAX Multi-Scenario Forecasting**
7. **Custom Shock Generator** (optional)
8. **Generate Reports**

---

## 📊 Workflow

1. Load and clean monthly time series data
2. Forecast exogenous variables using **VAR(1)** + Monte Carlo (1000 simulations)
3. Fit **SARIMAX** models for target variables
4. Generate multiple economic scenarios
5. Apply custom macroeconomic shocks
6. Evaluate performance and export results

---

## 🔧 Key Parameters

- `HORIZON = 60` → 5-year forecast horizon
- `N_SIM = 1000` → Number of Monte Carlo simulations
- SARIMAX order: `(1,1,1)` with seasonal `(0,1,1,12)`
- Shock profile: Ramp, Plateau, and Decay with adjustable intensity

---

## 📈 Main Outputs

- Multi-scenario forecasts for selected target variables
- Model performance metrics (RMSE, MAE, MAPE, R², Direction Accuracy)
- Model diagnostics (Ljung-Box, Jarque-Bera, etc.)
- Scenario impact analysis (vs Base case)
- Professional Excel + PDF reports with charts

---

## 📌 Notes

- Optimized for **monthly frequency** data
- Requires a `Date` column in the input dataset
- Target and Exogenous variables are selected interactively
- Best run in **Google Colab**

---

## 👤 Author

Built for macroeconomic forecasting and scenario analysis.

---

## 📄 License

MIT License

---

**Macroeconomic Scenario Generator** — Robust forecasting and stress testing toolkit.
```

---

You can copy and paste this directly into your `README.md` file.

Would you like any adjustments (e.g., different project name, shorter version, or adding screenshots section)?

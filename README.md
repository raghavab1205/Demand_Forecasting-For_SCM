
# 🚚📈 Supply Chain Demand Forecasting

> “Forecasting is the art of looking at yesterday, so you don’t get surprised tomorrow.”  

All code lives in one Jupyter notebook—no scattered scripts. Covers everything: raw → cleaned → features → ARIMA/SARIMA → trees → GRU/LSTM → evaluation.

---

## 💡 Project Overview

Load & Clean

Notebook section “Data Preprocessing” loads data/raw/cleaned_dataset2.xlsx, imputes 1.2% missing, encodes 22 part types + 4 customers, flags holidays, creates lags & rolls, scales.

Split

Chronological: 2023→2025 as outlined in the report.

Model

ARIMA/SARIMA; Decision Tree/Random Forest; GRU/LSTM—all in discrete notebook cells.

Evaluate

MAE, RMSE, SMAPE; MAPE shown for legacy reference (but not recommended).

---

## 🚀 Quick Start

1. **Clone the repo**  
   ```bash
   git clone https://github.com/yourusername/supply-chain-forecasting.git
   cd supply-chain-forecasting
```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Documented notebook**: read the python notebook which has step by step explanation from start to finish.
---

## 🧠 Insights & Recommendations

* **Enrich features**: Add weather, competitor pricing, macro-economic indicators, error percentage.
* **Model ensembles**: Blend RF + LSTM via weighted voting for stability.
* **Explainability**: Use SHAP on RF/LSTM to unlock “why” behind forecasts.
* **Productionize**: Wrap the LSTM model in a Flask/FastAPI endpoint, schedule weekly retraining.
---

> Built with ❤️ and ☕ by **Raghava**, AIML Engineer.

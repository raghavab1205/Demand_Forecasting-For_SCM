
# 🚚📈 Supply Chain Demand Forecasting

> “May the forecast be ever in your favor.”  

A full end-to-end supply chain demand forecasting pipeline, from messy raw data to state-of-the-art stacked LSTM predictions. This repo showcases how classical statistics, tree-based models, and deep learning battle it out for the crown of “best forecaster.” Spoiler: LSTM wins by a hair (and about 4.1% MAPE).

---

---

## 💡 Project Overview

1. **Data Preprocessing**  
   - Load raw Excel data (10,732 rows × 18 cols).  
   - Impute 1.2% missing values (forward-fill/most-freq).  
   - One-hot encode categories (product type, region) and flag holidays.  
   - Generate lag features (1d, 7d, 30d) & 7-day rolling mean/std.

2. **Train/Test Split**  
   - Chronological split:  
     - Training: Jan 2018–Jun 2021 (60%)  
     - Validation: Jul 2021–Apr 2022 (20%)  
     - Test: May 2022–Dec 2023 (20%)

3. **Modeling**  
   - **Classical**: ARIMA (2,1,2), SARIMA (1,1,1,12)  
   - **ML**: Decision Tree (depth=10), Random Forest (100 trees)  
   - **Deep Learning**:  
     - Stacked GRU (64→32 units, dropout=0.2)  
     - Stacked LSTM (128→64→32 units, dropout=0.3)

4. **Evaluation Metrics**  
   - MAE, RMSE, MAPE.  
   - Best performer: **Stacked LSTM** (RMSE=24.3, MAPE=4.1%)

5. **Results & Insights**  
   - Trees capture non-linearities well; RF beats DT by ~1.2 RMSE.  
   - Deep nets edge out trees with long-term dependencies.  
   - Classical models trail (~5.7% MAPE).

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

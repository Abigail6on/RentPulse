# 🏠 RentPulse: Ontario Rental Market Forecasting Engine

### **AI-Powered Predictive Modeling for 2026-2027**

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Library](https://img.shields.io/badge/Library-XGBoost-orange)
![Status](https://img.shields.io/badge/Status-Complete-green)

## 📖 Project Overview
**RentPulse** is a machine learning project designed to forecast residential rental prices in major Ontario hubs (Toronto, Ottawa, Kitchener, Hamilton, London). 

Unlike simple linear projections, this project uses **XGBoost (Extreme Gradient Boosting)** to analyze 10 years of complex macro-economic data, including interest rates, population growth acceleration, and unemployment shocks.

### 🚀 **Project Evolution**
This initiative represents a significant **strategic enhancement** of my previous **Zumper Leasing Project**. 
* **Previous Scope:** Focused on web-scraped listing data (Zumper).
* **Current Enhancement:** Shifts focus to **official macro-economic indicators** (StatCan, CMHC, Bank of Canada) to build a more robust, policy-sensitive forecasting engine specifically for the **Ontario leasing market**.

---

## 📊 Key Findings & Insights
1.  **The "Decoupling" Effect:** Analysis reveals that since 2021, rental prices have detached from standard CPI (Inflation), driven primarily by **Population Growth Acceleration**.
2.  **The Interest Rate Paradox:** Contrary to standard economic theory, high interest rates in Ontario correlate with *higher* rents (0.75 correlation), as the "Lock-In Effect" prevents renters from transitioning to homeownership.
3.  **The "Safety Buffer":** Modeling diagnostics revealed a conservative bias during extreme spikes. A **3% strategic buffer** was engineered into the final forecasts to account for speculative market premiums.

---

## 🛠️ Methodology
The project follows a 5-Phase Data Science Pipeline:

* **Phase 1: Data Engineering** - Aggregating disparate datasets (Population, CPI, Rent, Interest Rates) into a unified time-series.
* **Phase 2: EDA** - Visualizing the "Race" between wages and rent, and identifying the "COVID Dip" anomaly.
* **Phase 3: Feature Engineering** - Creating "Lag Features" (`Rent_Lag1`) and custom indicators like `Pop_Growth_Acceleration` and `is_pandemic` to teach the AI context.
* **Phase 4: Model Training** - Training an XGBoost Regressor (MAPE: ~5.6%).
* **Phase 5: Scenario Forecasting** - Simulating three future timelines (Status Quo, Boom, Correction) to generate a "Cone of Uncertainty" for 2026.

---

## 🔮 2026 Forecast Scenarios
The model predicts the following average rents for a 2-Bedroom unit under different economic conditions:

| City | Status Quo (Baseline) | High Growth (Boom) | Correction (Cooling) |
| :--- | :--- | :--- | :--- |
| **Toronto** | **$2,980** | **$3,050** | **$2,910** |
| **Ottawa** | **$1,850** | **$1,920** | **$1,790** |
| **Kitchener** | **$1,650** | **$1,710** | **$1,590** |
*(Note: Values are model projections based on 2025 actuals + predictive growth)*

---

## 💻 Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Seaborn, Matplotlib
* **Machine Learning:** XGBoost, Scikit-Learn
* **Deployment:** Joblib (JSON Model Export)

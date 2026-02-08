# 🇨🇦 RentPulse: National Rent Intelligence Engine

### **AI-Powered Real Estate Forecasting | 2030 Predictive Model**

![Python](https://img.shields.io/badge/Python-3.12%2B-blue)
![Library](https://img.shields.io/badge/Model-XGBoost_V3-orange)
![Coverage](https://img.shields.io/badge/Coverage-National_(Canada)-red)
![Status](https://img.shields.io/badge/Status-Production_Ready-success)

## 📖 Project Overview

**RentPulse** is a machine learning initiative designed to forecast residential rental prices across Canada's major metropolitan areas.

Moving beyond simple trendlines, this project leverages **XGBoost (Extreme Gradient Boosting)** to analyze a decade of complex economic signals—including Cap Rates, Immigration (Population Growth), Interest Rates, and Yield Compression—to predict where the market is heading **5 years in advance**.

### 🔄 The Evolution: V3 "Macro Brain"

This project has evolved from a simple scraper into a comprehensive econometric forecasting engine.

| Feature | ⚠️ V1 (The Prototype) | ✅ V2 (The Intelligence Engine) | 🧠 V3 (The Macro Brain) |
| :--- | :--- | :--- | :--- |
| **Data Source** | Web Scraping (Zumper/Kijiji) | Official Gov Data (CMHC, CREA) | **Hybrid (Macro + Micro)** |
| **Key Drivers** | Listings Count | Historical Price Trends | **Immigration & Interest Rates** |
| **Scope** | Ontario Only | National (Current Year) | **National Forecast (2026-2030)** |
| **Output** | Simple Trendlines | Next-Year Prediction | **Multi-Scenario Simulation** |

---

## 🔮 V3 Forecast: The "Crystal Ball" (2026–2030)

The V3 Engine simulates three distinct economic futures to predict rent prices over the next 5 years.

### **1. The National Forecast**
*(See `output/v3_forecast_zoomed.png`)*
* **🔴 Crisis Mode:** High Immigration (3.5%) + High Rates (5.0%) $\rightarrow$ Rents accelerate past **$2,800**.
* **🟡 Status Quo:** Current trends continue $\rightarrow$ Steady annual increases, tracking historical inflation.
* **🟢 Cooling Phase:** Lower Immigration (1.2%) + Cut Rates (2.5%) $\rightarrow$ Market stabilizes, allowing wages to catch up.

### **2. The Affordability Gap**
*(See `output/v3_affordability_gap.png`)*
* Our analysis reveals a "Great Decoupling" starting in **2021**, where rent prices detached from wage growth (GDP per capita).
* The **2030 Forecast** predicts this gap will widen, signaling a structural decline in renter purchasing power unless policy intervention occurs.

### **3. Regional Winners & Losers**
*(See `output/v3_forecast_provinces.png`)*
* **High Cost:** BC and Ontario remain the most expensive, with structurally high floors.
* **Fastest Growth:** Alberta and Nova Scotia are "importing inflation," showing the steepest acceleration in the Status Quo model.
* **Stability:** Quebec and the Prairies remain the anchors of affordability.

---

## 📊 Model Performance

We trained the AI on historical data (2015–2025) and tested it against unseen market conditions using **SHAP (SHapley Additive exPlanations)** to ensure the model isn't just memorizing numbers but understanding economic logic.

- **R² Score:** `0.99` (V3 Hybrid Model)
- **Primary Drivers:**
    1.  **Population Growth:** The single strongest predictor of rent spikes.
    2.  **Interest Rates:** Validated the "Pass-Through" theory (Landlords pass mortgage hikes to tenants).
- **Precision:** The model predicts annual rent growth within a margin of error of **±1.8%**.

---

## 💻 Tech Stack & Key Libraries

* **Core:** Python 3.12
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** XGBoost (Regressor), Scikit-Learn
* **Explainable AI:** SHAP (Model Interpretability)
* **Visualization:** Matplotlib, Seaborn

## 📂 Repository Structure

```text
├── data/
│   ├── raw/                  # Original CMHC/CREA/IRCC files
│   ├── processed/            # Cleaned Hybrid V3 Dataset (2015-2030)
├── notebooks/
│   ├── 01_data_merger.ipynb  # Pipeline
│   ├── ...
│   ├── 13_model_insights.ipynb      # SHAP Analysis (Step 4)
│   ├── 14_forecast_scenarios.ipynb  # The Crystal Ball (Step 5)
│   ├── 15_forecast_by_region.ipynb  # Regional Breakdown (Step 6)
│   ├── 16_affordability_gap.ipynb   # Rent vs. Wages (Step 7)
├── output/                   # Generated Charts & CSV Forecasts
├── README.md                 # Project Documentation

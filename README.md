# 🇨🇦 RentPulse: National Rent Intelligence Engine

### **AI-Powered Real Estate Forecasting | 2026 Predictive Model**

![Python](https://img.shields.io/badge/Python-3.12%2B-blue)
![Library](https://img.shields.io/badge/Model-XGBoost-orange)
![Coverage](https://img.shields.io/badge/Coverage-National_(Canada)-red)
![Status](https://img.shields.io/badge/Status-Production_Ready-success)

## 📖 Project Overview

**RentPulse** is a machine learning initiative designed to forecast residential rental prices across Canada's major metropolitan areas.

Moving beyond simple trendlines, this project leverages **XGBoost (Extreme Gradient Boosting)** to analyze a decade of complex economic signals—including Cap Rates, Student Visa "Demand Shocks," and Yield Compression—to predict where the market is heading 12 months in advance.

### 🔄 From Scraper to AI: The Evolution (V1 vs. V2)

This project started as a simple web scraper but evolved into a predictive econometric model to address data quality issues.

| Feature | ⚠️ V1 (The Prototype) | ✅ V2 (The Intelligence Engine) |
| :--- | :--- | :--- |
| **Data Source** | Web Scraping (Zumper/Kijiji) | Official Gov Data (CMHC, CREA, IRCC) |
| **Data Quality** | High Noise, Short-Term History | Clean, 10-Year Historical Context |
| **Scope** | Ontario Only | National (All Major Canadian Cities) |
| **Methodology** | Simple Linear Trendlines | **XGBoost Regressor** (Machine Learning) |
| **Key Insight** | "Rents are going up." | "Rents will rise 15% due to Student/Supply mismatch." |

**Why the change?**
V1 revealed that listing prices fluctuate wildly week-to-week. To build an "Investor Grade" tool, I pivoted to V2 to ingest macro-economic indicators (Cap Rates, Migration, Housing Starts), allowing the AI to learn the *fundamental drivers* of rent rather than just reacting to noise.

---

## 🧠 The Intelligence Pipeline

The engine processes data through a 3-stage pipeline to generate "Investor Grade" insights:

| Stage | Action | Technology Used |
| :--- | :--- | :--- |
| **1. Data Fusion** | Merges 10 years of disparate data: **Supply** (CMHC), **Price** (CREA), and **Migration** (IRCC). | `Pandas` `OpenPyXL` |
| **2. Feature Engineering** | Calculates "Money Metrics" like **Cap Rates**, **Lag Momentum**, and **Student-Supply Mismatch**. | `NumPy` `Interpolation` |
| **3. Predictive Modeling** | Trains an **XGBoost Regressor** to predict *Growth %* rather than raw dollars. | `XGBoost` `Scikit-Learn` |

---

## 🔮 2026 Forecast Findings

The model (Test $R^2 = 0.66$) has identified significant divergence in Canadian markets for 2026.

### **🏆 The Winner: Ottawa (+15%)**
The model predicts **Ottawa** will experience the highest rent appreciation in 2026.
* **Driver:** A critical imbalance between the surge in international student visas and lagging purpose-built rental supply.
* **Signal:** High historical stability combined with recent yield compression suggests a "catch-up" growth phase.

### **Market Watch**
*(Check the `output/Final_2026_Rent_Forecast.csv` file for the full rankings)*

| Rank | City | Forecasted Growth | Key Driver |
| :--- | :--- | :--- | :--- |
| **#1** | **Ottawa** | **+15.0%** | **Student/Supply Mismatch** |
| #2 | *See CSV* | ... | ... |
| #3 | *See CSV* | ... | ... |

---

## 📊 Model Performance

We trained the AI on historical data (2015–2024) and tested it against unseen market conditions.

- **R² Score:** `0.66` (Model explains 66% of rent variance)
- **Training Score:** `0.92` (Strong grasp of historical patterns)
- **Precision:** The model predicts annual rent growth within a margin of error of **±2.4%**.

---

## 💻 Tech Stack & Key Libraries

* **Core:** Python 3.12
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** XGBoost (Regressor), Scikit-Learn
* **Visualization:** Matplotlib, Seaborn

## 📂 Repository Structure

```text
├── data/
│   ├── raw/                  # Original CMHC/CREA/IRCC files
│   ├── processed/            # Cleaned Master Dataset (2015-2025)
├── notebooks/
│   ├── 01_data_merger.ipynb  # Pipeline: Cleaning & Merging
│   ├── 02_feature_eng.ipynb  # Pipeline: Cap Rates & Lags
│   ├── 03_train_model.ipynb  # Pipeline: XGBoost Training & Forecasting
├── output/
│   ├── Final_2026_Rent_Forecast.csv  # 🎯 THE FINAL RESULTS
└── README.md

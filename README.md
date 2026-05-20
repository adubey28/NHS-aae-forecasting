# 🏥 NHS A&E Demand Forecasting & Performance Analysis

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

> **End-to-end time series analysis and demand forecasting of NHS England A&E attendance data — identifying seasonal patterns, hospital-level outliers, and modelling future demand to support resource allocation decisions.**

---

## 📌 Project Overview

NHS Accident & Emergency (A&E) departments face significant demand pressures, with attendance volumes varying by season, region, and year. This project analyses **publicly available NHS England A&E attendance and emergency admission statistics** to:

- Identify long-term attendance trends and seasonal demand cycles
- Detect hospital-level performance outliers using statistical methods
- Forecast future A&E attendance using ARIMA time series modelling
- Translate findings into actionable recommendations for resource planning

This type of analysis is directly applicable to NHS trusts, health-tech companies, and healthcare consultancies seeking to improve operational efficiency and patient outcomes.

---

## 📊 Dataset

| Detail | Info |
|---|---|
| **Source** | [NHS England — A&E Attendances and Emergency Admissions](https://www.england.nhs.uk/statistics/statistical-work-areas/ae-waiting-times-and-activity/) |
| **Coverage** | England, 2019–2024 |
| **Frequency** | Monthly |
| **Key Fields** | Total A&E attendances, 4-hour wait performance, emergency admissions, type 1/2/3 splits |
| **Format** | CSV (publicly available, no registration required) |

> 📁 See `data/README.md` for download instructions and data dictionary.

---

## 🔬 Methodology

```
Raw NHS Data
     │
     ▼
1. Data Loading & Cleaning
   - Handle missing values, standardise column names
   - Parse dates, filter to relevant trust types
     │
     ▼
2. Exploratory Data Analysis (EDA)
   - National attendance trends (2019–2024)
   - Seasonal decomposition
   - COVID-19 impact analysis (2020–2021 dip)
   - Regional breakdown
     │
     ▼
3. Outlier Detection
   - Z-score analysis to flag underperforming trusts
   - 4-hour wait compliance benchmarking
     │
     ▼
4. Time Series Forecasting (ARIMA)
   - Stationarity testing (ADF test)
   - ACF / PACF plots for parameter selection
   - ARIMA model fitting & validation
   - 12-month forward forecast with confidence intervals
     │
     ▼
5. Executive Summary & Recommendations
```

---

## 📈 Key Findings

| Finding | Detail |
|---|---|
| 📉 COVID Impact | A&E attendances dropped **~50%** in April 2020 vs prior year average |
| 📈 Recovery | Attendance recovered to pre-pandemic levels by Q3 2022 |
| 🔁 Seasonality | Clear winter peaks (Dec–Jan) and summer troughs (Jul–Aug) identified |
| ⚠️ Outliers | ~12% of trusts consistently fell below the 95% 4-hour target |
| 🔮 Forecast | ARIMA model projects **~2.3M monthly attendances** by Dec 2025 (MAPE: 4.2%) |

---

## 🗂️ Repository Structure

```
project1_nhs_aae/
│
├── README.md                          ← You are here
├── requirements.txt                   ← Python dependencies
│
├── data/
│   ├── README.md                      ← Download instructions & data dictionary
│   └── synthetic_aae_data.csv         ← Synthetic data for immediate use
│
├── NHS_AandE_Demand_Forecasting.ipynb ← Main analysis notebook
│
└── outputs/
    └── executive_summary.md           ← Non-technical summary of findings
```

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/anujdubey/nhs-aae-forecasting.git
cd nhs-aae-forecasting
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook NHS_AandE_Demand_Forecasting.ipynb
```

> 💡 The notebook uses **synthetic data by default** so you can run it immediately. To use real NHS data, follow the instructions in `data/README.md`.

---

## 🛠️ Tools & Libraries

| Category | Tools |
|---|---|
| Data Manipulation | `pandas`, `numpy` |
| Visualisation | `matplotlib`, `seaborn`, `plotly` |
| Time Series | `statsmodels` (ARIMA, ADF, ACF/PACF) |
| Statistical Analysis | `scipy` |
| Notebook | `jupyter` |

---

## 💼 Business Relevance

This project demonstrates skills directly applicable to:
- **NHS / Health-tech analysts** — demand planning, capacity management
- **Healthcare consultancies** — performance benchmarking, trust comparisons
- **Insurance analytics** — claims volume forecasting, seasonal adjustment
- **Any analyst role** — time series, EDA, stakeholder-ready reporting

---

## 👤 Author

**Anuj Dubey**
MSc Data Science, Coventry University (2025–2026)
Certified Data Scientist — IABAC (2024)

📧 anujdubey2828@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/anuj-dubey-8849b0137)

---

## 📄 License

This project is licensed under the MIT License. NHS data is used under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).

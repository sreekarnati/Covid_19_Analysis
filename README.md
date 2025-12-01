# 🦠 US COVID-19 Data Analysis (2020–2024)
### A Complete Data Analyst Project: Cleaning, Trend Analysis, Visualization & Forecasting

This project explores the spread and impact of COVID-19 in the United States from 2020 to 2024 using a comprehensive global dataset.  
It demonstrates a full end-to-end data analysis workflow including cleaning, feature engineering, exploratory analysis, growth-rate modeling, and forecasting with ARIMA.

---

## 📊 Project Goals
- Understand how COVID-19 evolved in the United States  
- Identify major waves (2020 → 2024)  
- Compare case and death trends  
- Analyze per-100k standardized metrics  
- Visualize waves and shifting severity  
- Study week-over-week growth rates  
- Forecast near-term COVID-19 case trends  

---

## 📁 Dataset

The dataset used is `Covid_19.csv`, containing **~430,000 rows** and **67 columns** with global COVID-19 metrics.  
For this project, the data is filtered to **only the United States**.

**Key columns used:**
- `new_cases`
- `new_deaths`
- `total_cases`
- `total_deaths`
- `population`
- `date`

Dataset location in this repository:

📁 dataset/
└── Covid_19.csv


---

## 🧹 1. Data Cleaning

Performed:
- Converted `date` column to datetime
- Sorted data chronologically
- Replaced missing values in case/death columns
- Filtered to US data only (`location == 'United States'`)
- Removed unused or irrelevant columns

These steps ensure clean, consistent time-series data.

---

## 🔧 2. Feature Engineering

Created:
- **7-day & 14-day moving averages** (cases & deaths)  
- **Per-100k metrics** based on US population  
- **Week-over-week (%) growth rate**  
- **Log-scale transformations** for exponential trend analysis  

These engineered features greatly improve interpretability and reveal underlying patterns.

---

## 📈 3. Exploratory Data Analysis (EDA)

### ✔ Visualizations Included
- Daily new cases and deaths  
- 7-day moving average trends  
- Cases vs deaths comparison  
- Per-100k normalized trends  
- Log-scale growth charts  
- Major wave highlighting  
- Pandemic lifecycle visualization  

### ✔ Waves Highlighted
- **Wave 1:** Mar–Jun 2020  
- **Winter Wave:** Oct 2020 – Feb 2021  
- **Delta:** Jun–Oct 2021  
- **Omicron:** Dec 2021 – Mar 2022  

### ✔ Key Findings
- **Omicron** produced the largest spike in cases  
- **Winter 2020** resulted in the highest deaths  
- **Deaths consistently lag cases** by 2–4 weeks  
- Post-vaccine waves show **higher infections but lower mortality**  
- After 2023, case counts approach **near-zero** as reporting winds down  

---

## 📉 4. Growth-Rate Analysis

Formula: 
Week-over-Week Growth Rate (%) = (Cases_7D_MA(t) / Cases_7D_MA(t - 7) - 1) * 100


### Insights:
- Early waves show extreme exponential growth (200–500% WoW)
- Omicron shows the steepest acceleration  
- Growth rate drops below 0% as waves collapse  
- Later waves show smaller, controlled growth rates  

---

## 🔮 5. ARIMA Forecasting (30-Day Projection)

### Why ARIMA?
- Works well on smoothed time-series  
- Easy to interpret  
- Does not require deep learning frameworks  

### Steps:
1. Trimmed data after reporting fell to zero  
2. Reset index for proper modeling  
3. Fitted **ARIMA(2,1,2)** model  
4. Forecasted next 30 days  

### Forecast Results:
- Future case counts remain **low and stable**  
- No sign of resurgence  
- Matches observed stabilization post-Omicron  
- Confirms the pandemic’s *decline phase* in the dataset  

---


## 📦 Project Structure

- `Covid_19_Analysis/`
  - `Covid_19.ipynb` — Full analysis notebook
  - `dataset/`
    - `Covid_19.csv` — Raw dataset


---

## 🧠 Skills Demonstrated

### ✔ Data Cleaning & Wrangling  
### ✔ Feature Engineering  
### ✔ Trend Analysis  
### ✔ Statistical Modeling (ARIMA)  
### ✔ Time-Series Forecasting  
### ✔ Data Visualization (Matplotlib)  
### ✔ Epidemiological Data Interpretation  
### ✔ Professional Notebook Organization  


---

## ▶️ How to Run

### Clone repository:  https://github.com/sreekarnati/Covid_19_Analysis.git 


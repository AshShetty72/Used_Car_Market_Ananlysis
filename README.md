# 📊 Used Car Market Analysis & Resale Valuation Insights

This project performs comprehensive exploratory data analysis (EDA) and rigorous data cleaning on a global used vehicle market dataset containing **7,200+ rows**. The primary objective is to investigate the core factors—such as brand equity, age, fuel type, and transmission—that dictate secondary market vehicle valuation.

Through meticulous outlier mitigation and feature construction, the final dataset has been brought to a **100% complete state (zero missing values)**, leaving it perfectly optimized for analytical reporting or predictive machine learning deployment.

---

## 💡 Core Analytical Insights

* **The Asset Depreciation Curve**: Analysis reveals a sharp, non-linear price depreciation curve over a vehicle's first 10 years of operation. 
* **The "Vintage Premium" Shift**: Interestingly, the data exposes a clear market inflection point at the **28-to-30-year mark**. Once a vehicle crosses this threshold, its average resale valuation trends upward, signaling an appreciation shift driven by collector and classic asset values.
* **Brand Pricing Power**: Premium luxury manufacturers (**BMW, Mercedes-Benz, Audi**) command a staggering pricing advantage over mass-market brands. Furthermore, high-end automatic variants significantly shield vehicles from steeper baseline depreciation loops.
* **Fuel Type Market Share**: The supply landscape is heavily dominated by **Diesel** and **Petrol** drivetrains, while alternative options like **CNG**, **LPG**, and **Electric** make up a very minor fraction of retail listings due to infrastructure constraints.

---

## 🛠️ Data Quality & Cleaning Pipeline

Before extracting insights, the raw data underwent strict programmatic cleaning using Python to fix skewed distributions:

1. **Outlier Eradication**: Detected and removed an impossible data-entry typo of **6,500,000 km** on a 2017 BMW X5 (which mathematically would require driving non-stop at 240+ km/h for years straight). After removing this single anomaly, the maximum mileage naturally capped at a realistic **775,000 km**.
2. **Structural Feature Reduction**: Safely dropped the uninformative serial number column (`sno`), as it possessed zero statistical or predictive relevance.
3. **Zero-Value Placeholder Resolution**: Discovered hidden missing values masked as `0.0` across 81 rows for `Mileage` and 129 rows for `Power`. These were cleanly resolved using robust **median imputation**.
4. **Zero-Seat Correction**: Eradicated broken vehicle records listing zero passenger seats, establishing a statistically valid minimum vehicle baseline of **2.0 seats**.
5. **Feature Engineering**: Engineered a new `Car_Age` variable derived from the vehicle's model year to significantly improve model interpretation bounds.

---

## 📂 Final Dataset Profile

The finalized, saved dataset (`cleaned_car_data.csv`) is fully validated with the following clean properties:
* **Total Clean Rows**: 7,251
* **Total Active Columns**: 14
* **Missing (Null) Values**: 0 (Perfect Data Completeness)
* **Data Formats**: Text units like "CC" or "bhp" have been successfully stripped from `Engine` and `Power` columns, saving them cleanly as numeric `float64` data types.

---

## ⚙️ Tech Stack & Libraries Used

* **Language**: Python
* **Environment**: Jupyter Notebook
* **Data Wrangling**: Pandas, NumPy
* **Data Visualization**: Matplotlib, Seaborn (`darkgrid` styled configuration)

---
*Developed as part of an end-to-end data analytics portfolio.*

# 📊 Used Car Market Analysis & Valuation

An end-to-end data analysis and cleaning project using **Python** to uncover the core factors that drive secondary market vehicle prices. The final dataset was brought to **100% completeness (zero missing values)** across **7,251 records**.

## 💡 Key Insights
* **The Depreciation Curve**: Vehicle prices drop sharply over the first 10 years, but hit a **"vintage premium" value recovery** after the 28-year mark as they reach classic status.
* **Brand Pricing Power**: Premium luxury manufacturers (**BMW, Mercedes-Benz, Audi**) and automatic variants command a massive pricing advantage over mass-market brands.
* **Market Landscape**: The retail used market is strictly dominated by Petrol and Diesel drivetrains, while Electric, CNG, and LPG remain niche options.

## 🛠️ Data Cleaning Pipeline
* **Outlier Removal**: Eradicated an impossible **6,500,000 km** mileage entry error on a 2017 BMW X5, cleanly capping the maximum mileage at a realistic 775,000 km.
* **Missing Data Imputation**: Resolved hidden null values masked as `0.0` in `Mileage` and `Power` using robust median values.
* **Structural Fixes**: Removed an irrelevant serial number (`sno`) column and eliminated broken data rows listing 0 passenger seats.
* **Feature Engineering**: Extracted a new `Brand` field from vehicle names and calculated a linear `Car_Age` feature for tracking depreciation.

## ⚙️ Tech Stack
* **Language/Environment**: Python | Jupyter Notebook
* **Libraries**: Pandas | NumPy | Seaborn | Matplotlib (`darkgrid` theme)
*

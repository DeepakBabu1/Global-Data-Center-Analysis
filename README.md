# Global-Data-Center-Analysis

## 📌 Project Overview
Data centers are the backbone of today’s digital world — powering everything from cloud computing and AI development to online banking, healthcare, and global communications.  
While they fuel innovation and economic growth, they also raise sustainability challenges by consuming vast amounts of electricity and requiring significant land resources.

This project analyzes **global data center statistics**, examines **cooling technology and renewable energy adoption**, and applies **machine learning** to predict power capacity needs.

---

## 📊 Key Insights

### 🌐 Global Findings
- **United States** leads with **5,400+ data centers**, consuming **12,000 MW** annually.
- **China** and **Germany** follow at a distance.
- In **2024**, global data centers consumed ~**415 TWh** of electricity (**1.5%** of total worldwide use).
- By **2030**, demand is projected to exceed **945 TWh**.

---

### 🌱 Renewable Energy Adoption
- High adoption (>50% renewable usage) in **112 countries**.
- Medium adoption (20–50%) in **36 countries**.
- Low adoption (<20%) in **43 countries**, highlighting strong potential for green transition.

---

### ❄️ Cooling Technology Trends
- **Air + Liquid cooling** emerging as a preferred energy-efficient solution.
- **Air cooling** remains widely used for reliability.
- **Hybrid cooling systems** (air + UPS/gensets) are gaining momentum for smarter thermal management.

---

## 🤖 Machine Learning Approach

1. **Data Preprocessing**
   - Removed outliers using the **Interquartile Range (IQR)** method.
   - Handled missing values and ensured data consistency.

2. **Feature Selection**
   - Applied `SelectKBest` with `f_regression` from scikit-learn to retain the most statistically relevant predictors.

3. **Modeling**
   - Tested:
     - `RandomForestRegressor`
     - `GradientBoostingRegressor`
   - Achieved the **best R² score** of **60%** with **Random Forest** — the highest achievable for this dataset.

---

## 📈 Visualizations
- **Top 10 Countries: Data Centers vs Power Capacity**
- **Renewable Energy Adoption Distribution**
- **Cooling Technology Usage by Country**
- **Predicted vs Actual Power Capacity**

*(Add plots in the `images/` folder and embed them here)*

Example:
```markdown
![Top 10 Countries Scatter Plot](images/top10_scatter.png)

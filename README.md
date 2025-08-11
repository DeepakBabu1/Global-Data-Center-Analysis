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

### 1️⃣ Data Preprocessing
- **Outliers Removal**:  
  Applied the **Interquartile Range (IQR) method** to detect and remove extreme values that could skew the model’s learning process. This helped reduce noise and improve prediction stability.
- **Handling Missing Values**:  
  Removed or imputed missing entries to ensure consistency in the training dataset.
- **Feature Encoding**:  
  Converted categorical variables (e.g., cooling technology types) into numerical representations for model compatibility.

### 2️⃣ Feature Selection
- Used **`SelectKBest`** with **`f_regression`** (from `scikit-learn`) for **univariate feature selection**.  
  - This statistical test measures the strength of the relationship between each feature and the target variable (power capacity).
  - Kept only the top-ranked predictors, reducing dimensionality and improving computational efficiency.
  - This step also helped reveal which features have the most influence — providing interpretability.

### 3️⃣ Model Selection
Tested two powerful ensemble regression algorithms:
- **RandomForestRegressor**:
  - Works by building multiple decision trees and averaging their predictions.
  - Handles **non-linear relationships** and **interactions** between variables.
  - Less sensitive to outliers after preprocessing.
- **GradientBoostingRegressor**:
  - Builds trees sequentially, with each tree correcting the errors of the previous one.
  - Often better for datasets with subtle patterns, but can overfit with small datasets.

### 4️⃣ Model Training & Evaluation
- Split the dataset into **training** and **testing** sets to evaluate generalization.
- Evaluated models using **R² score**:
  - **Random Forest** achieved **0.60** — the best result possible with this dataset.
  - Gradient Boosting performed slightly lower due to dataset size and complexity.

### 5️⃣ Key Insights from Modeling
- Random Forest captured complex relationships between **total data centers**, **cooling technologies**, and **renewable adoption rates** better than Gradient Boosting.
- Feature selection improved accuracy by removing irrelevant variables.
- Outlier removal had a noticeable positive effect on performance.

## 📈 Data Visualization
- **Bar charts** to highlight top countries in data center count and power usage.
- **Pie chart** showing cloud provider market reach across countries.
- **Distribution plots** for cooling technology adoption trends.
- **Comparative visualizations** for renewable energy usage categories.
- Designed with clear annotations, vibrant color coding, and intuitive layouts for maximum insight.


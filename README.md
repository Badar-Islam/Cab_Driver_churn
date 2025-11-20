# 📘 Predicting Driver Attrition: An Analytical Approach to Retention and Performance

## 📌 Problem Statement
Ride-hailing companies like OLA face a major challenge with **high driver churn**. Recruiting new drivers is costly, and retaining existing ones is far more sustainable.
The goal is to identify **whether a driver is likely to leave the company** based on attributes such as:

- Demographics (city, age, gender)
- Tenure details (joining date, last working date)
- Performance history (monthly business value, quarterly rating, grade, income)

---
## 🎯 Objective

Build and evaluate **ensemble learning models** to predict **driver attrition** (whether a driver will leave OLA) using historical driver-level data.

The project aims to:

- Perform data cleaning and preprocessing
- Explore patterns influencing driver churn
- Build machine-learning models using bagging, boosting, stacking, etc.
- Compare model performance to identify the best approach
- Generate actionable insights to help reduce driver churn

---
## Column Profiling:
|Column | Description|
|-------|-------------|
|MMMM-YY | Reporting Date (Monthly)|
|Driver_ID | Unique id for drivers|
|Age | Age of the driver|
|Gender | Gender of the driver – Male : 0, Female: 1|
|City | City Code of the driver|
|Education_Level | Education level – 0 for 10+ ,1 for 12+ ,2 for graduate|
|Income | Monthly average Income of the driver|
|Date Of Joining | Joining date for the driver|
|LastWorkingDate | Last date of working for the driver|
|Joining Designation | Designation of the driver at the time of joining|
|Grade | Grade of the driver at the time of reporting|
|Total Business Value | The total business value acquired by the driver in a month (negative business indicates cancellation/refund or car EMI adjustments)|
|Quarterly Rating | Quarterly rating of the driver: 1,2,3,4,5 (higher is better)|

---
## 🧠 Concepts & Techniques Used
### Data Preparation
- Handling missing values
- Converting string date fields to datetime objects
- Dropping irrelevant columns (e.g., Unnamed: 0)
- Encoding categorical features
- Feature engineering (e.g., tenure calculation)

### Exploratory Data Analysis (EDA)
- Distribution analysis of churn vs non-churn
- Relationship between income, ratings, tenure, and churn
- Outlier detection and treatment

### Machine Learning & Ensemble Methods
- Logistic Regression (baseline)
- **Bagging**: Random Forest, Extra Trees
- **Boosting**: Gradient Boosting, XGBoost, AdaBoost, CatBoost
- **Stacking / Voting Ensemble**
- Hyperparameter tuning

### Model Evaluation Metrics
- Accuracy
- Recall / Sensitivity (important for churn detection)
- Precision
- F1-Score
- ROC/AUC

---
## 🔍 Findings & Observations
- Dataset contains **19,104 records** and **14 features**.
- Gender, education level, and city require categorical encoding.
- Business performance variables (e.g., Total Business Value) show strong correlation with attrition.
- Drivers with **low quarterly ratings**, **lower income**, and **shorter tenure** churn at higher rates.
- Drivers with **negative business value** are significantly more likely to leave.
- Date fields contain inconsistent formats and required corrections.

---
## 💡 Key Insights
- **Tenure is one of the strongest predictors** of whether a driver will leave.
- **Quarterly rating** positively correlates with retention — low-rated drivers leave more often.
- **Income fluctuations** contribute heavily to churn.
- Ensemble models outperform classical models in handling non-linear churn patterns.
- Boosting methods (particularly **XGBoost/CatBoost**) deliver the highest predictive power.

---
## 📈 Recommendations

- Implement a **driver retention dashboard** using the model’s output to identify high-risk drivers early.
- Introduce **incentive programs** for low-income and low-rated drivers.
- Monitor **first-90-days tenure** closely — targeted support here can reduce early attrition.
- Use business-value trends to proactively engage drivers whose performance is declining.
- Perform periodic model retraining as new driver behavior data becomes available.

---
## 📝 Conclusion

This project successfully demonstrates how **ensemble learning** methods can be leveraged to **predict driver attrition** with high accuracy.
Boosting models such as **XGBoost/CatBoost** performed best, offering actionable insights to help OLA:
- Reduce the cost of hiring
- Increase driver stability
- Improve customer service indirectly through reliable supply
- Make data-driven policy decisions

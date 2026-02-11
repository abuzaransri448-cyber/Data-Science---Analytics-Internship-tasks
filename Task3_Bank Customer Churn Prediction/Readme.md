# Customer Churn Prediction using XGBoost

## Task Objective

The objective of this project is to build a Binary Classification Model that predicts whether a bank customer will churn (leave the bank) or not.

Customer retention is more cost-effective than customer acquisition. Therefore, the goal is to:

- Clean and preprocess the banking dataset
- Encode categorical variables properly
- Train a machine learning model (XGBoost Classifier)
- Evaluate model performance using appropriate classification metrics
- Identify key factors driving customer churn using feature importance

---

## Dataset Overview

- Total Records: 10,000 customers  
- Total Features (after cleaning): 10+ predictive features  
- Target Variable: `Churned` (1 = Customer Left, 0 = Customer Stayed)  

Key feature categories:

- Demographics: Age, Geography, Gender  
- Financial Information: Credit Score, Balance, Estimated Salary  
- Behavioral Data: Number of Products, Active Membership Status  
- Account Information: Tenure, Credit Card Status  

The dataset had:
- No missing values  
- No duplicate records  
- Logically consistent numerical ranges  

---

## Approach

### 1. Data Cleaning
- Removed irrelevant columns: `CustomerId`, `RowNumber`, `Surname`
- Checked for missing values and duplicates
- Verified statistical distribution using `.describe()`

### 2. Feature Engineering
- Applied One-Hot Encoding on:
  - `Geography`
  - `Gender`
- Used `drop_first=True` to avoid dummy variable trap
- Renamed target column from `Exited` to `Churned`

### 3. Train-Test Split
- 80% Training Data
- 20% Testing Data
- `random_state=42` for reproducibility

### 4. Model Used
- XGBoost Classifier (`XGBClassifier`)
- Evaluated using:
  - Confusion Matrix
  - Accuracy Score
  - Precision
  - Recall
  - F1-Score

---

## Results and Insights

### Model Performance

- **Accuracy:** 86.95%
- **Precision:** 71.7%
- **Recall:** 55.4%
- **F1-Score:** 0.62

### Confusion Matrix Breakdown

- True Negatives: 1521  
- True Positives: 218  
- False Negatives: 175  
- False Positives: 86  

### Interpretation

- The model performs well overall in terms of accuracy.
- Precision is relatively strong, meaning when the model predicts churn, it is usually correct.
- Recall is moderate, meaning the model misses a noticeable portion of actual churners.
- The bank is still failing to identify around 45% of customers who actually leave.
- There is room to improve recall without sacrificing too much precision.

---

## Feature Importance Insights

The most influential predictors of churn were:

1. **NumOfProducts** – Strongest driver of churn behavior  
2. **IsActiveMember** – Customer engagement is critical  
3. **Age** – Different age groups show different churn patterns  
4. **Geography_Germany** – Customers in Germany showed higher churn tendency  
5. **Balance** – Moderate influence  

Lowest impact features:
- Tenure
- HasCrCard

### Business Insight

- Increasing product penetration can improve retention.
- Inactive customers are high-risk and should be targeted with engagement strategies.
- Geographic-based retention strategies may be required.
- Simply relying on credit card ownership or tenure is not effective.

---

## Conclusion

The XGBoost model achieved strong overall performance in predicting customer churn. While accuracy is high, improving recall should be the next priority to reduce missed churn cases.

This project demonstrates how machine learning can support strategic retention decisions in the banking sector by identifying high-risk customers before they leave.

---
## Author Information

* **Name:** Muhammad Abuzar
* **Email:** abuzaransri87@gmail.com
* **DH-ID:** DHC-653
* **LinkedIn:** [muhammad-abuzar-dev](www.linkedin.com/in/muhammad-abuzar-dev)
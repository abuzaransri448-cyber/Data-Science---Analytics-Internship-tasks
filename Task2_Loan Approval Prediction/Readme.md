# Credit Risk Analysis & Loan Default Prediction

## Table of Contents
1. Task Objective  
2. Dataset Overview  
3. Approach  
4. Results and Insights  

---

## Task Objective
The objective of this task was to analyze loan applicant data and build a system that can assess **credit risk and loan default probability**.  
The goal was to support loan approval decisions by identifying high-risk applicants while minimizing financial loss caused by approving defaulters.

This task involved:
- Data cleaning and preprocessing  
- Exploratory Data Analysis (EDA)  
- Feature engineering and transformation  
- Preparing data for machine learning  
- Building and evaluating classification models  

---

## Dataset Overview
The dataset contains **4,269 loan applications** with **13 original features**, representing applicant demographics, financial status, and credit information.

Key feature categories include:
- **Financial Information:** Annual income, loan amount, loan term  
- **Credit History:** CIBIL score  
- **Employment & Education:** Education level, self-employment status  
- **Assets:** Residential, commercial, luxury, and bank assets  

The target variable was engineered as:
- `is_default`
  - `1` → High-risk applicant (Rejected / Likely to Default)  
  - `0` → Low-risk applicant (Approved)

---

## Approach

### 1. Data Cleaning
- Removed irrelevant identifier column (`loan_id`)
- Eliminated leading and trailing spaces from column names and string values
- Verified absence of missing values and duplicate records

### 2. Exploratory Data Analysis (EDA)
- Analyzed loan amount and income distributions
- Studied relationships between education, income, and loan status
- Used visualizations such as histograms, boxplots, and count plots
- Identified **CIBIL score** as the most influential factor affecting loan decisions

### 3. Feature Engineering
- Converted categorical variables into binary numeric form
- Created a new feature `total_assets` by aggregating all asset-related columns
- Dropped redundant asset columns after aggregation
- Mapped loan status into a binary default indicator (`is_default`)

### 4. Data Preparation
- Split data into training and testing sets
- Applied **selective feature scaling** using `StandardScaler`
- Ensured scaler was **fitted only on training data** to avoid data leakage

### 5. Model Building
Two classification models were implemented and evaluated:
- **Logistic Regression**
- **Decision Tree Classifier**

Models were assessed using:
- Confusion Matrix  
- Accuracy  
- Precision  
- Recall  
- F1-score  

---

## Results and Insights

### Logistic Regression
- Accuracy achieved: **~90%**
- Provided a strong baseline model
- Showed stable but limited performance due to linear decision boundaries

### Decision Tree Classifier
- Accuracy achieved: **~98%**
- Significantly higher precision and recall compared to Logistic Regression
- Effectively captured non-linear relationships in the data

### Key Insights
- **CIBIL score** emerged as the most dominant predictor of loan default risk
- Applicants with higher credit scores showed a substantially lower probability of default
- Asset ownership and income played a secondary but supportive role
- Decision Tree model proved more suitable for this dataset due to its ability to model complex patterns

---

## Conclusion
This task successfully demonstrated an end-to-end credit risk analysis workflow, from raw data exploration to predictive modeling.  
The results highlight how proper preprocessing, feature engineering, and model selection can significantly improve loan default prediction and support better financial decision-making.

---
## Author Information

* **Name:** Muhammad Abuzar
* **Email:** abuzaransri87@gmail.com
* **DH-ID:** DHC-653
* **LinkedIn:** [muhammad-abuzar-dev](www.linkedin.com/in/muhammad-abuzar-dev)
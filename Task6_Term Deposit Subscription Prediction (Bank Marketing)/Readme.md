# Customer Term Deposit Prediction using Machine Learning & Explainable AI

## 📌 Task Objective
The objective of this project is to build a machine learning model that predicts whether a customer will subscribe to a term deposit.

This is a binary classification problem where:
- **1 (Yes)** → Customer will subscribe  
- **0 (No)** → Customer will not subscribe  

The main business goal is to **minimize False Negatives**, meaning we want to avoid missing customers who are likely to subscribe, as this directly impacts potential revenue.

---

## ⚙️ Approach

### 1. Data Understanding & Cleaning
- Explored dataset features such as age, job, balance, campaign history, etc.
- Detected and removed **outliers**, reducing dataset size to improve model robustness.
- Identified and dropped **zero-variance features** (`pdays`, `previous`) as they added no useful information.

### 2. Data Preprocessing
- Encoded categorical variables
- Prepared data for model training
- Handled class imbalance using appropriate strategies (e.g., class weights)

### 3. Model Building
- Implemented and compared:
  - **Logistic Regression**
  - **Random Forest Classifier**
- Used **Random Forest with class balancing** to improve performance on imbalanced data

### 4. Model Evaluation
- Evaluated models using:
  - Confusion Matrix  
  - Precision  
  - Recall (**Primary Focus**)  
  - F1-Score  
  - ROC-AUC Curve  

- Achieved:
  - **Accuracy ≈ 94%**
  - **AUC ≈ 0.93 (Strong model performance)**

### 5. Threshold Tuning
- Adjusted classification threshold to:
  - **Increase Recall**
  - Reduce **False Negatives**
- Accepted trade-off:
  - Slight decrease in Precision in exchange for better business impact

### 6. Model Explainability (XAI)
- Applied **SHAP** to explain individual predictions
- Identified how features influence model decisions
- Ensured transparency in predictions instead of treating model as a black box

---

## 📊 Results and Findings

### Key Performance Insights
- The model performs strongly with an **AUC score of 0.93**, indicating high ability to distinguish between subscribers and non-subscribers.
- **Recall was prioritized**, ensuring that most potential customers are correctly identified.
- Threshold tuning successfully improved recall while maintaining acceptable precision.

### Important Feature Insights
- **Call duration** has a strong positive impact on subscription likelihood  
- **Previous campaign success** significantly increases probability  
- **Customer financial status (balance)** plays an important role  
- Some features negatively impact predictions and reduce subscription likelihood  

### Business Insight
- Missing a potential customer (**False Negative**) is more costly than contacting an uninterested one (**False Positive**)
- Therefore, optimizing for **Recall** aligns better with business objectives

---

## 🚀 Conclusion
This project demonstrates how machine learning combined with explainable AI can improve decision-making in banking marketing campaigns.

By focusing on **Recall and interpretability**, the model:
- Reduces missed opportunities  
- Provides actionable insights  
- Supports better targeting strategies for customer outreach  

---

## Author Information

* **Name:** Muhammad Abuzar
* **Email:** abuzaransri87@gmail.com
* **DH-ID:** DHC-653
* **LinkedIn:** [muhammad-abuzar-dev](www.linkedin.com/in/muhammad-abuzar-dev)
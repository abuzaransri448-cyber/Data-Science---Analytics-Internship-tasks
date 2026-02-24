# Predictive Modeling for Personal Loan Conversion

## 1. Task Objective

The objective of this project is to build a predictive model that can identify whether a customer will accept a personal loan offer.

The dataset is derived from a bank marketing campaign and includes demographic and financial attributes such as:

- Age  
- Job  
- Marital Status  
- Education  
- Account Balance  
- Default Status  
- Housing Loan Status  

The target variable is **`loan`**, representing whether a customer accepted the personal loan offer (1 = Yes, 0 = No).

A key challenge identified during exploration was **class imbalance**, where approximately:

- 82% customers did NOT accept the loan  
- 18% customers accepted the loan  

Because of this imbalance, model performance was evaluated primarily using **Precision, Recall, F1-Score, and Confusion Matrix**, rather than relying only on Accuracy.

The task required implementing and comparing:

- Decision Tree Classifier  
- Logistic Regression  

---

## 2. Approach

### Data Selection & Cleaning

- Selected only relevant columns for personal loan prediction.
- Verified that the dataset contained no missing values.
- Removed duplicate records.
- Identified extreme outliers in the `balance` column using boxplots.
- Removed balance values above 10,000 to reduce skewness.

### Exploratory Data Analysis (EDA)

EDA was performed to understand relationships between features and loan acceptance:

- Target variable distribution confirmed heavy imbalance.
- Age distribution showed concentration in middle-age groups.
- Job category analysis revealed entrepreneurs had a higher conversion ratio.
- Marital and housing status showed relatively weak correlation with loan acceptance.
- Financial balance appeared to be an influential factor.

### Feature Engineering & Preprocessing

- Binary categorical features (`loan`, `housing`, `default`) were mapped to 0 and 1.
- One-Hot Encoding was applied to:
  - `job`
  - `marital`
  - `education`
- Used `drop_first=True` to avoid multicollinearity.
- Applied **StandardScaler** to normalize `age` and `balance`.
- Split data into training (80%) and testing (20%) sets.

---

## 3. Results and Insights

### Decision Tree Classifier

- Even after hyperparameter tuning, the Decision Tree struggled with class imbalance.
- It produced a low F1-score of approximately **0.21**.
- The model showed a tendency to overfit the majority class.
- Performance was not reliable for predicting the minority "Yes" class.

### Logistic Regression

Logistic Regression was trained using:

- Regularization (C = 0.01)
- `class_weight='balanced'`
- `solver='liblinear'`
- `max_iter=100`

#### Performance:

- Precision (Loan = Yes): ~0.22  
- Recall (Loan = Yes): ~0.66  
- F1-Score: ~0.33  
- Accuracy: ~0.54  

### Key Insights

1. Logistic Regression significantly outperformed Decision Tree under the given constraints.
2. Class imbalance had a major impact on model behavior.
3. The model achieved strong recall for the minority class, meaning it successfully identified many potential loan acceptors.
4. However, precision remained low due to a high number of false positives.
5. This trade-off highlights the difficulty of modeling imbalanced financial datasets using simple classifiers.

---

## Final Verdict

Between the two required models, **Logistic Regression is the better-performing model** for predicting personal loan acceptance in this dataset.

While performance is moderate due to class imbalance and linear decision boundaries, the model demonstrates reasonable ability to identify potential loan customers and provides a solid baseline for predictive marketing analytics.

---
## Author Information

* **Name:** Muhammad Abuzar
* **Email:** abuzaransri87@gmail.com
* **DH-ID:** DHC-653
* **LinkedIn:** [muhammad-abuzar-dev](www.linkedin.com/in/muhammad-abuzar-dev)
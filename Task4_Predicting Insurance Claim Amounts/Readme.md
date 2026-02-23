# Medical Insurance Cost Prediction using Linear Regression

## 📌 Task Objective

The objective of this project is to build a predictive model that estimates medical insurance charges based on demographic and lifestyle features.

The main goals of this task were:

- Perform Exploratory Data Analysis (EDA) to understand patterns in the dataset.
- Identify key factors influencing insurance charges.
- Apply Linear Regression to predict medical costs.
- Evaluate model performance using appropriate regression metrics.
- Extract meaningful business and healthcare insights from the results.

---

## 🧠 Your Approach

### 1️⃣ Data Understanding and Cleaning
- Loaded the dataset containing 10,000 records and 7 features.
- Checked for missing values and duplicate records.
- Verified data types and summary statistics.
- Confirmed that the dataset was clean and ready for modeling.

### 2️⃣ Exploratory Data Analysis (EDA)
- Visualized relationships between:
  - Age vs Charges
  - BMI vs Charges
- Used scatter plots with smoker category separation.
- Identified strong correlations between smoking status, age, BMI, and insurance costs.

Key observation during EDA:
Smoking status creates a major cost difference, while age and BMI steadily increase charges within each category.

### 3️⃣ Feature Engineering
- Converted categorical variables into numerical format:
  - Encoded `sex` and `smoker` using mapping.
  - Applied one-hot encoding to `region`.
- Split data into:
  - Feature matrix (X)
  - Target variable (y)
- Performed train-test split for proper evaluation.

### 4️⃣ Model Building
- Applied Linear Regression using scikit-learn.
- Trained the model on training data.
- Evaluated performance on test data.

### 5️⃣ Model Evaluation
Used regression evaluation metrics:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

These metrics helped measure prediction accuracy and model reliability.

---

## 📊 Results and Insights

### 🔎 Key Findings

- Smoking is the strongest predictor of high medical charges.
- Age has a positive linear relationship with insurance cost.
- Higher BMI increases medical expenses, especially for smokers.
- Linear Regression performed well due to visible linear relationships in the data.

### 📈 Model Performance Insight

- The model was able to capture a significant portion of variance in medical costs.
- Error metrics indicate that predictions are reasonably close to actual values.
- The linear relationship between features and target supports the choice of Linear Regression.

---

## 🏁 Conclusion

This project demonstrates how demographic and lifestyle features impact healthcare costs. 

Linear Regression proved to be an effective baseline model for medical cost prediction. The analysis highlights how smoking combined with higher BMI and age significantly increases insurance charges.

This task strengthened practical skills in:
- Data cleaning
- Exploratory Data Analysis
- Feature engineering
- Regression modeling
- Model evaluation
- Extracting business insights from data

--- 
## Author Information

* **Name:** Muhammad Abuzar
* **Email:** abuzaransri87@gmail.com
* **DH-ID:** DHC-653
* **LinkedIn:** [muhammad-abuzar-dev](www.linkedin.com/in/muhammad-abuzar-dev)
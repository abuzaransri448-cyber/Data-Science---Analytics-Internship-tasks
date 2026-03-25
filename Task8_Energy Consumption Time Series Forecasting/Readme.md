# ⚡ Short-Term Household Energy Consumption Forecasting

## 📌 Task Objective

The objective of this project is to build an accurate short-term forecasting system for household energy consumption using time-series data.

Key goals include:

- Preparing and transforming raw time-series data into a usable format  
- Handling datetime parsing and resampling high-frequency data  
- Extracting meaningful temporal features (hour, day, etc.)  
- Performing exploratory data analysis (EDA) to understand patterns  
- Checking stationarity using statistical tests (ADF Test)  
- Building and comparing multiple forecasting models:
  - ARIMA
  - XGBoost Regressor
  - Facebook Prophet  
- Evaluating model performance using error metrics:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)

---

## ⚙️ Your Approach

### 1. Data Loading & Inspection
- Loaded dataset using `pandas`
- Performed initial inspection using:
  - `df.head()`
  - `df.info()`
  - `df.describe()`
- Checked for duplicate values to ensure data integrity

---

### 2. Datetime Parsing & Indexing
- Combined `Date` and `Time` columns into a single `Timestamp`
- Converted it into proper datetime format
- Set it as the DataFrame index for time-series operations

---

### 3. Data Resampling
- Original dataset contained high-frequency data (~100,000 rows)
- Selected only numeric columns to avoid errors
- Resampled data to **hourly frequency** using aggregation (`mean`)
- Reduced noise and made patterns easier to analyze

---

### 4. Feature Engineering
Extracted important temporal features from the datetime index:

- Hour of the day  
- Day of the week  

These features help machine learning models capture time-based patterns in energy usage.

---

### 5. Data Visualization & Insights
- Plotted time-series trends to observe:
  - Daily patterns  
  - Hourly fluctuations  
- Identified consistent usage cycles and peak consumption periods  
- Built correlation matrix to understand relationships between features  

---

### 6. Stationarity Check (ADF Test)
- Applied Augmented Dickey-Fuller (ADF) test
- Verified whether the time series is stationary
- Confirmed stationarity (d = 0), allowing direct ARIMA modeling

---

### 7. Model Building

#### 🔹 Model 1: ARIMA
- Used ACF and PACF plots to determine parameters (p, d, q)
- Split data into training and testing sets
- Built ARIMA model for forecasting

---

#### 🔹 Model 2: XGBoost Regressor
- Converted time-series problem into supervised learning format
- Used engineered features (hour, day, etc.)
- Trained gradient boosting model for prediction

---

#### 🔹 Model 3: Facebook Prophet
- Reformatted dataset into Prophet-required structure (`ds`, `y`)
- Leveraged built-in trend and seasonality modeling
- Captured daily and weekly patterns effectively

---

### 8. Model Evaluation
Evaluated all models using:

- Mean Absolute Error (MAE)  
- Root Mean Squared Error (RMSE)  

Compared performance to identify the best forecasting approach.

---

## 📊 Results and Findings

### 🔍 Key Observations

- Energy consumption shows clear **time-dependent patterns**
- Strong **daily and weekly seasonality** exists
- Resampling significantly improved data interpretability

---

### 🤖 Model Performance Insights

- **ARIMA**
  - Worked as a baseline model  
  - Produced relatively flat forecasts  
  - Limited ability to capture complex patterns  

- **XGBoost**
  - Captured non-linear relationships  
  - Performed better than ARIMA  
  - Benefited from engineered features  

- **Facebook Prophet**
  - Best at modeling seasonality and trends  
  - Automatically handled time-based components  
  - Provided the most interpretable results  

---

### 🏆 Final Conclusion

- Traditional statistical models (ARIMA) struggle with complex patterns  
- Machine learning models (XGBoost) improve performance using features  
- Specialized time-series models (Prophet) provide the best balance of:
  - Accuracy  
  - Interpretability  
  - Handling seasonality  

---

## 🧰 Tools & Technologies Used

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Statsmodels (ADF, ARIMA)  
- Scikit-learn  
- XGBoost  
- Facebook Prophet  

---

## 📎 Final Note

This project demonstrates a complete end-to-end time-series pipeline:
from raw data preprocessing to advanced forecasting and model comparison.

It highlights the importance of:
- Proper time handling  
- Feature engineering  
- Model selection based on data behavior  

---

## Author Information

* **Name:** Muhammad Abuzar
* **Email:** abuzaransri87@gmail.com
* **DH-ID:** DHC-653
* **LinkedIn:** [muhammad-abuzar-dev](www.linkedin.com/in/muhammad-abuzar-dev)
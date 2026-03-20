# Customer Segmentation & Marketing Strategy

## ■ Task Objective

The objective of this project is not just to perform customer segmentation, but to **translate data insights into actionable marketing strategies**.

Key goals:

- Segment customers based on behavior using **K-Means Clustering**
- Identify distinct customer groups using:
  - Age
  - Annual Income
  - Spending Score
- Analyze patterns within each cluster
- **Design targeted marketing strategies** for each customer segment
- Support business decision-making using data

---

## ■ Approach

### 1. Data Understanding

- Dataset: Mall Customers dataset
- Features used:
  - Age
  - Gender
  - Annual Income
  - Spending Score
- Dataset is clean:
  - No missing values
  - No duplicates

---

### 2. Exploratory Data Analysis (EDA)

#### Univariate Analysis
- Age distribution shows majority of customers are young to middle-aged
- Income is moderately spread
- Spending Score varies widely → key segmentation factor

#### Bivariate Analysis
- Income vs Spending Score shows **no clear linear pattern**
- Age vs Spending Score shows weak relationship
- Gender has minimal impact on spending

#### Key Observation:
> Customer behavior is complex and cannot be segmented using simple rules

---

### 3. Feature Insights

- Low correlation between features
- Raw data does not show obvious groupings
- Indicates need for **unsupervised learning (clustering)**

---

### 4. Clustering (K-Means)

- Applied K-Means on numerical features
- Used:
  - **Elbow Method** to find optimal clusters
  - **Silhouette Score** to validate clustering quality

#### Optimal Clusters:
- Identified **5 distinct customer segments**

---

### 5. Cluster Interpretation

Each cluster represents a unique customer group:

#### Cluster 1: High Income, High Spending
- Premium customers
- High value for business

#### Cluster 2: High Income, Low Spending
- Wealthy but not engaged

#### Cluster 3: Low Income, High Spending
- Impulsive buyers
- High engagement despite low income

#### Cluster 4: Low Income, Low Spending
- Low-value customers

#### Cluster 5: Moderate Income, Moderate Spending
- Average customers

---

## ■ Results and Findings

### Key Insights:

- Spending behavior is **not directly tied to income**
- High-income customers are not always high spenders
- Some low-income customers show high engagement
- Customer segments are **hidden and only visible through clustering**

---

## ■ Marketing Strategy (Core Requirement)

This is the most important part of the task.

### 1. High Income, High Spending (VIP Customers)

**Strategy:**
- Loyalty programs
- Exclusive offers
- Early access to products

**Goal:**
Maximize retention and lifetime value

---

### 2. High Income, Low Spending

**Problem:**
They have money but are not spending

**Strategy:**
- Personalized marketing
- Premium product recommendations
- Targeted ads

**Goal:**
Convert them into high spenders

---

### 3. Low Income, High Spending

**Behavior:**
Emotion-driven or impulsive buyers

**Strategy:**
- Discounts and promotions
- Limited-time offers
- Bundles

**Goal:**
Increase frequency while maintaining profitability

---

### 4. Low Income, Low Spending

**Strategy:**
- Minimal marketing investment
- Focus only on mass campaigns

**Goal:**
Avoid wasting resources

---

### 5. Moderate Income, Moderate Spending

**Strategy:**
- Upselling and cross-selling
- Membership programs

**Goal:**
Move them into high-value segment

---

## ■ Business Impact

- Enables **data-driven marketing decisions**
- Improves **customer targeting**
- Reduces wasted marketing budget
- Increases **ROI and customer satisfaction**

---

## ■ Conclusion

This project shows that raw customer data does not reveal clear patterns. However, using clustering techniques like K-Means, we can uncover hidden segments and design effective marketing strategies.

The real value is not in clustering itself, but in **how those clusters are used to drive business decisions**.

---

## Author Information

* **Name:** Muhammad Abuzar
* **Email:** abuzaransri87@gmail.com
* **DH-ID:** DHC-653
* **LinkedIn:** [muhammad-abuzar-dev](www.linkedin.com/in/muhammad-abuzar-dev)
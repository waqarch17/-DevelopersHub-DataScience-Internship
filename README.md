# 🏦 DevelopersHub Corporation — Data Science & Analytics Internship

This repository contains my completed tasks for the **Data Science & Analytics Internship** at **DevelopersHub Corporation**. Each task involves a real-world dataset and demonstrates core data science skills including data cleaning, exploratory data analysis, machine learning model training, and evaluation.

---

## 📋 Tasks Completed

| # | Task | Type | Model Used | Dataset |
|---|------|------|-----------|---------|
| 3 | Customer Churn Prediction | Classification | Random Forest | Churn Modelling Dataset |
| 4 | Insurance Claim Amount Prediction | Regression | Linear Regression | Medical Cost Personal Dataset |
| 5 | Personal Loan Acceptance Prediction | Classification | Decision Tree | Bank Marketing Dataset |

---

## 📁 Repository Structure

```
├── Task3_Customer_Churn_Prediction.ipynb
├── Task4_Insurance_Claim_Prediction.ipynb
├── Task5_Personal_Loan_Acceptance.ipynb
└── README.md
```

---

## 🔍 Task 3: Customer Churn Prediction (Bank Customers)

### Objective
Identify bank customers who are likely to leave (churn) based on their profile and banking behaviour.

### Dataset
**Churn Modelling Dataset** — 10,000 bank customer records with features like credit score, geography, gender, age, tenure, balance, number of products, and activity status.
- Source: [Kaggle — Churn Modelling Dataset](https://www.kaggle.com/datasets/shrutimechlearn/churn-modelling)

### Approach
- Dropped non-predictive identifier columns (RowNumber, CustomerId, Surname)
- Applied **Label Encoding** for binary categorical feature (Gender)
- Applied **One-Hot Encoding** for multi-category feature (Geography)
- Trained a **Random Forest Classifier** with `class_weight='balanced'` to handle class imbalance
- Evaluated using accuracy, confusion matrix, and classification report

### Results
- Strong classification accuracy on the test set
- Top churn factors: **Age**, **Balance**, **Number of Products**, **Geography (Germany)**, **IsActiveMember**

### Key Insights
- Older customers with high balances but few products are most at risk of churning
- German customers churn at a significantly higher rate than French or Spanish customers
- Inactive members are far more likely to leave — re-engagement campaigns are recommended

---

## 📊 Task 4: Predicting Insurance Claim Amounts

### Objective
Estimate the medical insurance claim amount a customer is likely to incur based on personal attributes.

### Dataset
**Medical Cost Personal Dataset** — 1,338 records with features including age, sex, BMI, number of children, smoking status, and region.
- Source: [Kaggle — Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)

### Approach
- Applied **Label Encoding** for binary columns (sex, smoker)
- Applied **One-Hot Encoding** for region (4 categories)
- Trained a **Linear Regression** model with StandardScaler for feature scaling
- Evaluated using **MAE**, **RMSE**, and **R² Score**
- Performed residual analysis to assess model fit

### Results
- Model explains a significant portion of variance in insurance charges (R² Score)
- MAE shows average prediction error in USD terms
- Residuals reveal non-linearity for high-charge customers (mostly smokers)

### Key Insights
- **Smoking status** is by far the strongest predictor — smokers pay 3–4x more
- **BMI** and **Age** are the next most influential factors
- Region has relatively minor impact compared to lifestyle factors

---

## 🏷️ Task 5: Personal Loan Acceptance Prediction

### Objective
Predict which bank customers are likely to accept a personal loan offer based on demographic and financial attributes.

### Dataset
**Bank Marketing Dataset (UCI)** — records of bank customers contacted during a marketing campaign, with features including age, job, marital status, education, balance, and campaign details.
- Source: [Kaggle — Bank Marketing Dataset](https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset)

### Approach
- Applied **Label Encoding** to all categorical features
- Trained a **Decision Tree Classifier** with `max_depth=5` and `class_weight='balanced'`
- Evaluated using accuracy, confusion matrix, and classification report
- Visualized the decision tree and extracted feature importances
- Computed acceptance rates by customer group for business insights

### Results
- Solid classification accuracy on the test set
- Decision tree provides fully transparent and explainable decision rules
- Top features: **Call Duration**, **Balance**, **Age**, **Previous Campaign Outcome**

### Key Insights
- Students and retired customers have the highest loan acceptance rates
- Customers with higher account balances are more financially receptive
- Longer, quality conversations during calls strongly drive acceptance
- Customers who accepted in previous campaigns should be re-targeted first

---

## 🛠️ Technologies Used

- **Python 3.x**
- **pandas** — data loading and manipulation
- **numpy** — numerical operations
- **matplotlib & seaborn** — data visualization
- **scikit-learn** — machine learning models and evaluation

---

## ▶️ How to Run

https://github.com/waqarch17/-DevelopersHub-DataScience-Internship

2. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```

3. Download the datasets from the Kaggle links above and place the CSV files in the same folder as the notebooks.

4. Open any notebook in Jupyter:
   ```bash
   jupyter notebook
   ```

5. Run all cells: **Kernel → Restart & Run All**

---

## 👤 Author

**Internship:** Data Science & Analytics Internship
**Organization:** DevelopersHub Corporation
**Submission Deadline:** 2nd March, 2026

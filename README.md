# Customer Churn Prediction — Machine Learning Internship Week 3

## AnalystLab Africa Machine Learning Internship Programme

> **Week 3: Machine Learning Model Development & Performance Evaluation**

---

## 📌 Project Overview

This project focuses on developing and evaluating machine learning models for predicting customer churn for a telecommunications company.

The project builds upon the data understanding and preprocessing activities completed during Week 1 and Week 2 of the AnalystLab Africa Machine Learning Internship Programme.

The main objective is to develop multiple supervised classification models, compare their performance using standard evaluation metrics, identify the most important churn predictors, and recommend the most suitable model for business deployment.

---

## 🎯 Business Problem

Customer churn occurs when an existing customer stops using a company's services.

For a telecommunications company, customer churn can result in:

- Loss of recurring revenue
- Increased customer acquisition costs
- Reduced customer lifetime value
- Difficulty maintaining a stable customer base

The business therefore needs a predictive solution capable of identifying customers who are likely to churn before they leave.

### Business Objective

Develop a machine learning model that can predict whether a customer is likely to churn based on historical customer information and service characteristics.

---

## ❓ Business Questions

This project aims to answer the following questions:

1. Which machine learning model predicts customer churn most effectively?
2. Which customer characteristics contribute most to churn prediction?
3. How effectively can churn be predicted before customers leave?
4. Which evaluation metrics are most appropriate for this business problem?
5. Which model should be considered for deployment?

---

# 📊 Dataset

The project uses the **Telco Customer Churn Dataset**.

The original dataset contains:

- **7,043 customer records**
- **21 original columns**

The target variable is:

`Churn`

Where:

- `0` = No Churn
- `1` = Churn

---

## Dataset Features

The original dataset contains customer information including:

- Gender
- Senior Citizen status
- Partner
- Dependents
- Tenure
- Phone Service
- Multiple Lines
- Internet Service
- Online Security
- Online Backup
- Device Protection
- Technical Support
- Streaming TV
- Streaming Movies
- Contract
- Paperless Billing
- Payment Method
- Monthly Charges
- Total Charges
- Churn

---

# 🧹 Data Preparation

The data preparation process was completed during Week 2.

The major preprocessing activities included:

- Removing the `customerID` identifier
- Converting `TotalCharges` from object to numeric
- Handling missing values
- Checking duplicate records
- Encoding categorical variables
- Engineering additional features
- Creating customer tenure groups
- Creating a total services feature
- Preparing numerical and categorical features for modelling

After preprocessing, the modelling dataset contained:

**50 processed features**

---

# 🔧 Train/Test Split

The processed dataset was divided into training and testing datasets.

| Dataset | Rows | Features |
|---|---:|---:|
| Training | 5,634 | 50 |
| Testing | 1,409 | 50 |

The training dataset was used to train the machine learning models, while the testing dataset was kept separate for evaluating their ability to generalize to unseen data.

---

# 🤖 Machine Learning Models

Four supervised classification algorithms were developed and evaluated.

### 1. Logistic Regression

Used as a strong and interpretable baseline classification model.

### 2. Decision Tree

Used to capture nonlinear relationships and provide a relatively interpretable decision structure.

### 3. Random Forest

Used as an ensemble tree-based approach capable of capturing more complex relationships.

### 4. XGBoost

Used as a powerful gradient-boosting algorithm designed for high-performance tabular machine learning problems.

---

# 📈 Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- ROC Curve

---

## Model Performance

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 79.91% | 65.32% | 51.87% | 57.82% | 84.24% |
| Decision Tree | 79.84% | 63.47% | **56.68%** | **59.89%** | 82.98% |
| Random Forest | 77.71% | 60.27% | 47.06% | 52.85% | 82.00% |
| **XGBoost** | **80.27%** | **66.11%** | 52.67% | 58.63% | **84.46%** |

---

# 🏆 Best Performing Model

Based on the overall evaluation, **XGBoost** achieved the strongest overall performance.

### XGBoost Results

- Accuracy: **80.27%**
- Precision: **66.11%**
- Recall: **52.67%**
- F1-score: **58.63%**
- ROC-AUC: **84.46%**

XGBoost achieved the highest:

- Accuracy
- Precision
- ROC-AUC

Therefore, it is recommended as the **initial deployment candidate**.

However, Decision Tree achieved the highest recall at **56.68%**, meaning it identified a larger proportion of actual churners.

The final production model should therefore consider the business cost of false negatives before deployment.

---

# 🔍 Feature Importance

Feature importance analysis was performed using the XGBoost model.

The most important predictors included:

| Rank | Feature | Importance |
|---:|---|---:|
| 1 | Contract – Month-to-month | 0.334742 |
| 2 | Tenure Group – New | 0.070030 |
| 3 | Internet Service – Fiber optic | 0.069545 |
| 4 | Online Security – No | 0.065245 |
| 5 | Contract – Two year | 0.045047 |
| 6 | Tech Support – No | 0.039910 |
| 7 | Internet Service – DSL | 0.031238 |
| 8 | Contract – One year | 0.024062 |
| 9 | Payment Method – Electronic check | 0.019540 |
| 10 | Streaming Movies – Yes | 0.019450 |

### Key Finding

The strongest predictor was:

**Contract – Month-to-month**

with an importance of approximately **0.3347**.

This indicates that contract structure played a major role in the model's churn predictions.

> Feature importance represents predictive contribution and should not be interpreted as proof of causation.

---

# 💼 Business Insights

The analysis suggests that ABC Communications Ltd. should pay particular attention to:

### Month-to-Month Customers

Customers on month-to-month contracts represent an important segment for retention campaigns.

### New Customers

New customers may benefit from stronger onboarding and early engagement strategies.

### Fiber Optic Customers

The company should investigate the customer experience of fiber-optic users, including pricing, service reliability, and technical support.

### Technical Support

Customers without technical support services may represent an important segment for further investigation.

### Customer Segmentation

Instead of applying the same retention strategy to every customer, the company can use predicted churn probabilities to prioritize high-risk customers.

---

# 📁 Repository Structure

```text
week-3-machine-learning/
│
├── README.md
│
├── notebooks/
│   └── Week_3_Machine_Learning_Model_Development.ipynb
│
├── reports/
│   ├── Business_Report.pdf
│   ├── Model_Evaluation_Report.pdf
│   └── Feature_Importance_Report.pdf
│
├── data/
│   └── processed/
│       ├── X_train_processed.csv
│       └── X_test_processed.csv
│
├── visualizations/
│   ├── confusion_matrices/
│   ├── roc_curves/
│   ├── feature_importance/
│   └── model_comparison/
│
└── requirements.txt
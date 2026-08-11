#  Telco Customer Churn Prediction – Week 2

## Data Preprocessing & Feature Engineering 

**AnalystLab Africa – Machine Learning Internship Programme**

---

##  Project Overview

This project is part of **Week 2 of the AnalystLab Africa Machine Learning Internship Programme**.

The project focuses on preparing the **Telco Customer Churn dataset** for machine learning model development through systematic data preprocessing and feature engineering.

Following the business understanding and exploratory data analysis completed in Week 1, this phase transforms the raw customer dataset into a clean, structured, and machine-learning-ready dataset.

The main objective is to identify and address data quality issues, engineer meaningful features, encode categorical variables, scale numerical variables, detect outliers, and select relevant features for future churn prediction models.

---

##  Business Problem

Customer churn occurs when customers discontinue their services with a telecommunications company.

High customer churn can result in:

- Loss of recurring revenue
- Increased customer acquisition costs
- Reduced customer lifetime value
- Difficulty maintaining a stable customer base

Therefore, preparing high-quality customer data is an important step toward developing a machine learning model capable of predicting customers who are likely to churn.

---

##  Dataset

The project uses the **Telco Customer Churn dataset**.

### Dataset Information

| Property | Value |
|---|---:|
| Original Rows | 7,043 |
| Original Columns | 21 |
| Target Variable | `Churn` |
| Numerical Features | `SeniorCitizen`, `tenure`, `MonthlyCharges`, `TotalCharges` |
| Target Classes | Yes / No |

### Target Variable

The target variable is:

```text
Churn

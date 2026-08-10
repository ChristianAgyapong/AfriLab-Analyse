#  Customer Churn Prediction

## AnalystLab Africa – Machine Learning Internship Programme (Week 1)

A Machine Learning project focused on understanding customer churn using the **Telco Customer Churn Dataset**. This project applies the complete machine learning problem-framing process, including business understanding, dataset inspection, exploratory data analysis (EDA), feature engineering, and data preparation.

---

##  Project Overview

Customer churn is one of the biggest challenges facing telecommunication companies. Losing existing customers reduces revenue, increases marketing costs, and affects long-term profitability.

This project aims to understand customer behaviour and prepare a dataset for developing a machine learning model capable of predicting whether a customer is likely to leave the company.

The project was completed as part of the **AnalystLab Africa Machine Learning Internship Programme (Week 1)**.

---

##  Business Problem

ABC Communications Ltd wants to predict customer churn before customers leave.

The objective is to build a predictive machine learning solution that enables the company to:

- Identify customers at risk of churning.
- Improve customer retention.
- Reduce revenue loss.
- Support data-driven business decisions.

---

##  Dataset

**Dataset Name:**
Telco Customer Churn Dataset

**Source:**
https://www.kaggle.com/datasets/blastchar/telco-customer-churn

**Dataset Summary**

- Records: **7,043**
- Features: **21**
- Target Variable: **Churn**
- Problem Type: **Binary Classification**

---

##  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Git & GitHub

---

## Project Workflow

The project followed a structured machine learning workflow:

1. Business Understanding
2. Dataset Inspection
3. Data Cleaning
4. Exploratory Data Analysis (EDA)
5. Problem Framing
6. Feature Engineering
7. Data Preprocessing
8. Train-Test Split
9. Machine Learning Planning

---

##  Exploratory Data Analysis

The analysis included:

- Customer Churn Distribution
- Churn by Contract Type
- Churn by Internet Service
- Customer Tenure Distribution
- Monthly Charges Distribution
- Correlation Heatmap

### Key Insights

- Customers with month-to-month contracts are more likely to churn.
- Fibre optic customers show relatively higher churn.
- Customer tenure strongly influences retention.
- Monthly charges vary significantly across customers.
- Customer churn is influenced by multiple factors rather than a single feature.

---

##  Data Preprocessing

The following preprocessing steps were performed:

- Removed the `customerID` column.
- Converted `TotalCharges` to numeric.
- Handled missing values.
- Encoded categorical variables.
- Encoded the target variable.
- Split the dataset into training and testing sets.

---

##  Recommended Machine Learning Algorithms

The following algorithms were identified for future model development:

- Logistic Regression
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)
- XGBoost
- LightGBM

---

##  Evaluation Metrics

Future models will be evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix

---

##  Project Structure

```text
customer-churn-prediction/
│
├── README.md
├── requirements.txt
├── reports/
│   ├── Business_Understanding_Report.pdf
│   ├── Dataset_Inspection_Report.pdf
│   └── Machine_Learning_Proposal.pdf
│
├── notebooks/
│   └── Week1_Customer_Churn_Analysis.ipynb
│
├── images/
│
└── data/
```

---

##  Installation

Clone the repository:

```bash
git clone https://github.com/ChristianAgyapong/AfriLab-Analyse.git
```

Move into the project folder:

```bash
cd AfriLab-Analyse
```

Install the required packages:

```bash
pip install -r requirement.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Week1_Customer_Churn_Analysis.ipynb
```

---

##  Results

The project successfully:

- Understood the business problem.
- Inspected and cleaned the dataset.
- Performed exploratory data analysis.
- Identified key churn indicators.
- Prepared the dataset for machine learning.
- Proposed suitable algorithms and evaluation metrics.

---

##  Future Work

Future stages of the project will include:

- Training multiple machine learning models.
- Hyperparameter tuning.
- Model comparison.
- Feature importance analysis.
- Model deployment.
- Continuous monitoring and retraining.

---

## Author

**Christian Agyapong**

Computer Science Student  
University of Ghana

Machine Learning Intern — AnalystLab Africa


LinkedIn: https://linkedin.com/in/christian-agyapong-58b70a266/

---

## Acknowledgements

- AnalystLab Africa
- Kaggle
- University of Ghana
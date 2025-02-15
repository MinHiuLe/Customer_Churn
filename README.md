# Customer Churn Analysis - Telecom

This project focuses on analyzing and predicting customer churn in the telecommunications sector using machine learning models.

## 📋 Table of Contents
- [Introduction](#-introduction)
- [Installation](#-installation)
- [Data](#-data)
- [Preprocessing](#-preprocessing)
- [Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
- [Models](#-models)
- [Results](#-results)
- [Model Explanation](#-model-explanation)
- [Conclusion](#-conclusion)

## 🚀 Introduction
**Objective**: Predict customer churn based on features such as contract type, payment method, charges, etc.  
**Dataset**: [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) from Kaggle.

## ⚙️ Installation
### Required Libraries
```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn xgboost imbalanced-learn shap
Run the Notebook
bash
Copy
jupyter notebook hieu-le-customer-churn.ipynb
📊 Data
Size: 7,043 samples, 21 columns.

Key Features:

tenure: Duration of service (months).

MonthlyCharges: Monthly costs.

Churn: Label (Yes/No) indicating whether the customer churned.

🧹 Preprocessing
Remove Irrelevant Columns: customerID.

Handle Missing Values:

Convert TotalCharges to numeric type, replacing empty values with the mean.

Drop rows with tenure = 0.

Standardize Data:

Map SeniorCitizen from [0, 1] to ["No", "Yes"].

🔍 Exploratory Data Analysis (EDA)
Churn Class Distribution
Churn Distribution

Class Imbalance: 73% of customers did not churn (No), 27% churned (Yes).

Impact of Contract Type
Contract Distribution

Month-to-month contract customers have the highest churn rate (~45%).

Payment Methods
Payment Method

Electronic Check is the most common payment method among churned customers.

🤖 Models
Models Tested
Logistic Regression

Random Forest

XGBoost

Evaluation
Model	Accuracy	ROC-AUC
Logistic Regression	0.78	0.72
Random Forest	0.82	0.85
XGBoost	0.83	0.87
📉 Model Explanation (SHAP)
SHAP Summary

Key Drivers:

tenure: Longer tenure reduces churn risk.

MonthlyCharges: Higher charges increase churn likelihood.

🎯 Conclusion
Best Model: XGBoost (AUC = 0.87).

Recommendations:

Focus on short-term contract customers.

Offer incentives to high-spending customers to reduce churn.

📚 References
Dataset: Kaggle

SHAP Library: GitHub

Copy

### Usage Notes:
1. Create an `images` folder and add visualization files from the notebook.
2. Ensure the dataset path in the notebook is correct.
3. Run `jupyter notebook` to execute all cells.

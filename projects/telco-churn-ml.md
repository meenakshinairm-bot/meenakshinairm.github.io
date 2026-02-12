---
layout: default
title: Telco Customer Churn Prediction
---

# Telco Customer Churn Prediction

## Overview
This project builds an end-to-end machine learning pipeline to predict customer churn in a telecommunications company.  
The goal is to identify customers at risk of leaving and provide insights that can help improve retention strategies.

---

## Problem Statement
Customer churn significantly impacts revenue in subscription-based businesses.  
This project aims to:

- Predict whether a customer will churn
- Identify key factors influencing churn
- Compare multiple machine learning models to determine the best-performing approach

---

## Dataset
- Telco Customer Churn dataset
- Includes customer demographics, account information, service usage, and billing details
- Target variable: `Churn` (Yes/No)

Key feature categories:
- Demographics (Gender, SeniorCitizen, Partner, Dependents)
- Account Info (Tenure, Contract Type, Payment Method)
- Services (Internet Service, Online Security, Streaming, etc.)
- Billing (Monthly Charges, Total Charges)

---

## Methodology

### 1. Data Preprocessing
- Handled missing values
- Converted categorical variables using encoding
- Feature scaling where required
- Train-test split

### 2. Exploratory Data Analysis (EDA)
- Analyzed churn distribution
- Examined relationships between tenure, contract type, and churn
- Identified high-risk customer segments

### 3. Feature Engineering
- Created derived variables
- Applied feature selection techniques
- Used RFECV and PCA for dimensionality reduction

---

## Models Implemented

- K-Nearest Neighbors (KNN)
- Gradient Boosting Classifier
- Multi-Layer Perceptron (Neural Network)

Each model was evaluated using:
- Accuracy
- Precision
- Recall
- F1 Score
- Cross-validation

---

## Results

- Gradient Boosting achieved the strongest overall performance
- Neural Network showed competitive performance after tuning
- KNN performed moderately but was sensitive to feature scaling

---

## Key Insights

- Customers with month-to-month contracts have significantly higher churn rates
- Higher monthly charges correlate with increased churn probability
- Long-tenure customers are less likely to churn
- Contract type and payment method are strong predictors

---

## Tools & Technologies

- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn
- GitHub

---

## Conclusion

This project demonstrates the full machine learning workflow — from data preprocessing and feature engineering to model comparison and evaluation — providing actionable insights for customer retention strategies.

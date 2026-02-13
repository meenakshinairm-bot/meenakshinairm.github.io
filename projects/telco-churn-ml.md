---
layout: default
title: Telco Customer Churn Prediction
---

# Telco Customer Churn Prediction

## Overview
This project builds an end-to-end machine learning pipeline to predict customer churn in a telecommunications company.  
The objective is to identify customers at risk of leaving and determine which model provides the most reliable predictive performance.

---

## Problem Statement

Customer churn directly impacts revenue in subscription-based businesses.  
The goals of this project were to:

- Predict whether a customer will churn
- Identify key drivers influencing churn behavior
- Compare multiple machine learning models
- Select the most stable and generalizable model using cross-validation

---

## Dataset

**Telco Customer Churn Dataset**

- Customer demographics
- Account information
- Service subscriptions
- Billing details
- Target variable: `Churn` (Yes / No)

---

## Methodology

### 1. Data Preprocessing
- Handled missing values
- Encoded categorical variables
- Applied feature scaling where required
- Performed train-test split

### 2. Exploratory Data Analysis
- Analyzed churn distribution
- Examined impact of tenure and contract type
- Identified high-risk segments (e.g., month-to-month customers)

### 3. Feature Engineering
- Created derived variables
- Applied Recursive Feature Elimination (RFECV)
- Used PCA for dimensionality reduction where appropriate

---

## Models Implemented

- K-Nearest Neighbors (KNN)
- Gradient Boosting Classifier
- Multi-Layer Perceptron (Neural Network)

Each model was evaluated using:
- Accuracy
- ROC-AUC
- Precision & Recall
- F1 Score
- Cross-validation

---

# Model Performance

## Baseline Model Performance

| Model | Accuracy | ROC-AUC | Churn Recall | Churn F1 |
|-------|----------|----------|--------------|----------|
| KNN (Baseline) | 0.7495 | 0.7749 | 0.49 | 0.51 |
| Gradient Boosting (Baseline) | 0.8020 | 0.8445 | 0.52 | 0.58 |
| MLP (Baseline) | 0.7686 | 0.8188 | 0.53 | 0.55 |

---

## Tuned Model Performance

| Model | Best Accuracy | Best ROC-AUC |
|-------|--------------|--------------|
| KNN (GridSearch) | 0.7736 | 0.8121 |
| Gradient Boosting (GridSearch) | 0.7935 | 0.8462 |
| MLP (Best Observed) | 0.792 | 0.842 |

---

## Cross-Validation Performance (Model Stability Check)

| Model | CV Metric | Average Score |
|-------|------------|--------------|
| KNN (Tuned) | F1-Macro | 0.6998 |
| Gradient Boosting (Tuned) | F1-Macro | 0.729 |
| MLP (Repeated Holdout) | F1-Macro | 0.671 |

---

## Final Model Selection

Gradient Boosting was selected as the final model because:

- Highest ROC-AUC score
- Strong cross-validation stability
- Balanced recall and precision for churn class
- More consistent generalization compared to MLP

---

## Key Business Insights

- Customers with **month-to-month contracts** show significantly higher churn rates.
- Higher **monthly charges** correlate with increased churn probability.
- Long-tenure customers are less likely to churn.
- Contract type and payment method are strong churn predictors.

These insights can support targeted retention campaigns and contract restructuring strategies.

---

## Tools & Technologies

- Python
- Pandas & NumPy
- Matplotlib
- Scikit-learn
- Git & GitHub

---

## Repository

Full preprocessing pipeline, modeling workflow, and evaluation code:

🔗 [GitHub Repository](https://github.com/meenakshinairm-bot/meenakshinairm.github.io/blob/main/projects/code/Telco%20churn.ipynb)

---

## Conclusion

This project demonstrates a complete machine learning workflow — from preprocessing and feature engineering to model comparison and validation — with emphasis on model stability and business interpretation.

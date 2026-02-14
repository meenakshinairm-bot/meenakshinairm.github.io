---
layout: default
title: Medical Expenses Prediction Using Regression
---

# Medical Expense Prediction using Regression Models

## Overview

This project applies regression modeling techniques to analyze and predict individual medical expenses using demographic and lifestyle factors. The objective was to identify key predictors of healthcare costs and determine the best-performing regression model.

The analysis demonstrates statistical modeling, feature engineering, and model evaluation using real-world insurance data.

---

## Problem Statement

Medical expenses vary significantly across individuals. This project aims to:

- Predict medical charges using regression models  
- Identify the most important factors influencing healthcare costs  
- Compare multiple regression approaches  
- Select the best-performing statistical model  

---

## Dataset

The dataset used is the **insurance.csv** dataset from Kaggle.

Dataset characteristics:

- 1,338 observations  
- Target variable: `charges`

Features include:

- Age  
- Sex  
- BMI (Body Mass Index)  
- Number of Children  
- Smoking Status  
- Region  

Engineered features:

- Age groups  
- BMI categories  
- Binary smoker indicator  
- Polynomial and transformed variables  

---

## Methodology

### 1. Data Preprocessing and EDA

- Checked dataset structure and summary statistics  
- Verified missing values  
- Converted categorical variables into numeric indicators  
- Created derived features for age and BMI categories  
- Visualized distributions using histograms and boxplots  
- Examined relationships using scatterplots and correlation matrices  

---

### 2. Regression Models Implemented

The following regression models were built and compared:

- Simple Linear Regression  
- Multiple Linear Regression  
- Polynomial Regression  
- Regression with Interaction Terms  
- Log and Square Root Transformations  
- Robust Regression  
- Weighted Least Squares Regression  

---

### 3. Model Evaluation

Models were evaluated using:

- Adjusted R-squared  
- AIC (Akaike Information Criterion)  
- BIC (Bayesian Information Criterion)  
- Mean Squared Error (MSE)  
- Residual diagnostics  

---

## Results

### Key Findings

- Smoking is the strongest predictor of medical expenses  
- Age has a nonlinear relationship with charges  
- BMI has a moderate positive effect on charges  
- Region and number of children have minimal impact  

---

### Model Performance Comparison

| Model | Adjusted R² | MSE |
|------|-------------|-----|
| Multiple Linear Regression | 0.75 | 329,456 |
| Polynomial Regression | 0.78 | 312,100 |
| Interaction Model | 0.76 | 319,500 |
| Robust Regression | 0.77 | 317,000 |

---

### Best Model

Polynomial Regression achieved the best performance with:

- Highest Adjusted R²  
- Lowest MSE  
- Best model fit  

---

## Visualizations and Analysis

The project included:

- Distribution plots of medical charges  
- Predictor vs target relationship plots  
- Correlation heatmaps  
- Residual diagnostic plots  
- Regression fit comparisons  

These confirmed nonlinear relationships and validated model assumptions.

---

## Tools and Technologies

- R  
- tidyverse  
- ggplot2  
- Statistical Modeling  
- Regression Analysis  

---

## Skills Demonstrated

- Regression modeling  
- Statistical analysis  
- Feature engineering  
- Model comparison  
- Data visualization  
- Healthcare data analysis  

---

## Project Links

Project Report (HTML):  
[View Full Analysis](YOUR_HTML_LINK_HERE)

Source Code:  
[View Code](YOUR_GITHUB_REPO_LINK_HERE)

---

## Conclusion

This project demonstrates how regression models can effectively predict healthcare costs and identify major contributing factors. Smoking status, age, and BMI were the most significant predictors. Polynomial regression provided the best predictive performance.

This analysis highlights the importance of statistical modeling in healthcare cost prediction and decision-making.

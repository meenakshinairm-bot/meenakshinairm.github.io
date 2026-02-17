---
layout: default
title: Obesity & Lifestyle Data Visualization
---

# Obesity & Lifestyle Data Visualization

## Overview

Obesity is one of the most significant public health challenges in the United States, contributing to increased risk of chronic diseases such as diabetes, cardiovascular disease, and certain cancers.

This project analyzes obesity patterns and their relationship with lifestyle behaviors such as physical inactivity and dietary habits using CDC Behavioral Risk Factor Surveillance System (BRFSS) data.

The goal is to identify patterns, explore behavioral risk factors, and communicate findings through effective data visualization and storytelling.

---

## Objectives

This project aims to:

- Analyze obesity prevalence across U.S. states
- Examine the relationship between obesity and physical inactivity
- Investigate dietary factors such as fruit consumption
- Identify behavioral patterns contributing to obesity
- Communicate insights using clear and meaningful visualizations

---

## Datasets

### Dataset 1: CDC Nutrition, Physical Activity, and Obesity Dataset

Source: CDC BRFSS (via Kaggle)

Includes:

- Obesity prevalence (%)
- Physical inactivity rates (%)
- Fruit consumption behavior
- State-level identifiers
- Adult health indicators across all 50 U.S. states

---

### Dataset 2: American Indian and Alaska Native BRFSS Subset (2023)

This dataset focuses on a specific demographic population, allowing analysis of health disparities and targeted behavioral trends.

---

## Methodology

### Data Preparation

- Imported and cleaned CSV datasets using R
- Filtered relevant health indicators
- Aggregated state-level values
- Prepared data for visualization

---

### Visualization Techniques

The project uses multiple visualization approaches to explore relationships:

- Bar charts for state comparisons
- Scatter plots for behavioral relationships
- Multi-variable visualizations for integrated analysis
- Regression trend lines to highlight associations

All visualizations were created using ggplot2 with consistent styling.

---

## Key Visualizations and Findings

### 1. Obesity Rates by State

- Significant variation exists between states
- Some states show consistently higher obesity prevalence

---

### 2. Obesity vs Physical Inactivity

Key finding:

States with higher physical inactivity rates tend to have higher obesity prevalence.

This suggests physical inactivity is a major contributing factor.

---

### 3. Obesity vs Low Fruit Consumption

Key finding:

States with lower fruit consumption tend to show higher obesity rates.

This supports the relationship between dietary behavior and obesity.

---

### 4. Combined Behavioral Analysis

When combining inactivity and diet:

- States with both high inactivity and poor diet show the highest obesity rates
- Multiple lifestyle factors contribute together rather than independently

---

## Tools & Technologies

- R
- tidyverse
- ggplot2
- dplyr
- readr
- R Markdown

---

## Project Output (Full Analysis Report)

View complete report with code and visualizations:

[View Full PDF Report](https://github.com/meenakshinairm-bot/meenakshinairm.github.io/blob/main/projects/code/Obesity.pdf)

---

## Key Insights

- Physical inactivity is strongly associated with obesity prevalence
- Poor dietary habits contribute to increased obesity rates
- Obesity patterns vary significantly across states
- Multiple behavioral factors interact to influence obesity risk

---

## Conclusion

This project demonstrates how data visualization can be used to analyze and communicate public health trends effectively.

The results highlight the importance of lifestyle behaviors such as physical activity and diet in influencing obesity outcomes.

This project showcases skills in:

- Data cleaning
- Exploratory data analysis
- Data visualization
- Public health data analysis
- Data storytelling

---

## Future Improvements

- Include regression modeling
- Analyze trends over multiple years
- Incorporate socioeconomic variables
- Apply predictive modeling techniques

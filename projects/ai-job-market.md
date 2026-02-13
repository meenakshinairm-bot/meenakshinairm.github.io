---
layout: default
title: AI Job Market Trends (2023–2025)
---

# AI Job Market Trends (2023–2025)

## Overview

This project analyzes global trends in Artificial Intelligence (AI), Machine Learning (ML), and Data Science job postings using a dataset of 2,000 job listings (2023–2025).

The goal is to understand:

- Which AI/ML roles are most in demand
- How salaries vary by experience level
- Which technical skills are most frequently required
- Geographic hiring distribution
- Broader employment patterns in the AI ecosystem

All analysis was conducted in **R** using `tidyverse`, `ggplot2`, and `dplyr`.

---

## Dataset

- 2,000 AI/ML job postings  
- Time range: September 2023 – September 2025  
- Key fields:
  - Job title
  - Skills
  - Experience level
  - Industry
  - Location
  - Salary range (USD)
  - Company size
  - Employment type

### Data Preparation

Key preprocessing steps:

- Split salary ranges into `min_salary` and `max_salary`
- Created `avg_salary` as midpoint
- Parsed location to extract country token
- Expanded comma-separated skills into individual rows
- Created derived variables:
  - `skill_count`
  - `primary_skill`
  - `role_group`

---

# Exploratory Findings

## Top Roles by Demand

| Role | Postings |
|------|----------|
| Data Analyst | 271 |
| NLP Engineer | 265 |
| AI Product Manager | 258 |
| Quant Researcher | 251 |
| ML Engineer | 250 |
| Data Scientist | 238 |
| AI Researcher | 237 |
| Computer Vision Engineer | 230 |

The dataset shows strong demand for both applied analytics roles and specialized ML engineering roles.

---

## Compensation by Experience Level

| Experience Level | Average Salary (USD) |
|------------------|----------------------|
| Entry | $123,404 |
| Mid | $121,441 |
| Senior | $124,329 |

Interestingly, mid-level salaries appear slightly lower than entry-level in this dataset, suggesting sampling composition effects or inconsistent level labeling.

---

## Most Requested Skills

Top technical skills by frequency:

TensorFlow, Excel, Pandas, FastAPI, NumPy, Reinforcement Learning, Azure, Hugging Face, SQL, Keras, AWS, GCP, Power BI, Python, LangChain.

This reflects employer demand for:

- Core programming (Python, SQL)
- ML frameworks (TensorFlow, Keras)
- Cloud platforms (AWS, GCP, Azure)
- Deployment tools (FastAPI, LangChain)

---

## Geographic Distribution (Preliminary)

Country tokens were extracted from the location field.  
Top tokens by count:

PG (19), BB (18), BT (18), FJ (18), HR (18), IQ (17), JO (17), GQ (16), JM (16), UZ (16)

Note: These are parsed country codes and require ISO validation for accurate mapping.

---

# Advanced Analysis Highlights

### Temporal Hiring Trends (2023–2025)
Monthly posting counts show sustained hiring activity with minor fluctuations.  
AI hiring remained consistently strong across the two-year period.

### Role Demand by Industry
Technology had the broadest role distribution.  
Finance and Healthcare showed higher demand for specialized Data Scientists and Quant Researchers.

### Salary by Role & Experience
Senior ML Engineers and AI Researchers showed the highest salary medians and widest ranges.

### Skill Co-occurrence Patterns
Two dominant clusters emerged:
- Core ML stack: Python, Pandas, NumPy, ML frameworks
- Production stack: Cloud platforms, APIs, deployment tools

This indicates increasing demand for full-stack ML capability.

---

# Key Takeaways

- AI hiring demand is strong and diversified across roles.
- Employers value both modeling expertise and productionization skills.
- Senior specialization commands higher compensation.
- Cloud and MLOps knowledge significantly increases role competitiveness.

---

# Limitations

- Dataset may not fully represent the global AI job market.
- Salary midpoint averaging masks bonus/equity variability.
- Location parsing requires ISO validation.
- Skill parsing may miss synonyms or alternate naming.

---

# Future Work

- Map country tokens to standardized ISO codes.
- Build a salary regression model controlling for role, industry, and company size.
- Apply NLP clustering to job descriptions.
- Develop an interactive dashboard for filtering roles and regions.

---

# Tools & Technologies

- R
- tidyverse
- ggplot2
- dplyr
- plotly

---

## Conclusion

This project transforms 2,000 AI job postings into a structured analysis of role demand, compensation patterns, and skill trends. The findings highlight a job market that rewards both advanced ML expertise and deployment-ready technical skills.

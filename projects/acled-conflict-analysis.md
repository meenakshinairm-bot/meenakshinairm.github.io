---
layout: default
title: Conflict Events Analysis in Africa (ACLED)
---

# Conflict Events Analysis in Africa (ACLED)

## Overview

Political violence and conflict significantly impact regional stability, economic development, and humanitarian conditions. Understanding where, when, and how conflicts occur is essential for identifying high-risk regions and analyzing trends over time.

This project analyzes conflict events across Africa using the Armed Conflict Location & Event Data (ACLED) dataset from 2021 to 2024.

The goal is to identify trends, analyze regional differences in conflict intensity, examine fatalities, and visualize the geographic distribution of conflict events using spatial data analysis techniques.

---

## Objectives

This project aims to:

- Analyze trends in conflict events across Africa from 2021 to 2024
- Identify regions with the highest number of conflict events
- Examine regional differences in fatalities
- Analyze the distribution of conflict event types
- Identify countries with the highest conflict activity
- Visualize geographic hotspots using spatial mapping techniques

---

## Dataset

### Dataset: ACLED Conflict Events Dataset

Source: Armed Conflict Location & Event Data (ACLED)

Includes:

- Event date and year
- Country and region
- Event type (Protests, Battles, Violence against civilians, etc.)
- Fatalities count
- Latitude and longitude coordinates
- Actor and event classification information

Regions included:

- Western Africa  
- Eastern Africa  
- Northern Africa  
- Middle Africa  
- Southern Africa  

---

## Methodology

### Data Preparation

- Imported dataset using R
- Inspected data structure and summary statistics
- Checked for missing values
- Filtered and organized data by year, region, and country
- Prepared geographic coordinates for spatial analysis

---

### Exploratory Data Analysis

The analysis examined:

- Conflict events per year
- Conflict events by region
- Fatalities by region and year
- Distribution of conflict event types
- Country-level conflict activity

Grouped summaries and aggregations were created using dplyr.

---

### Spatial Analysis and Visualization

Spatial visualization was performed using latitude and longitude coordinates to:

- Map conflict event locations
- Identify geographic hotspots
- Visualize event severity based on fatalities
- Compare conflict intensity between regions and countries

All visualizations were created using ggplot2 and spatial mapping techniques.

---

## Key Visualizations and Findings

### 1. Conflict Events Over Time

Key finding:

Conflict events increased steadily from 2021 to 2024, indicating rising instability in several African regions.

---

### 2. Conflict Events by Region

Key finding:

Eastern Africa recorded the highest number of conflict events, followed closely by Western Africa.

Southern Africa had the lowest number of conflict events.

---

### 3. Fatalities by Region

Key finding:

Western Africa recorded the highest number of fatalities despite having slightly fewer total events than Eastern Africa.

This indicates conflicts in Western Africa tend to be more severe.

---

### 4. Conflict Event Types Distribution

Key finding:

The most common conflict types include:

- Protests  
- Battles  
- Violence against civilians  
- Riots and explosions  

Protests were the most frequent event type overall.

---

### 5. Country-Level Conflict Analysis

Key finding:

Countries with the highest conflict activity include:

- Nigeria  
- Mali  
- Burkina Faso  

These countries represent major conflict hotspots in Western Africa.

---

### 6. Spatial Conflict Mapping

Spatial visualization showed:

- Clear geographic clustering of conflict events
- Higher concentration of severe events in Western and Eastern Africa
- Regional hotspots visible through geographic mapping

---

## Tools & Technologies

- R
- tidyverse
- ggplot2
- dplyr
- sf (spatial analysis)
- viridis
- R Markdown
- GitHub Pages

---

## Project Output (Full Analysis Report)

View complete report with code and visualizations:

[View Full HTML Report](https://github.com/meenakshinairm-bot/meenakshinairm.github.io/blob/main/projects/code/Conflict-Events-Analysis-in-Africa.pdf)

---

## Code Availability

View R Markdown source code:

[View R Markdown File](../rmd/acled-conflict-analysis.Rmd)

---

## Key Insights

- Conflict events increased steadily from 2021 to 2024
- Eastern Africa had the highest number of events
- Western Africa had the highest fatalities
- Nigeria, Mali, and Burkina Faso were major conflict hotspots
- Protest was the most common conflict type
- Spatial analysis revealed clear geographic conflict clusters

---

## Conclusion

This project demonstrates how spatial and temporal data analysis can be used to understand conflict patterns and regional instability.

The results highlight increasing conflict activity and regional differences in severity across Africa.

This project showcases skills in:

- Data cleaning
- Exploratory data analysis
- Spatial data analysis
- Data visualization
- Geographic mapping
- Data storytelling

---

## Future Improvements

- Include predictive modeling for conflict forecasting
- Analyze socioeconomic and political factors influencing conflict
- Expand analysis to additional years
- Apply machine learning techniques for pattern detection

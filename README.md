# DSA 210 Tesla Analysis

## Introduction

This project explores and analyzes charging and driving behaviors using TeslaMate data. The goal is to apply advanced data science techniques to uncover insights into energy consumption, driving patterns, and charging efficiencies while integrating additional contextual data, such as weather, to enhance the analysis.

## Objectives

1. Perform Exploratory Data Analysis (EDA) to understand trends, anomalies, and distributions in the TeslaMate dataset.
2. Apply statistical methods to test hypotheses related to energy consumption, weather effects, and charging behavior.
3. Develop meaningful visualizations to communicate insights effectively.
4. Leverage Tesla API and Open-Meteo API to enrich the dataset with real-time weather information.
5. Use Google Cloud to ensure scalability and accessibility for data storage and analysis.

## Tools and Techniques

- **Data Manipulation**: Python libraries such as Pandas and NumPy.
- **Visualization**: Matplotlib, Seaborn, and Plotly for interactive charts.
- **Statistical Analysis**: Hypothesis testing, regression, and correlation analysis.
- **API Integration**: Tesla API for vehicle data, Open-Meteo API for weather conditions.
- **Cloud Infrastructure**: Google Cloud Platform (GCP) for hosting TeslaMate and processing datasets efficiently.

## Dataset

The dataset includes TeslaMate logs with detailed information about:

### Charging Sessions
- **Metrics**: kWh, duration, location, and charger type.
- **Focus**: Correlation with weather conditions and time of day.

### Driving Sessions
- **Metrics**: Distance traveled, energy consumption, and efficiency.
- **Enrichment**: Elevation and route mapping using Open-Meteo API.

The integration of weather and driving data allows for enriched contextual analysis, identifying relationships between external factors and vehicle performance.

## Methodology

### 1. Data Collection
- Data sourced from TeslaMate, stored in a PostgreSQL database hosted on Google Cloud.
- Weather data fetched via the Open-Meteo API based on GPS coordinates from Tesla logs.

### 2. Data Cleaning
- **Addressing Missing Values**: Techniques like KNN imputation and regression were applied to fill gaps.
- **Formatting**: Conversion of datetime columns and standardization of units.

### 3. Exploratory Data Analysis (EDA)
- **Visualization**:
  - Scatter plots for energy consumption vs. distance traveled.
  - Boxplots for analyzing energy consumption under different weather conditions.
  - Correlation heatmaps for identifying relationships between variables.
- **Key Metrics**:
  - Distribution of charging durations.
  - Daily energy efficiency patterns.

### 4. Statistical Hypothesis Testing
- **Tests Used**:
  - Pearson and Spearman correlations for linear and monotonic relationships.
  - Mann-Whitney U test for comparing energy efficiency across weather conditions.
- **Example Hypothesis**:
  - Null Hypothesis ( H0): Weather conditions do not significantly affect energy consumption.
  - Alternative Hypothesis ( H1): Weather conditions significantly impact energy consumption.

### 5. Advanced Modeling
- Multiple regression to predict energy consumption based on distance, weather, and speed.
- Exploratory network analysis to understand the connections between charging locations.

## What Has Been Done So Far

1. Successfully hosted TeslaMate on Google Cloud and processed the initial dataset.
2. Conducted EDA to identify trends in energy usage and driving patterns.
3. Resolved dataset formatting issues for compatibility with analytical tools.
4. Integrated weather data from Open-Meteo API for enhanced contextual analysis.
5. Developed visualizations, including scatter plots and heatmaps, to illustrate findings.

## Next Steps
Getting more data and understanding the real effect of everytihng on efficency of EV

## References

The project extensively uses insights and methodologies from the following:

1. Tesla API Documentation for vehicle data integration.
2. Open-Meteo API Documentation for weather enrichment.
3. Google Cloud services for data hosting and analysis scalability.
4. Python libraries: Pandas, Matplotlib, Seaborn.



# weather-trend-forecasting
Weather forecasting and climate analysis using ML models

## Overview

This project was completed as part of the PM Accelerator Technical Assessment.

The objective was to analyze global weather data, identify patterns and trends, and build machine learning models capable of forecasting temperature. In addition to forecasting, the project explores weather relationships through exploratory data analysis, anomaly detection, feature importance analysis, environmental impact analysis, and spatial analysis.

---

## Dataset

The project uses the Global Weather Repository dataset from Kaggle:

https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository

The dataset contains weather observations collected from cities around the world and includes information such as temperature, humidity, wind speed, pressure, precipitation, air quality indicators, and geographical coordinates.

---

## Project Workflow

### 1. Data Cleaning and Preprocessing

The dataset was inspected for missing values and duplicate records. Datetime information was converted into a suitable format for time-series analysis, and additional time-based features were created, including:

* Month
* Day
* Day of Week

These features helped capture seasonal and temporal weather patterns.

### 2. Exploratory Data Analysis

Several analyses were performed to better understand the data:

* Temperature distribution
* Humidity analysis
* Precipitation analysis
* Correlation analysis
* Country-wise temperature comparisons
* Time-series trend analysis

Visualizations were created to identify trends, relationships, and unusual observations.

### 3. Machine Learning Models

Two regression models were developed and evaluated:

#### Linear Regression

Used as a baseline model to understand linear relationships between weather variables and temperature.

#### Random Forest Regressor

Used to capture more complex, non-linear relationships in weather data. This model significantly outperformed Linear Regression and was selected as the final forecasting model.

---

## Model Performance

### Random Forest Results

| Metric   | Value |
| -------- | ----- |
| R² Score | 0.96  |
| MAE      | 1.3   |
| RMSE     | 1.8   |

### Cross Validation

Average Cross-Validation R² Score:

0.856

These results indicate that the model is able to explain a large portion of temperature variability while maintaining good generalization performance.

---

## Advanced Analyses

### Feature Importance

Feature importance analysis was performed using Random Forest to understand which variables contribute most to temperature prediction.

The most influential features were:

* Latitude
* UV Index
* Pressure
* Month
* Longitude

### Anomaly Detection

Isolation Forest was used to identify unusual weather observations. These anomalies may represent rare weather conditions or extreme events.

### Environmental Impact Analysis

Relationships between weather conditions and air quality indicators such as PM2.5, PM10, Ozone, and Carbon Monoxide were explored using correlation analysis.

### Spatial Analysis

Geographical patterns were analyzed using latitude and longitude to understand how weather conditions vary across different regions.

---

## Key Findings

* Random Forest performed significantly better than Linear Regression.
* Feature engineering substantially improved forecasting performance.
* Latitude was the strongest predictor of temperature.
* Weather conditions showed measurable relationships with air quality indicators.
* Anomaly detection successfully identified unusual weather observations.
* Geographical location plays a major role in temperature variation.

---

## Repository Structure

```text
weather-trend-forecasting
│
├── images
├── notebooks
├── README.md
└── requirements.txt
```

---

## Running the Project

1. Install the required libraries:

```bash
pip install -r requirements.txt
```

2. Open the notebook:

```text
Weather analysis.ipynb
```

3. Run all cells to reproduce the analysis and results.

---

## Conclusion

This project demonstrates a complete machine learning workflow, starting from data cleaning and exploratory analysis through model development and advanced analytical techniques. The final Random Forest model achieved strong predictive performance and provided valuable insights into global weather patterns and the factors influencing temperature.

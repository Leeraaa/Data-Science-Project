# It's better to watch the presentation SeasonalTemp !!!

# Data-Science-Project

# Seasonal Temperature Forecasting Using Time Series Analysis

## Overview

The goal of the project is to forecast maximum daily temperature using historical weather observations and advanced time series forecasting techniques.

The project combines statistical modeling, feature engineering, exploratory data analysis, and hybrid forecasting methods to improve prediction accuracy.

---

## Problem Statement

Weather forecasting is a classic time series prediction problem.

The objective of this project is to predict future maximum temperatures using:

* Historical temperature observations
* Weather-related variables
* Seasonal patterns
* Temporal dependencies

The project investigates how different forecasting models capture seasonality, trends, and external influences.

---

## Dataset

The dataset contains historical weather measurements including:

* Maximum temperature
* Minimum temperature
* Precipitation
* Wind speed
* Calendar information

The target variable is:

* Maximum daily temperature

---

## Exploratory Data Analysis (EDA)

Before model development, an extensive exploratory analysis was performed.

### Time Series Visualization

The analysis revealed:

* Strong annual seasonality
* Stable long-term patterns
* Variability in precipitation and wind speed

### Outlier Detection

Outliers were identified using Z-score analysis.

Detected outliers:

* Precipitation: 37
* Maximum temperature: 0
* Minimum temperature: 1
* Wind speed: 15

### Correlation Analysis

Key findings:

* Strong correlation between maximum and minimum temperature
* Weak relationship between temperature and precipitation
* Weak relationship between temperature and wind speed

These variables were included as additional regressors.

### Seasonality Analysis

Seasonality was investigated using:

* Moving averages
* Monthly boxplots
* Trend visualization

The analysis confirmed a strong yearly seasonal pattern.

---

## Stationarity Analysis

The Augmented Dickey-Fuller (ADF) test was used to evaluate stationarity.

Techniques applied:

* Seasonal differencing
* Trend removal
* Statistical validation

Stationarity was achieved prior to model fitting.

---

## Models Implemented

### 1. SARIMA

Seasonal AutoRegressive Integrated Moving Average.

The model captures:

* Trend
* Autoregressive behavior
* Moving-average structure
* Seasonal patterns

Parameters were selected using:

* ACF analysis
* PACF analysis

---

### 2. Prophet with Enhanced Regressors

The Prophet model was extended with additional predictors.

Added regressors:

* Minimum temperature
* Precipitation
* Wind speed
* Day of week
* Month
* Lag features

Prophet automatically models:

* Trend
* Seasonality
* Calendar effects

---

### 3. Hybrid Prophet + SARIMA

A two-stage forecasting approach.

Step 1:

Prophet generates the primary forecast.

Step 2:

SARIMA models and corrects residual autocorrelation.

This hybrid architecture combines:

* Prophet's flexibility
* SARIMA's ability to model temporal dependencies

---

## Model Evaluation

Models were evaluated using:

### Mean Absolute Error (MAE)

Measures average prediction error.

Lower values indicate better performance.

### Root Mean Squared Error (RMSE)

Measures the magnitude of prediction deviations.

### Ljung-Box Test

Used to evaluate residual independence.

A p-value greater than 0.05 indicates well-behaved residuals.

---

## Results

The hybrid Prophet + SARIMA model achieved the best overall performance.

Key findings:

* SARIMA effectively captures seasonality.
* Prophet benefits from additional regressors.
* Residual correction with SARIMA improves forecast quality.
* The hybrid model produced the lowest forecasting errors.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Prophet
* Scikit-Learn
* Google Colab

---

## Skills Demonstrated

This project demonstrates practical experience in:

* Data Science
* Time Series Forecasting
* Forecast Analytics
* Statistical Modeling
* SARIMA
* Prophet
* Feature Engineering
* Exploratory Data Analysis
* Model Evaluation
* Forecast Validation
* Scientific Programming

---

## Repository Contents

* Complete implementation
* Project presentation
* Forecasting models and evaluation results
* Visualizations and diagnostics

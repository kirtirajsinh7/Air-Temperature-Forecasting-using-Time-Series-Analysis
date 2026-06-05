# Air Temperature Forecasting using Time Series Analysis

## Overview

This project focuses on analyzing historical monthly mean air temperature data and developing a forecasting model capable of predicting future temperature trends.

The project combines exploratory data analysis, time series decomposition, statistical testing, forecasting model comparison, cross-validation, and business recommendations to support climate-related decision-making.

---

# Business Problem

Air temperature is one of the most important environmental variables affecting multiple industries. Even small temperature changes can impact:

* Agriculture productivity
* Energy demand
* Urban planning
* Weather-related risk management
* Climate monitoring

The goal of this project is to:

1. Analyze historical temperature patterns
2. Identify seasonality and trend components
3. Build forecasting models for future temperature prediction
4. Compare multiple time series models
5. Provide actionable recommendations based on forecasts

---

# Dataset Information

## Dataset

The dataset used in this project contains historical monthly mean air temperature observations.

The dataset consists of:

* Monthly Timestamp (month)
* Monthly Mean Air Temperature (mean_temp)

### Dataset Characteristics

* Approximately 462 observations
* Monthly frequency
* Univariate time series dataset
* Covers nearly 38 years of historical temperature records

---

# Project Workflow

## 1. Data Understanding

* Data loading
* Data type validation
* Missing value analysis
* Statistical summary
* Duplicate checks

## 2. Exploratory Data Analysis (EDA)

* Univariate analysis
* Distribution analysis
* Outlier detection
* Time series visualization
* Seasonal decomposition
* Trend analysis

## 3. Time Series Analysis

Performed statistical checks including:

* Stationarity testing using ADF Test
* ACF Analysis
* PACF Analysis
* Seasonal pattern analysis

## 4. Data Preprocessing

Applied preprocessing techniques including:

* Datetime conversion
* Index creation
* Time-based transformations
* Train-test split for time series

## 5. Model Development

Multiple forecasting models were trained and compared:

* ARIMA
* Tuned ARIMA
* SARIMA
* Tuned SARIMA
* Holt-Winters Exponential Smoothing

## 6. Model Evaluation

Models were evaluated using:

* RMSE (Root Mean Squared Error)
* MAE (Mean Absolute Error)
* MAPE (Mean Absolute Percentage Error)
* R² Score
* Walk-Forward Cross Validation

---

# Key Insights

## Time Series Characteristics

* Strong yearly seasonality with 12-month repeating cycles
* Mild upward temperature trend observed over time
* Stable temperature range without extreme anomalies
* Significant temporal dependency between observations

## Statistical Findings

* ADF Test confirms stationarity in mean level
* Strong seasonal structure exists despite stationarity
* Seasonal differencing improves forecasting performance

---

# Final Model Performance

| Model        | RMSE   | MAE    | MAPE  |
| ------------ | ------ | ------ | ----- |
| ARIMA        | 0.8835 | 0.7620 | 2.70% |
| Tuned ARIMA  | 0.8747 | 0.7512 | 2.66% |
| Holt-Winters | 0.5931 | 0.4678 | 1.66% |
| SARIMA       | 0.6239 | 0.4939 | 1.75% |
| Tuned SARIMA | 0.6137 | 0.4853 | 1.72% |

---

# Model Selection

The final selected model was:

**Tuned SARIMA Model**

Reasons for selection:

* Captures seasonality effectively
* Lower forecasting error
* Better long-term prediction capability
* Performs well on walk-forward validation

---

# Forecasting Results

The selected SARIMA model was used to forecast:

* Next 12 months of temperature values
* Confidence intervals for future predictions
* Seasonal temperature fluctuations

Forecast observations suggest:

* Seasonal temperature cycles continue
* No abrupt climate shifts detected
* Gradual warming trend persists

---

# Business Recommendations

Based on analysis and forecasting results:

* Use forecasts for agricultural planning
* Support energy demand management
* Improve weather-related preparedness
* Assist climate monitoring initiatives
* Enable long-term environmental planning

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Scikit-learn
* Jupyter Notebook

---

# Project Structure

```bash
air-temperature-forecasting/
│
├── data/
│   └── raw_data/
│
├── Project Summary/
│   ├── Analysis/
│   └── Requirement/
│
├── src/
│   ├── data_processing/
│   └── models/
│
├── .gitignore
├── README.md
```

---

# Validation Strategy

To ensure robust forecasting performance:

* Holdout test evaluation was performed
* Walk-forward cross validation was used
* Residual diagnostics were analyzed
* Forecast uncertainty intervals were generated

---

# Conclusion

This project successfully analyzed historical air temperature patterns and developed a forecasting model capable of predicting future temperature trends with seasonal awareness.

The generated insights and forecasts can support environmental planning, climate monitoring, and operational decision-making across multiple industries.

---

# Author

- Kirteeraj Zala

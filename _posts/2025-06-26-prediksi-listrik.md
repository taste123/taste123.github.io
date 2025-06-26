---
layout: default
title: Electricity Consumption Forecasting
description: A project to forecast electricity consumption using ARIMA, SARIMA, and LSTM models, complete with an interactive Streamlit dashboard for visualization and analysis.
date: 2025-06-16
categories: [Project, Time Series Analysis]
tags: [Python, Streamlit, LSTM, ARIMA, SARIMA, Scikit-Learn, Tensorflow, Keras, Plotly, Pandas]
image:
  path: /assets/img/predict.png
---

# ⚡ Forecasting Electricity Consumption with Time Series Models

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com/ReyRiz/forecasting-electricity-consumption/blob/main/README.md)
[![Status](https://img.shields.io/badge/Status-Completed-success.svg)]()

![](/assets/img/predict.png)

## 📋 Project Description

This project develops and compares multiple time series models to forecast electricity consumption. It explores classical statistical methods alongside modern deep learning techniques to improve prediction accuracy and understand energy usage patterns. The primary output is an interactive web application that serves as a comprehensive dashboard for data visualization, forecasting, and model comparison.

### 🎯 Project Objectives
- To implement and evaluate various time series models for electricity forecasting.
- To compare the performance and characteristics of statistical models (ARIMA, SARIMA) versus deep learning models (LSTM).
- To develop an interactive and user-friendly Streamlit dashboard for visualizing data, generating forecasts, and analyzing results.
- To provide a practical tool for understanding and predicting electricity consumption patterns.

## 🏆 Key Features

- **Interactive Dashboard**: A multi-page Streamlit application for a seamless user experience.
- **Data Visualization**: Rich, interactive plots showing historical consumption, trends, and seasonal patterns.
- **Multi-Model Forecasting**: Generate and visualize forecasts from four distinct models.
- **Dynamic Comparison**: Select and compare forecasts from different models side-by-side on the same plot.
- **Usage Insights**: Analyze consumption patterns, such as hourly usage distribution and weekly trends.

## 📊 Dataset

- **Source**: Individual household electric power consumption dataset.
- **Preprocessing**: The raw data is resampled to an hourly frequency, and missing values are handled using time-based interpolation to create a clean, continuous time series suitable for modeling.
- **Features**: The primary feature is `Global_active_power` (in kilowatts). The Enhanced LSTM model also incorporates temporal features like hour of the day and day of the week.

## 🛠️ Technologies Used

### Core Language
- **Python 3.8+**

### Key Libraries
```python
# Web App & Visualization
streamlit
plotly
matplotlib
seaborn

# Data Handling & Machine Learning
pandas
numpy
scikit-learn
tensorflow
keras
statsmodels
joblib
```

## 📁 Project Structure
The project is organized into a main Streamlit application file, model files, and utility scripts, making it straightforward to run and understand.

```
forecasting-electricity-consumption/
│
├── electricity_forecast_app_fixed.py  # Main Streamlit application
│
├── best_arima_model.pkl          # Pre-trained ARIMA model
├── best_sarima_tuned_model.pkl   # Pre-trained SARIMA model (Assumed)
├── best_lstm_model.h5            # Pre-trained Basic LSTM model
├── lstm_scaler.pkl               # Scaler for Basic LSTM
├── best_enhanced_lstm_model.h5   # Pre-trained Enhanced LSTM model
├── enhanced_lstm_scaler.pkl      # Scaler for Enhanced LSTM
│
├── show_forecasting.py           # UI components for forecasting page
├── show_model_comparison.py      # UI components for comparison page
│
├── dataset.csv                   # Processed dataset (Assumed from app)
├── requirements.txt              # Project dependencies
└── README.md                     # Project documentation
```

## 📈 Methodology

### 1. Data Preprocessing
- Data is loaded and parsed into a proper datetime index.
- It is resampled to an hourly average to smooth out noise and create a consistent time frequency.
- Missing values are imputed using time-based interpolation to ensure data continuity.

### 2. Model Development
Four models were developed and pre-trained:
- **ARIMA**: A statistical model for non-seasonal time series data.
- **SARIMA**: An extension of ARIMA that explicitly models seasonal components in the data.
- **Basic LSTM**: A Long Short-Term Memory network that learns patterns from a sequence of past consumption values.
- **Enhanced LSTM**: A more advanced LSTM model that uses both past consumption values and engineered temporal features (e.g., sine/cosine transformations of hour and day) to capture more complex patterns.

### 3. Forecasting & Evaluation
- The Streamlit application loads the pre-trained models.
- Users can select a model and a forecast horizon (in days).
- The application generates forecasts and plots them against historical data.
- The comparison tool visualizes forecasts from multiple models simultaneously and presents descriptive statistics (mean, min, max, std dev) for each forecast.

## 🔮 Future Development

- [ ] Integrate a test set evaluation to display quantitative accuracy metrics (MAE, RMSE, R²) for each model.
- [ ] Implement hyperparameter tuning options in the dashboard.
- [ ] Add SHAP or similar methods for model interpretability, especially for the LSTM models.
- [ ] Allow users to upload their own time series data for forecasting.

<a href="https.github.com/ReyRiz/forecasting-electricity-consumption" target="_blank" class="btn btn-primary">
  <i class="fas fa-fw fa-code"></i>
  Source Code
</a>

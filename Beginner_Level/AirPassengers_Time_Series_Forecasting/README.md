# AirPassengers Time Series Forecasting

## Project Overview

This project applies classical time series analysis and forecasting techniques to the benchmark AirPassengers dataset using Python. The goal is to identify underlying patterns such as demand trends and seasonal cycles in monthly international airline passenger numbers, and to generate reliable multi-step forecasts.

Understanding these patterns is crucial for airlines to accurately plan capacity, schedule crews, and manage procurement. This analysis provides a comprehensive pipeline from data exploration and stationarity testing to building and comparing various forecasting models.

## Analysis Objectives

The analysis aims to explore the dataset and accomplish the following key objectives:
- **Data Exploration & Visualization:** Visualize the raw time series to identify visible trends and seasonal patterns.
- **Time Series Decomposition:** Decompose the series to isolate trend, seasonality, and residual components.
- **Stationarity Testing:** Apply the Augmented Dickey-Fuller (ADF) test and explore ACF/PACF plots.
- **Classical Modeling:** Build and evaluate multiple time series models, including:
  - Autoregression (AR)
  - Moving Average (MA)
  - Exponential Smoothing & Holt-Winters
  - ARIMA & SARIMA
- **Model Evaluation:** Compare model performance using Mean Squared Error (MSE) to identify the best forecasting approach.

## Libraries Used

- `pandas` for data manipulation
- `numpy` for numerical computing
- `matplotlib` for data visualization
- `statsmodels` for time series decomposition, statistical testing, and modeling
- `scikit-learn` for evaluation metrics and data scaling

## Workflow

1. **Load Data**: The dataset `AirPassengers.csv` is loaded, and the month column is parsed as a datetime index.
2. **Exploratory Data Analysis (EDA)**: Visualizing the raw series to form a baseline understanding of trends and multiplicative seasonality.
3. **Decomposition & Stationarity**: Decomposing the time series and using ADF testing and ACF/PACF plots to check for stationarity.
4. **Model Building**: Training a progression of classical time series models (AR, MA, Exponential Smoothing, Holt-Winters, ARIMA, SARIMA).
5. **Evaluation & Comparison**: Forecasting future values and comparing model accuracies using MSE.

## How to Run

Open the `AirPassengers_Time_Series_Forecasting.ipynb` Jupyter Notebook and run the cells sequentially. Make sure you have the required libraries installed and the dataset `AirPassengers.csv` in the appropriate directory as referenced in the notebook.

## Credits

Dataset provided by [rakannimer on Kaggle](https://www.kaggle.com/datasets/rakannimer/air-passengers).

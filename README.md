# Time Series Analysis of Total Fossil Fuels Consumption (problem 1)

This repository contains the code and analysis for forecasting the consumption of total fossil fuels using time series analysis techniques. The project focuses on understanding and predicting trends in fossil fuel consumption, including coal, natural gas, and petroleum products, by leveraging ARIMA (AutoRegressive Integrated Moving Average) and VAR (Vector Autoregression) models.

## Overview

The analysis includes the following components:

1. **Data Exploration and Visualization**:
   - Initial exploration of the time series data to identify trends, seasonality, and any patterns.
   - Visualization of the time series plot to illustrate the historical consumption of total fossil fuels.

2. **ARIMA Model Selection and Forecasting**:
   - Transformation of the data using natural logarithms and differencing to achieve stationarity.
   - Identification of optimal ARIMA model parameters using AIC (Akaike Information Criterion) and BIC (Bayesian Information Criterion).
   - Diagnostic checks (e.g., Ljung-Box test) to validate the chosen ARIMA model.
   - Generation of forecasts for the subsequent months, considering seasonal variations in fossil fuel consumption.

3. **VAR Model Analysis and Comparison**:
   - Integration of additional economic indicators (e.g., GDP growth rate, Industrial Production Index) into a VAR model.
   - Comparative analysis between the ARIMA and VAR models to assess the impact of economic factors on energy consumption trends.

4. **Insights from Related Time Series**:
   - Analysis of related time series data (e.g., GDP growth rate, Industrial Production Index) to understand their influence on fossil fuel consumption.
   - Visualization of time series plots and forecast trends for economic indicators.


Feel free to contribute, suggest improvements, or provide feedback to enhance this time series analysis project.

# Modeling Volatility of Tesla, Inc. Stock (TSLA) using GARCH

This repository contains the analysis and modeling of volatility for Tesla, Inc. (TSLA) stock returns from January 1, 2022, to January 1, 2024, utilizing a Generalized Autoregressive Conditional Heteroskedasticity (GARCH) model.

## Summary Statistics

After uploading the data and processing observations from January 3, 2022, to December 29, 2023, the following summary statistics were obtained for the variable 'ld_AdjClose' (500 valid observations):

- Mean: -0.00095184
- Median: 0.00099742
- Minimum: -0.13059
- Maximum: 0.10436
- Standard deviation: 0.038102
- Coefficient of Variation (C.V.): 40.030
- Skewness: -0.29333
- Excess Kurtosis: 0.74510
- 5% Percentile: -0.068778
- 95% Percentile: 0.060470
- Interquartile Range: 0.041742
- Missing observations: 1

## Model Estimation and Analysis

1. **AR(1) Model for Logarithm of Adjusted Close (ld_AdjClose)**:
   - The estimated coefficient is very close to 1, indicating high persistence in the series.

2. **Time Series Plot of Difference in Log-Transformed Returns**:
   - The plot shows a mean of 0 with significant variability around it, suggesting volatility in returns without visible predictability.

3. **Correlogram of Squared Excess Returns**:
   - The correlogram demonstrates the lack of correlation between returns and their own past, indicative of no autocorrelation in squared returns.

4. **GARCH Model Parameters**:
   - **Constant (const)**: Estimated value is -0.000528564 with a p-value of 0.7483, indicating insignificance.
   - **Alpha(0)**: Coefficient is 2.72254 x 10^-5 (p=0.2308), also not statistically significant.
   - **Alpha(1)**: Coefficient is 0.0319516 (p=0.0157), indicating statistical significance.
   - **Beta(1) (β1)**: Coefficient is 0.948037 (p < 0.0001), suggesting high persistence in volatility.

5. **Model Fit and Statistics**:
   - **Mean of Dependent Variable Variance**: -0.000952, indicating the average change in variance.
   - **Standard Error of Dependent Variable Variance**: 0.038102, representing variance variation around the mean.
   - **Unconditional Variance of the Error**: 0.00136048, with lower values indicating model superiority.
   - **Likelihood Ratio Test for GARCH**: Significant chi-square value (15.2984) with a p-value close to zero (0.000476415), indicating improved model performance with GARCH terms.

## Forecasting

The forecast for the next day (February 1, 2024) has a standard deviation of 0.038102, which is relatively close to the unconditional standard error of 0.03688468516.

Feel free to collaborate and contribute to this project focused on modeling volatility for Tesla, Inc. stock using GARCH techniques.

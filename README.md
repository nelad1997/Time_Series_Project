# TimeSeris_Project
Project Overview
This project focuses on analyzing and forecasting international flight departures from the United States between 1990 and 2020. The analysis integrates time series models with external economic indicators (CPI indices) to understand long-term trends, detect anomalies, and improve forecasting accuracy.

## Key Goals:

### Data Integrity:
Ensure clean, continuous, and reliable time series data by filtering, imputing, and aligning flight and CPI datasets.

### Seasonal and Structural Insights:
Uncover recurring patterns and regime shifts using decomposition, residual diagnostics, and change point detection.

### Model Evaluation:
Compare multiple forecasting models using both absolute and relative performance metrics (MSE, MAPE).

###Interpretability:
Incorporate economic context using CPI indices (Energy, Transportation, Gasoline) as exogenous regressors to enhance explainability of flight activity.

### Data Preprocessing:

Aggregated monthly international departures and aligned CPI data to the same time span (1990–2020).

Removed post-COVID-19 data to preserve structural stability.

Missing CPI energy values (1990–1992) were optionally imputed with January 1993 values or left as NaNs depending on the experiment.

###  Modeling Approaches:

#### SARIMA: Classical time series model with and without exogenous variables.

#### Prophet: Flexible model for handling seasonality and trend shifts, tested with regularization.

#### Exponential Smoothing: Captures level, trend, and seasonal components.

##### Linear Regression with Fourier Terms: Models seasonality explicitly and supports external regressors.

#### Regression with AR(1): Enhances model fit by accounting for autocorrelation in residuals.

### Evaluation and Forecasting:

Used an 80/20 train/test split, equivalent to training on 24 years and testing on the last 6.

Forecast horizon extended up to 5 years.

Each model was evaluated using MSE and MAPE for robust comparison.

Anomaly Detection and Insights:

Residual analysis from the SARIMA model revealed key anomalies (e.g., 9/11, 2008 crisis, and a subtle deviation in September 2000).

Change point detection techniques supported the discovery of structural breaks.

Visualization and Interpretation:

Normalized CPI vs. departures graph highlights alignment between economic signals and flight activity.

Forecast plots include historical patterns and key event markers for contextual clarity.

Residual diagnostics include scatter plots, histograms, QQ-plots, and ACFs.

## Files Included:

ProjectEx1.ipynb: full code and analysis

ProjectEx1.pdf: final submitted report

dataProjectEx1.csv: cleaned, combined dataset

ProjectEx1.html: HTML-rendered version of notebook for viewing

## Lessons Learned:
This project provided hands-on experience in time series modeling, feature engineering with exogenous data, and the trade-offs between flexibility and overfitting in models like Prophet. It also emphasized the value of preprocessing, diagnostics, and careful metric selection for meaningful evaluation.

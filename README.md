# Interest Rate Forecasting using VAR Model

### Project Overview

This project focuses on forecasting interest rates using a Vector Autoregression (VAR) model. The goal is to predict future interest rates such as the 10-year bond yield, the 3-month Treasury bill rate, and the Federal Reserve's interest rate (FedRate) over a period of 12 months. The VAR model is used to capture the interdependencies between these variables and generate reliable forecasts based on historical data from 1990 to 2019.

### Key Features

- Reliable VAR Forecasting: The model includes fallbacks for unreliable forecasts, ensuring that output is always generated.
- Dynamic Forecasting: The model forecasts interest rates over a 12-month horizon.
- Data Resampling: The dataset is resampled to a quarterly frequency for stability and then made stationary using differencing.
- Forecast Visualization: The forecasted interest rates are plotted alongside historical data to provide a clear comparison.

### Dataset

The dataset consists of US bond yield data from 1990 to 2019, which includes:

- 3-month yield
- 2-year yield
- 10-year yield

The data is used to calculate various yield curve spreads, which are key indicators of potential economic downturns.

### Project Workflow

1. Data Preprocessing:
- Data was cleaned and resampled to a quarterly frequency to ensure stability and consistency.
- The target variable for forecasting is the 10-year bond yield, and predictors include the 3-month Treasury bill rate and the Federal Reserve's interest rate.

2. Modeling Approach:
- The VAR model is implemented using a reliable approach, with fallbacks for situations where the model might fail.
- The dataset is made stationary by differencing, ensuring that it is suitable for time-series modeling.
- The VAR model is fit to the stationary data with a conservative lag of 2 periods for reliability.
- If the VAR model fails, a fallback method (last value persistence) is used for forecasting.

3. Forecasting:
- After fitting the VAR model, the forecast for the next 12 months is generated.
- The forecast includes the predicted values for the 10-year bond yield, 3-month Treasury bill rate, and the Federal Reserve's interest rate.
- Forecast results are plotted alongside the actual historical data to visualize the predictions.

### Results

- Forecasted interest rates are presented for the next year, showing expected declines in the 10-year bond yield and smaller changes in the short-term rates.

- The forecast provides insights into potential trends in interest rates and can inform economic planning and investment decisions.

### Conclusion

The VAR model forecasts future interest rates, helping to anticipate economic trends. The results of this model can be used to inform investment decisions, policy planning, and financial forecasting. This project demonstrates the potential of VAR models to capture the relationships between key interest rates and make predictions about their future behavior.

### Source

![U.S. Treasury Yields from Kaggle](https://www.kaggle.com/datasets/guillemservera/us-treasury-yields-daily)

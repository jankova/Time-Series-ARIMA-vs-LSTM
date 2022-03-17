# Comparison of ARIMA and LSTM for time series forecasting

We compare the performance of traditional ARIMA models and Recurrent Neural Networks (LSTMs) for time series forecasting.

There are numerous ways of formulating a time series forecasting problem depending on the business scenario.

We simulate two scenarios. In both scenarios a time series model is trained and deployed, and we monitor its test performance over time. 
The model is not retrained during this testing phase.

1. **One-step moving origin forecasting**: 
 We produce a one-step forecast at each time step t and we observe a new data point that is added to the training dataset to compute the next step forecast. This is called 'moving origin' since we always observe a new data point at time t and thus the model is using only true historical data for every one-step forecast.

2. **Fixed origin forecasting:** Fixed origin means that the forecast we make at time step t will be added to the training dataset to compute the forecast at step t+1. This problem formulation is arguably more challenging than (1) as the model is using its own forecasts to generate further forecasts. 

Both monitoring strategies produce a sequence of one-step forecasts, which can be compared against the true test observations. 

As a measure of performance of the models, we use **MAPE** (mean absolute percentage error). 

We perform the analysis on two datasets:

1. **Electricity consumption** (trend and seasonality)

    Jupyter Notebook: [Electricity-consumption-times-series.ipynb](https://github.com/jankova/Time-Series-ARIMA-vs-LSTM/blob/main/Electricity-consumption-times-series.ipynb)


2. **Air pollution** (no clear trend or seasonality)

    Jupyter Notebook: [Pollution-times-series.ipynb](https://github.com/jankova/Time-Series-ARIMA-vs-LSTM/blob/main/Pollution-times-series.ipynb)



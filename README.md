# Comparison of ARIMA and LSTM for time series forecasting

We compare the performance of traditional ARIMA models and Recurrent Neural Networks (LSTMs) for time series forecasting.

There are numerous ways of formulating a time series forecasting problem depending on the business scenario.

We simulate a scenario where a time series model is trained and deployed, and we monitor its test performance over time. 
The model is not retrained during this testing phase.
We produce a one-step forecast at each time step t and we observe a new data point that is added to the training dataset to compute the next step forecast.

This monitoring strategy produce a sequence of one-step forecasts, which can be compared against the true test observations. 

As a measure of performance of the models, we use **MAPE** (mean absolute percentage error). 

We perform the analysis on two datasets:

1. **Electricity consumption** (trend and seasonality)

    Jupyter Notebook: [Electricity-consumption-times-series.ipynb](https://github.com/jankova/Time-Series-ARIMA-vs-LSTM/blob/main/Electricity-consumption-times-series.ipynb)


2. **Air pollution** (no clear trend or seasonality)

    Jupyter Notebook: [Pollution-times-series.ipynb](https://github.com/jankova/Time-Series-ARIMA-vs-LSTM/blob/main/Pollution-times-series.ipynb)



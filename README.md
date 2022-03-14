# Comparison of ARIMA and LSTM for time series forecasting

We compare the performance of traditional ARIMA models and Recurrent Neural Networks (LSTMs) for time series forecasting.




To compare the different models, we will monitor their performance for one-step forecasting (without model retraining at each step). 
This simulates the scenario where a time series model is trained and deployed, and we want to monitor its performance over time, while at each time step we collect a new data point. This new data point will augment the training dataset for the next step forecast. 


This monitoring strategy produces a sequence of one-step forecasts, which can be compared against the true test observations. 

As a measure of performance of the models, we will use the mean absolute percentage error (MAPE). 



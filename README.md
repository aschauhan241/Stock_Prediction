# Stock_Prediction
For Level A :-
Objective: The objective of this project is to create a predictive model using the ARIMA (AutoRegressive Integrated Moving Average) algorithm to forecast the stock price (Close column) of ASIANPAINTs, an Indian company listed in the Nifty50 stock market data.

Data Preparation and Analysis: The dataset was imported from Kaggle, containing historical stock prices of ASIANPAINTs. The 'Date' column was set as the index to facilitate time series analysis. Various statistical tests, such as the Augmented Dickey-Fuller (ADF) test, were performed to check for stationarity in the data, and differencing was applied to achieve stationarity when necessary.

ARIMA Model: The ARIMA algorithm was selected for time series forecasting. The order of differencing (p, d, q) was determined using the ADF, KPSS, and PP tests. The ARIMA model was trained using data from 2000 to 2007 to predict the stock prices for the year 2008 and data from 2009 to 2015 for the year 2016. Root Mean Squared Error (RMSE) was chosen as the accuracy metric to evaluate the model's performance.

Results and Visualization: The ARIMA model successfully made predictions for the stock prices in 2008 and 2016. The actual and predicted stock prices were visualized in separate plots for both years. The RMSE values for the predictions in 2008 and 2016 were calculated and reported, providing an indication of the accuracy of the model's forecasts. and when compared with the test data for that particular years it seems like arima is not able to model the data effectively.


For Level B:- Similar Objective and Dataset as above but we have to make use of LSTM model and optimize it.
The LSTM model is constructed with a fixed network layout, including a single LSTM layer, dropout layer to prevent overfitting, and a dense output layer.
Hyperparameter optimization is performed using random search, exploring different learning rates and optimizers (adam, rmsprop, sgd).
The model is trained on data from the years 2000-2007 and evaluated using data from 2008, with the goal of finding the best-performing model based on the lowest MSE (Mean Squared Error).
The optimized LSTM model is used to make predictions for the years 2008 and 2016.
Predictions are inverse transformed using MinMaxScaler to obtain actual stock prices.
The results are plotted with the actual stock prices to visualize the model's performance in predicting the "Close" values for ASIANPAINTS in 2008 and 2016.

It gives much better results than the first model used ie - Arima

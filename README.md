# Multivariate Time Series Forecasting

![stock_pred](https://github.com/jmayank23/MultivariateTimeSeriesForecasting/assets/27727185/4dd8b83c-2d7d-472b-8be6-be3f43bbb7c0)

**TODO:** Look at Quantile Regression

## Overview

This repository contains a robust and versatile model to perform multivariate time series forecasting to analyze and predict stock market data. 

One of the core aspects of this project is its emphasis on generalizability and ease of use. The code has been meticulously structured and fine-tuned to provide users the capability to modify various parameters, and still ensure perfect running of the code along with all visualizations. 

Key features that users can customize include:

1. `features to train on` and `features to predict`: This unique feature offers users the freedom to choose the specific features they want to train their model on and also the features they want the model to predict. This allows for a high degree of customization and control, enabling users to make the model as specific or as broad as they want it to be.

2. `n_past`: This allows you to set the number of past days of data that the model should consider when making a prediction. By tweaking this value, you can control the extent of historical data being factored into your predictions.

3. `n_future`: This allows you to specify the number of days into the future that the model should predict. Whether you are interested in short-term or long-term predictions, this feature gives you the flexibility to adjust the model's forecasting horizon as needed.

4. `start` and `end` dates for the stock data: This feature lets you define the specific timeframe for the data you wish to analyze. No matter how vast or limited the date range may be, the code ensures seamless data extraction and analysis.

## Code Description

The script includes the following steps:

1. **Downloading Stock Data:** The data is downloaded from Yahoo Finance for a specific ticker within a specific date range. 

2. **Data Exploration:** The script generates various plots to help visualize the data, including line plots for stock adjusted closing prices and volume, as well as plots showing stock high, low, and spread.

3. **Data Processing:** The data is then processed and scaled using StandardScaler. The past 'n' days are used to predict the 'n_future' days. The data is also split into training and testing sets.

4. **Machine Learning:** Different deep learning models are trained on the data, including an LSTM model, a CNN model, an Ensemble model which uses both LSTM and CNN, and a hybrid LSTM Conv model. These models are then used to predict future prices.

5. **Training:** The models are trained using a predefined number of epochs, and the loss for both training and validation datasets is plotted to observe how the models perform.

6. **Predicting and Validating:** The models are used to predict future stock prices for specific dates, and the results are compared against the actual prices to assess the model's accuracy.


## Usage

The parameters at the beginning of the script can be adjusted based on your specific use case. You may want to adjust the ticker for which you want to predict stock prices, the number of past days to use for the prediction (n_past), the number of future days to predict (n_future), and which features you want to use for training and prediction.

After setting these parameters, simply run the script, and it will handle data download, preprocessing, model training, and prediction. 

## Caveats

It is important to understand that stock price prediction is a complex task with many influencing factors. The models and techniques used here are basic examples and may not be able to accurately predict stock prices due to the randomness and unpredictability in stock market data. Therefore, these predictions should not be used for real-world trading without further enhancements and evaluations.

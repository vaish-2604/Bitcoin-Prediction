# Bitcoin-Prediction

Predicting Bitcoing prices can be challenging due to its high volatility. So, I will be comparing the performance of various ML models.

## Dataset : from 2014-09-17  to  2022-02-19

The data set has 9 columns:
      1. Date
      2. Opening price
      3. Closing price
      4. Highest price
      5. Lowest price
      6. Adjusted close
      7. Volume

## Models:
###      1. ARIMA:
            a. Effective for capturing linear trends in time series data.
            b. Low computational cost.
            c. Might not be great for seasonal data and extremely volatile data like bitcoin prices.
###      2. SARIMAX:
            a. Effective for capturing linear trends and seasonal patterns in time series data.
            b. Low computational cost.
            c. It struggles with non linear patterns which may pose a probelm due to the volatility in our data.
###      3. LSTM :
            a. It is specialized for sequential and time dependent data.
            b. Can learn long term dependencies which is beneficial for capturing complex temporal patterns.
            c. Handles non linear relationships well.
            d. Sensitive to hyperparameter and therefore prone to overfitting.
            e. Requires significant computational resources and time to train.
###      4. Gradient Boost Regressor:
            a. Highly flexible and powerful with non linear relationships.
            b. Fast to train.
            c. Doesn’t inherently handle time dependencies, so you must manually add lagged features and other temporal indicators.
            d. Can overfit if the dataset is noisy or the model is overly complex.
###      5. Random Forest Regressor:
            a. Works well with a mix of features and is generally robust to overfitting on complex datasets.
            b. Performs well with non-linear relationships and noisy data, making it adaptable to price prediction.
            c. May struggle with high volatility, as it averages over predictions, potentially missing sharp price movements.
            d. More prone to underfitting than boosting algorithms in complex scenarios.


## Enhancing Dataset

For now, I'm working only with date, OLHC prices and volume. We can add features like Daily Returns, Moving Averages, Volatility indicators and MACD for better models. 

# Bitcoin-Prediction

Predicting Bitcoing prices can be challenging due to its high volatility. So, I will be comparing the performance of various ML models.

## Literature Survey

https://library.gito.de/wp-content/uploads/2021/08/B4_manuscript_final.pdf
https://www.ijfmr.com/papers/2023/6/10384.pdf
https://www.granthaalayahpublication.org/ijetmr-ojms/index.php/ijetmr/article/view/IJETMR21_A05_2586/771
https://jfin-swufe.springeropen.com/articles/10.1186/s40854-024-00643-1#:~:text=work%20are%20presented.-,Literature%20review,the%20characteristics%20of%20the%20output.
https://www.mdpi.com/1911-8074/16/1/51

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
###      4. XgBoost:
            a. Highly flexible and powerful with non linear relationships.
            b. Fast to train.
            c. Doesn’t inherently handle time dependencies, so you must manually add lagged features and other temporal indicators.
            d. Can overfit if the dataset is noisy or the model is overly complex.
###      5. Random Forest:
            a. Works well with a mix of features and is generally robust to overfitting on complex datasets.
            b. Performs well with non-linear relationships and noisy data, making it adaptable to price prediction.
            c. May struggle with high volatility, as it averages over predictions, potentially missing sharp price movements.
            d. More prone to underfitting than boosting algorithms in complex scenarios.
###      6. Transformer models:
            a. Excellent for long-range dependencies in time series data due to its self-attention mechanism.
            b. Highly flexible, as it can handle multiple input features without extensive preprocessing.
            c. Can capture both trend and complex patterns in a single framework.
            d. Very computationally demanding, requiring more memory and time compared to LSTM or traditional models.
            e. Complex to set up and tune effectively, as it requires more intricate architecture and parameter choices.
###      7. Hybrid Models: 
            a. Combines the strengths of linear and non-linear models, where SARIMA captures trend and seasonality, and the ML model (like XGBoost or Random Forest) captures the residuals or complex patterns.
            b. Computationally more intensive, as it involves training two models and combining predictions.

## Enhancing Dataset

For now, I'm working only with date, OLHC prices and volume. We can add features like Daily Returns, Moving Averages, Volatility indicators and MACD for better models. 

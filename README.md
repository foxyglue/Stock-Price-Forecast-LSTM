# Stock-Price-Forecast-LSTM

A case study analyzing and predicting AMD and Apple stock prices from Yahoo Finance data until April 1st 2020 with the LSTM model.

## Steps:
1. **EDA**
    - Exploring and preprocessing data. Separating data into and output with window size = 5.
2. **Preprocessing data**
    - Separating data into horizon = 1, window size = 5.
    - Changing 'Time' data type
    - Splitting data into train (80%), validation (10%), test (10%)
3. **Modelling**
    - Base model:
        - 1 LSTM layer with 50 units and ReLu activation
        - Dense layer optimized with ADAM
    - Tuned Model:
        - Early stopping has been implemented to prevent overfitting and save training time.
        - Dropout is applied to prevent overfitting by randomly deactivating a number of neurons during training.
        - Addition of Layers and Units: More units were added to the first LSTM layer, and another LSTM layer was added with Dropout in between. This helps the model capture more complex temporal patterns and further reduces overfitting.
4. **Model Evaluation**
    - Analyzing model performance based on MAE, RMSE, and MAPE metrics


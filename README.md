<div align="center">
<h1>
    Bitcoin Price Prediction
</h1>

<h4>
 This research aims to predict the price of Bitcoin accurately, focusing on the direction of its price movement.
</h4>

## <div align="center">Overview</div>

Bitcoin presents an interesting parallel to this as it is a time series prediction problem in a market still in its transient stage. As a result, there is high volatility in the market and this provides an opportunity in terms of prediction. In addition, Bitcoin is the leading cryptocurrency in the world with adoption growing consistently over time. Due to the open nature of Bitcoin it also poses another paradigm as opposed to traditional financial markets. 
WAGMI 

## <div align="center">Dataset</div>

The dataset contains various attributes such as the opening price, closing price, highest price, lowest price, volume, and market capitalization of Bitcoin for each day.

1. “Open” : Opening price of bitcoin on a particular day.
2. “Close” : Closing price of bitcoin on a particular day.
3. “High” : Highest price of bitcoin on a particular day.
4. “Low” : Lowest price of bitcoin on a particular day.
5. “Volume” : Volume of bitcoin in the market on a particular day.
6. “Market Cap” : Market capitalization price of bitcoin on a particular day.

The dataset was preprocessed, and additional features were created, including the closing price of Bitcoin after 10 days and the average value of the selected attributes. The dataset was split into training and testing sets (85:15 ratio). Regression models were then applied to predict the future price.

## <div align="center">Model</div>

I experimented with different regression models and obtained their respective R-squared scores. The models used were:
1. Linear Regression: R-squared score of 0.9595 
2. KNeighborsRegressor: R-squared score of 0.9828 (Hyperparameters: n_neighbors=12, weights='distance', p=2, leaf_size=36)
3. RandomForestRegressor: R-squared score of 0.9815 (Hyperparameters: n_estimators=227, random_state=0, max_features=0.3, max_depth=15, criterion='absolute_error', min_samples_split=2, min_samples_leaf=3)
4. DecisionTreeRegressor: R-squared score of 0.9804 (Hyperparameters: random_state=0, max_features='log2', max_depth=14, criterion='friedman_mse', splitter='random', min_samples_split=5, min_samples_leaf=2)
5. XGBRegressor: R-squared score of 0.9827 (Hyperparameters: n_estimators=40, max_depth=6, learning_rate=0.25)
6. LGBMRegressor: R-squared score of 0.9818 (Hyperparameters: num_leaves=120, max_depth=5, n_estimators=120, learning_rate=0.13, cosample_bytree=0.7, random_state=0)

Pipeline: The top five models, including KNeighborsRegressor, RandomForestRegressor, DecisionTreeRegressor, XGBRegressor, and LGBMRegressor, were selected for implementation in a pipeline.


Results: The final R-squared score achieved through the pipeline was 0.9838, indicating a high level of accuracy in predicting the future price of Bitcoin.

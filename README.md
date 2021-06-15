# **THE DENARII TRADER: - motto - A daytrader trying to make a “day's wage” from a desktop brain!!**

![MLSP](https://user-images.githubusercontent.com/78338890/121461642-40314d80-c97d-11eb-9045-43d68de8d24b.jpg)

## *OVERVIEW*

Machine learning is a subset of artificial intelligence involved with the creation of algorithms that can change itself without human intervention to produce an output by feeding itself through structured data. In this project, we created a model that makes a 7-day prediction for a particular stock/ticker using different machine learning models.We were able to extract data from Yahoo Finance and run it through our prepared model to get the predictions that help us make buying and selling decisions on our stocks.

## *DATASET AND FEATURES*

The first step is to intitialize imports and prepare the data. We load the dataset and calculate the indicators- RSI, MACD and CMF. The dataset was downloaded from the YahooFinance. 

#### *Initial imports*

<img width="641" alt="Screen Shot 2021-06-14 at 22 42 44" src="https://user-images.githubusercontent.com/78338890/121984985-ef956800-cd61-11eb-9645-66f6bded26d1.png">

<img width="280" alt="Screen Shot 2021-06-14 at 22 42 59" src="https://user-images.githubusercontent.com/78338890/121985006-f6bc7600-cd61-11eb-95ff-7505b456fdf6.png">



#### *Identifying the ticker we want to analyze (in our case, AAPL) and importing data from Yahoo Finance*

<img width="492" alt="Screen Shot 2021-06-14 at 22 44 37" src="https://user-images.githubusercontent.com/78338890/121985127-24a1ba80-cd62-11eb-9462-1de8237c065c.png">



#### *Calculating and adding Indicators- RSI, MACD, CMF and Bollinger band signals to create our dataframe df* 

- RSI indicator (Relative Strength Index) is an indicator that we can use to measure if given asset is priced to high or too low. It is intended to chart the current and historical strength or weakness of a stock or market based on the closing prices of a recent trading period.

- MACD indicator stands for Moving Average Convergence Divergence. As the name suggests, indicator is evaluating two moving averages and the relation between them. It is calculated by subtracting the 26-period exponential moving average (EMA) from the 12-period EMA.

- Chaikin Money Flow (CMF) is a technical analysis indicator used to measure Money Flow Volume over a set period of time. Money Flow Volume (a concept also created by Marc Chaikin) is a metric used to measure the buying and selling pressure of a security for single period.

- Bollinger Bands are a type of price envelope developed by John BollingerOpens in a new window. (Price envelopes define upper and lower price range levels.) Bollinger Bands are envelopes plotted at a standard deviation level above and below a simple moving average of the price. Because the distance of the bands is based on standard deviation, they adjust to volatility swings in the underlying price. Bollinger Bands use 2 parameters, Period and Standard Deviations, StdDev. The default values are 20 for period, and 2 for standard deviations, although you may customize the combinations. Bollinger bands help determine whether prices are high or low on a relative basis. They are used in pairs, both upper and lower bands and in conjunction with a moving average. Further, the pair of bands is not intended to be used on its own. Use the pair to confirm signals given with other indicators.

<img width="1274" alt="Screen Shot 2021-06-14 at 22 46 34" src="https://user-images.githubusercontent.com/78338890/121985250-6894bf80-cd62-11eb-9dac-75de637170b7.png">


##### *Plotting of the three indicators*

<img width="777" alt="Screen Shot 2021-06-14 at 22 47 46" src="https://user-images.githubusercontent.com/78338890/121985391-a8f43d80-cd62-11eb-8b92-b2066a61561f.png">

<img width="766" alt="Screen Shot 2021-06-14 at 22 48 01" src="https://user-images.githubusercontent.com/78338890/121985408-af82b500-cd62-11eb-9e38-892a2e52237b.png">

##### *Cleaning dataframe and saving as a csv*

<img width="1006" alt="Screen Shot 2021-06-14 at 22 49 25" src="https://user-images.githubusercontent.com/78338890/121985508-dc36cc80-cd62-11eb-98b3-65618eadc0f6.png">


## *TRAINING MODELS*

### *MODEL 1- Forecasting stock prices using LSTM*

- Set Index Date as string type.
- Select features from the dataset that are to be used for training and predicting. In our case, Columns 0 to 5.
- Create array for LSTM model to run
<img width="364" alt="Screen Shot 2021-06-14 at 22 58 37" src="https://user-images.githubusercontent.com/78338890/121986184-16ed3480-cd64-11eb-974a-3c174d7c4c6b.png"> 
- Scale the features and create a datastructure with 90 timestamps and 1 output.
- Now, initialize the LSTM based Neural Network
<img width="550" alt="Screen Shot 2021-06-14 at 22 59 39" src="https://user-images.githubusercontent.com/78338890/121986499-9a0e8a80-cd64-11eb-9d4a-e3692966906e.png">

- Start training
<img width="827" alt="Screen Shot 2021-06-14 at 23 03 56" src="https://user-images.githubusercontent.com/78338890/121986706-01c4d580-cd65-11eb-8aa3-97209e37b3bd.png">

- Generate list of sequence of days for predictions
- Convert Pandas Timestamp to Datetime object
- Perform predictions 
<img width="768" alt="Screen Shot 2021-06-14 at 23 45 31" src="https://user-images.githubusercontent.com/78338890/121989792-b4e3fd80-cd6a-11eb-9ca7-4d290073a892.png">
- Plotting predicted stock price
<img width="1011" alt="Screen Shot 2021-06-14 at 23 48 40" src="https://user-images.githubusercontent.com/78338890/121990062-291ea100-cd6b-11eb-8a5c-22a1d6395fa0.png">

### *MODEL 2- Forecasting stock prices using ARIMA*

<img width="1010" alt="Screen Shot 2021-06-14 at 23 55 32" src="https://user-images.githubusercontent.com/78338890/121990707-3720f180-cd6c-11eb-9635-78143c6c1a3f.png">
<img width="1004" alt="Screen Shot 2021-06-14 at 23 55 43" src="https://user-images.githubusercontent.com/78338890/121990722-3e47ff80-cd6c-11eb-87c3-dbe7088d3d90.png">
<img width="1022" alt="Screen Shot 2021-06-14 at 23 55 58" src="https://user-images.githubusercontent.com/78338890/121990732-43a54a00-cd6c-11eb-857d-4632022482a8.png">
<img width="1019" alt="Screen Shot 2021-06-14 at 23 56 19" src="https://user-images.githubusercontent.com/78338890/121990749-4a33c180-cd6c-11eb-93fc-9c6e4d5d3d53.png">
<img width="1015" alt="Screen Shot 2021-06-14 at 23 56 32" src="https://user-images.githubusercontent.com/78338890/121990757-515acf80-cd6c-11eb-9850-c5c300cd7e3e.png">
<img width="362" alt="Screen Shot 2021-06-14 at 23 59 05" src="https://user-images.githubusercontent.com/78338890/121990880-8bc46c80-cd6c-11eb-8b49-2057c9457208.png">

- Creating dataframes of predicted close prices (for next 7 days), defining start date as tomorrow and a dateframe with just the Dates (of next 7 days).
- Concatenate the two dataframes into one and rename respective columns to Date and Predicted price.

<img width="385" alt="Screen Shot 2021-06-15 at 00 06 09" src="https://user-images.githubusercontent.com/78338890/121991373-8d426480-cd6d-11eb-83da-c8f18f6061f3.png">

<img width="1033" alt="Screen Shot 2021-06-15 at 00 05 00" src="https://user-images.githubusercontent.com/78338890/121991292-5ec48980-cd6d-11eb-86e0-a9ae155b2f26.png">



## *RESULTS FROM THE PREDICTIONS*

After running the test data on the LSTM model, the predictions were pretty close to the actual readings. As you can see in the graph here, the predicted and the actual values are going hand in hand.


(graphs to be added here)



### *SOURCES*

- https://tcoil.info/compute-rsi-for-stocks-with-python-relative-strength-index/
- https://tcoil.info/compute-macd-indicator-for-stocks-with-python/
- https://tcoil.info/predict-stock-price-trend-with-machine-learning-random-forest-scikit-python/ 
- https://github.com/vb100/multivariate-lstm/blob/master/LSTM_model_stocks.ipynb
- https://www.tradingview.com/support/solutions/43000501974-chaikin-money-flow-cmf/
- https://www.fidelity.com/learning-center/trading-investing/technical-analysis/technical-indicator-guide/bollinger-bands



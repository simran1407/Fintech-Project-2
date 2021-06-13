# **THE DENARII TRADER: - motto - A daytrader trying to make a “day's wage” from a desktop brain!!**

![MLSP](https://user-images.githubusercontent.com/78338890/121461642-40314d80-c97d-11eb-9045-43d68de8d24b.jpg)

## *OVERVIEW*

Machine learning is a subset of artificial intelligence involved with the creation of algorithms that can change itself without human intervention to produce an output by feeding itself through structured data. In this project, we created a model that makes a 7-day prediction for a particular stock/ticker using different machine learning models.We were able to extract data from Yahoo Finance and run it through our prepared model to get the predictions that help us make buying and selling decisions on our stocks.

## *DATASET AND FEATURES*

The first step is to intitialize imports and prepare the data. We load the dataset and calculate the indicators- RSI, MACD and CMF. The dataset was downloaded from the YahooFinance. 

#### *Initial imports*
<img width="413" alt="imports" src="https://user-images.githubusercontent.com/78338890/121817980-7a873d00-cc52-11eb-9d4d-95eb699162f5.png">

#### *Identifying the ticker we want to analyze (AAPL) and importing data from Yahoo Finance*
<img width="687" alt="Screen Shot 2021-06-13 at 14 27 46" src="https://user-images.githubusercontent.com/78338890/121818161-917a5f00-cc53-11eb-89b8-a3ca131e3765.png">

#### *Calculating and adding Indicators- RSI, MACD, CMF and Bollinger band signals to create our dataframe df*
<img width="1048" alt="Screen Shot 2021-06-13 at 14 41 21" src="https://user-images.githubusercontent.com/78338890/121818496-888a8d00-cc55-11eb-9c90-552ca9ece93c.png">

   ##### *Plots of the three indicators*
<img width="927" alt="Screen Shot 2021-06-13 at 14 39 34" src="https://user-images.githubusercontent.com/78338890/121818454-3f3a3d80-cc55-11eb-99b0-39ce27a33ec2.png">

  ##### *Original dataframe-df, saved as a csv*
  
  <img width="1306" alt="Screen Shot 2021-06-13 at 16 59 00" src="https://user-images.githubusercontent.com/78338890/121821730-d5c42a00-cc68-11eb-8fba-42a6448d92e1.png">
<img width="1041" alt="Screen Shot 2021-06-13 at 16 59 53" src="https://user-images.githubusercontent.com/78338890/121821736-e379af80-cc68-11eb-9c81-65683448ec29.png">

  
  
  
  
#### *Creating 2 new dataframes, df2 and df3 using original df*

### *df2*
 <img width="873" alt="Screen Shot 2021-06-13 at 17 18 09" src="https://user-images.githubusercontent.com/78338890/121822134-6c91e600-cc6b-11eb-8396-ff1c37b90dbf.png">
<img width="661" alt="Screen Shot 2021-06-13 at 17 21 05" src="https://user-images.githubusercontent.com/78338890/121822204-c4c8e800-cc6b-11eb-81cf-07ae226c0214.png">


### *df3*
<img width="646" alt="Screen Shot 2021-06-13 at 17 26 04" src="https://user-images.githubusercontent.com/78338890/121822314-79630980-cc6c-11eb-8abd-416b7ffb34ef.png">







### *We used the following Machine Learning algorithms for our Stock Prediction model.


## *RESULTS FROM THE PREDICTIONS*

After running the test data on the LSTM model, the predictions were pretty close to the actual readings. As you can see in the graph here, the predicted and the actual values are going hand in hand.


(graphs to be added here)



### *SOURCES*

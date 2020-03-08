# Crypto-Project
## Research Question:
Is it possible to accurately predict the changes in cryptocurrency valuation in the market using the previous days data? Are we able to make a profit off these predictions?

## Data:
In order to acquire the necessary data, I found the top cryptocurrencies off of Yahoo Finance with a market valuation of over $1 billion. After scraping the list using BeautifulSoup, I used the AlphaVantage API to retrieve the market data for each currency in regard to the USD. The AlphaVantage API returned the historic prices for the open, close, high, low of the day, as well as the volume of trades. With this information, I was able to do some data manipulation in order to create pertinent data points such as volatility, profit, and sing and exponential moving averages. These data points were important to make inferences on the type of trading day that could influence the profit for the following day. 

## Modeling:
Initially, I had hoped to use an ARIMA model to try to predict the fluctuations of the stock prices. However, the white noise inherent in the data proved to be greater than the seasonality and trend, and did not provide consistent predictions that could be used to determine profitability. Instead, I attempted to classify whether a day would be profitable (if the close price was greater than the open) using the day before's market movement. The idea here was that based off the sale volume (the amount of trades on a particular currency), the volatility (difference between the high and low price of the day) and other trends from the day before, the model would determine if the stock was at an under or over valued price.

### Classification Modeling:

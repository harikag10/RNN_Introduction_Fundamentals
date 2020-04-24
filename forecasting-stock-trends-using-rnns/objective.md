# Objective

Predicting how the stock market will perform is one of the most difficult things to do. There are so many factors involved in the prediction – physical factors vs. psychological, rational and irrational behaviour, etc. All these aspects combine to make share prices volatile and very difficult to predict with a high degree of accuracy.

Here we are trying to predict the stock price of Apple. It's pretty challenging to predict since there is Brownian Motion which states that we couldn't predict future variations in stock prices using past data but its actually possible to predict trends in data

* We will make an LSTM Model that will try to capture upward and downward trends in the selected stock price
* We are gonna implement a Stacked LSTM and dropout layers to avoid overfitting.

We will try to predict the last 60 days using the data from 2000 to 2019.


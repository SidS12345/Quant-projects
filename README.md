## Quant-projects
A collection of quant projects I have built to deepen my understanding of the field. I will complete a series of projects that each focus on different aspects of quant finance, in order to get the best possible general understanding. I am completing these projects semi-simultaneously, so in each project there are a few next steps that I intend to take as I develop these projects further.
In all projects, the list of stocks is a list called tickers - to run the programs on different sets of stocks, simply update the list tickers.

# Project 1 - Portfolio Management
In this project, I use SciPy optimization to determine how best to split capital across a portfolio to optimize its sharpe ratio. This project uses historical stock data to interpret mean log returns of a range of stocks, and applying constraints (e.g. no shorting, maximum 40% of capital placed in a single stock) to calculate the optimal portfolio on these stocks

Next steps - add a risk dashboard (e.g. max drawdown, rolling sharpe ratio), track portfolio performance over time, simulate performance using Monte Carlo simulation

# Project 2 - Asset Price Prediction
In this project, I use extensive feature engineering on historical stock data (using python's technical analysis library for financial data) to create an ML model that predicts next day close prices of a range of stocks. Then, I implement a very simple trading strategy using these predicted prices (buy if prediction is above close price today, else sell). This helps give an indicator as to which stocks are able to perform well. Initially, I just used linear regression to predict prices, but I have now added a range of different types of ML models so that we can also evaluate performance of different ML models for stock prediction. 

Next steps - compare validation data predictions vs actuals, investigate how sensitive model performance is to the random state of train test split, evaluate performance of each ML model using metrics for prediction accuracy and profits

# Project 3 - Cointegrated Pairs Trading Strategy
In this project, I now aim to develop an actual trading strategy. My strategy relies on the cointegration of pairs of stocks - some pairs of stock prices will follow each other closely, remaining within a certain range of each other. These pairs of stocks drifting apart in price then signals a trading opportunity, assuming the prices will revert back to being close to each other. In this, I am mainly analysing tech sector stocks, though this can be done for any sector. 

Next steps - Generate spreads for cointegrated pairs, and create a trading signal that indicates when to buy and sell


# TradingAlgorithm
1. Unsupervised-learning trading strategy that utilizes S&amp;P 500 stocks for portfolio optimization.
- Download SP500 stocks prices data.
- Calculate different technical indicators and features for each stock.
- Aggregate on monthly level and filter for each month only top 150 most liquid stocks.
- Calculate monthly returns for different time-horizons to add to features.
- Download Fama-French Factors and calculate rolling factor betas for each stock.
- For each month fit a K-means clustering model to group similar assets based on their features.
- For each month select assets based on the cluster and form a portfolio based on Efficient Frontier max sharpe ratio portfolio optimization.
- Visualize the portfolio returns and compare to SP500 returns.

2. Twitter Sentiment trading strategy to rank NASDAQ stocks based on social media engagement (benchmarking performance against QQQ returns).
- Load NASDAQ stocks twitter sentiment data.
- Calculate a quantitative feature of the engagement ratio in Twitter of each stock.
- Every month rank all stocks and construct an equal-weight portfolio.
- Compare it against NASDAQ performance.

3. Intraday Investment Strategy leveraging the GARCH model for enhanced market analysis and decision-making (to profit from short-term price movements).
- Load simulated daily data and simulated 5-minute data.
- Define function to fit GARCH model and predict 1-day ahead volatility in a rolling window.
- Calculate prediction premium and form a daily signal from it.
- Merge daily data with intraday data and calculate intraday indicators to form the intraday signal.
- Generate the position entry and hold until the end of the day.
- Calculate final strategy returns.
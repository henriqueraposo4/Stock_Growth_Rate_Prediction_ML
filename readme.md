Stock Growth Rate Prediction
============================
The goal of this project is to predict the 10 week growth rate of US stocks based on historical data and financial metrics. 

## About the data
The data was obtained through a Python script that leverages Yahoo Finance API to extract the financial information and 2-year historical price of the stocks in the Russell 1000 index. This index lists the top 1000 companies by market capitalization in the United States. From this, two tables are produced, one with the financial data where each row is a ticker symbol and the columns are the metric, and a second table which contains the historical stock price values, in which each row is a day and each column a ticker symbol. The financial information is from September 24th, 2024, and the historical data ranges from September 24th, 2024 to September 26th, 2022.

## About the model
The prediction was done by utilizing XGBoost, a powerful model that creates multiple decision trees, where each new tree tries to minimize the error made by previous trees. By multiple interactions, the model starts with a decision tree, it calculates the error in prediction, then creates a new model that attempts to predict the residuals or assign higher weights to the samples that were predicted incorrectly in the previous round. This step is repeated multiple times until the model has no further improvement or when it reaches the maximum number of trees to create.

## Results
When compared to the actual growth rates, the predictions were more conservative, with less fluctuation. However, an analysis of the 10 stocks with the highest predicted 10-week growth rates shows that 7 out of the 10 are also among the top 10 stocks with the highest actual growth rates, with the remaining three were still in the top 30. This suggests that while the predicted growth rates were lower, the model successfully identified the stocks that experienced the highest growth.

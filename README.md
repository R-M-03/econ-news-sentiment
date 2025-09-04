# S&P 500 Sentiment Analysis
Analyzing the relationship between news headline sentiment and S&P 500 price movements (2008–2024) using Python, TextBlob, and machine learning.

## Motivation
- Investigate how daily news sentiment correlates with S&P 500 returns.
- Compare effects during crises (2008 recession, COVID-19 crash).
- Build a basic predictive model for market direction using sentiment features.

## Dataset
- Headlines from Kaggle: S&P 500 with Financial News Headlines (2008–2024) and Financial News Headlines Data
- Prices: Daily S&P 500 closing prices (from S&P 500 dataset)
- Features derived: sentiment score, rolling sentiment, lagged sentiment (yesterday's sentiment), daily returns, market direction (up = 1, down = 0) 

## Methods
- Sentiment analysis using TextBlob
- Aggregated daily sentiment, created 5-day rolling average
- Calculated daily returns and market direction
- Visualized trends and crisis comparisons
- Built a logistic regression model predicting market up/down using lagged and rolling sentiment

## Key Results
- Correlations between sentiment and returns (full sample, 2008, COVID)
- Overall, daily sentiment shows a very weak correlation with returns.
- Sentiment had a slightly stronger positive correlation during the COVID crash compared to the 2008 recession, indicating market reactions were     more sensitive to news in 2020.
- Crisis comparison plots
- Model performance:
    - Accuracy: ~51%
    - Confusion matrix and classification report saved in `results/`
- Actual up/down distribution saved in `results/`

## Repository Structure
- `data/` – raw data files and cleaned datasets (headlines and prices)
- `notebooks/` – Jupyter notebooks for analysis and modeling
- `results/` – final plots, summary tables, and model outputs

## Next Steps
- Experiment with more features: volatility, lagged returns, additional sentiment metrics
- Try advanced models (Random Forest, XGBoost) to capture nonlinear patterns and develop more actionable insights
- Consider resampling techniques to address class imbalance

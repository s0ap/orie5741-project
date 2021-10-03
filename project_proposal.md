
# Project Proposal

## What is our aim?
Financial markets have very complex structures that are highly nonlinear with a low signal-to-noise ratio which makes predicting short term asset returns difficult. However, factors like slow decay of autocorrelation in absolute returns (i.e. generally, returns tend to be more correlated with the most recent past returns and and less correlated with longer dated past returns), tend to suggest that volatility is to a large extent predictable. The aim of this project is to predict/forecast both weekly and daily realized volatility — in order to capture important events which may get muted when averaging out over a larger time frame (weekly). We plan to analyseperformance for Machine Learning based volatility forecasting and the forecast's accuracy.

## What data are we using?
- We will be using 1 minute tick data for S&P 500 from Kaggle (https://www.kaggle.com/gratefuldata/intraday-stock-data-1-min-sp-500-200821). The data is from 22 January 2008 to 6 May 2021. This dataset covers the financial crisis of 2008 to 2009, the European sovereign debt crisis, Greece brankruptcy, several rounds of dispute about the U.S. debt ceiling, and the flash crashes of 6 May 2010 and 24 August 2015 as well as the recent Covid crisis in 2020 and the market evolution after it.

- The explanatory variables/features that we will explore can be broadly classified as:
  - Macroeconomic variables: 
    - the CBOE volatility (VIX) index
    - the Hang Seng stock index squared log-return (HSI) (or any other index - based on highest economic exposure of stocks included in the S&P 500 index), 
    - the ADS Business Conditions index
    - the US 1-month T-bill rate (US1M)
    - the Economic Policy Uncertainty (EPU) index. 
    - NBER based Recession Indicators
  - Volatility lag variables: To study the effects of tagging on additional explanatory variables. Contains the daily, weekly, and monthly lag of realized variance. 
  - Index level variables: 
    - 1-week index momentum (M1W)
    - dollar trading volume (DVOL)
    - We can also look into S&P ex dividend dates

This is a preliminary feature list based on our economic intuition and the variables are subject to change on further data analysis.
 
## Why is this important?
With its crucial role in asset pricing, portfolio allocation, and risk management, volatility forecasting has attracted a large amount of attention. Especially during recent times when volatility products created a havoc in the stock market in March 2020, it makes sense to forecast the volatitlity so that we are able to pick up signals in future and be able to avoid such chaos. We believe that covering the crisis periods (from 2008-2020) will help us uncover questions about the volatility during turbulent times as well as normal times.

## How will Machine Learning help?
Conventional linear regression models fail to predict accurately when the input variables are strongly correlated or have a low signal-to-noise ratio, or the underlying structure is highly nonlinear. Machine Learning can deal with highly nonlinear structured data that often appear in volatility in financial markets. They can also extract valuable information from a large amount of data by looking at a broad feature space; linear regression models often fail to do so. Additionally, they are significantly resistant to a substantial amount of noise added to distort the original dataset, in contrast to the linear regression. So, we believe machine learning models of varying complexities would give some meaningful insights on market index volatility prediction.

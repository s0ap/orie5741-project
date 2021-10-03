
# Project Proposal

## Project Question
- Why can we predict volatility - and is it possible?
- Our goal: Predict both daily and weekly realized volatility. Computation of time serios of realised variance will be done at weekly as well as daily level so as to catch any signals which might get missed during the computation of daily realised variance.

## Project Dataset
- We will be using 1 minute tick data for S&P 500 from Kaggle (https://www.kaggle.com/gratefuldata/intraday-stock-data-1-min-sp-500-200821). The data is from 22 January 2008 to 6 May 2021. This dataset covers the financial crisis of 2008 to 2009, the European sovereign debt crisis, Greece brankruptcy, several rounds of dispute about the U.S. debt ceiling, and the flash crashes of 6 May 2010 and 24 August 2015 as well as the recent Covid crisis in 2020 and the market evolution after it.

- The explanatory variables/features we will be exploring are broadly classified as:
  - Macroeconomic variables: 
    - the CBOE volatility (VIX) index
    - the Hang Seng stock index squared log-return (HSI) (or any other index - based on highest economic exposure of stocks included in the S&P 500 index), 
    - the Aruoba, Diebold, and Scotti (2009) business conditions (ADS) index, 
    - the US 1-month T-bill rate (US1M)
    - the Economic Policy Uncertainty (EPU) index from Baker, Bloom, and Nicholas (2016). 
    - Also look at NBER based Recession Indicator and industrial output/production indicators (FRED)
  - Volatility lag variables: To study the effects of tagging on additional explanatory variables. Contains the daily, weekly, and monthly lag of realized variance. 
  - Index level variables: 
    - 1-week index momentum (M1W)
    - dollar trading volume (DVOL)
    - We can also look into S&P ex dividend dates

## Importance of the Question
 We believe that covering the crisis period will help us uncover questions about the volatility during turbulent times as well as normal time. With its crucial role in asset pricing, portfolio allocation, and risk management, volatility forecasting has therefore attracted a large amount of attention
 
## Reasons Why We Will Achieve the Goal
On the one hand, the structure of financial markets is complex, highly nonlinear and has a low signal-to-noise ratio, which makes it nearly impossible to predict short-term asset returns (see, e.g., Gu, Kelly, and Xiu, 2020; Chen, Pelger, and Zhu, 2019). On the other hand, various stylized facts (e.g., the slow decay of autocorrelation in absolute returns), implies that volatility is to a large extent predictable. With its crucial role in asset pricing, portfolio allocation, and risk management, volatility forecasting has therefore attracted a large amount of attention.

Why Machine Learning
- Traditional models, often relying on linear regression, break down when the explanatory variables are strongly correlated, exhibit low signal-to-noise ratio, or if the underlying structure is highly nonlinear. ML can deal with highly nonlinear structured data that often appear in financial markets.
- It can extract valuable information from a large amount of data by increasing feature space; linear regression models often fail to do so. 
- It is significantly resistant to a substantial amount of noise added to the original data set to obfuscate the signal, in contrast to the linear regression.


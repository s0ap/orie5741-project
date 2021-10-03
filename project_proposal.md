
# Project Proposal

## What is our aim?
Financial markets have very complex structures that are highly nonlinear with a low signal-to-noise ratio. This makes it really difficult to predict short-term asset returns. But then different factors like slow decay of autocorrelation in absolute returns tend to suggest that volatility is to a large extent predictable. The aim of this project is to predict both daily and weekly realized volatility so that we do not miss out on any important event by averaging out over a larger time frame. Computation of time series of realised variance will be done at weekly as well as daily level so as to catch any signals which might get missed during the computation of daily realised variance. We plan to analyse out of sample performance for Machine Learning base volatility forecasting using regularization, tree-based algorithms and neural networks and compare this performace with the traditional Heterogenous Auto-Regressive models to show how the new approaches improve the accuracy of forecasting volatility. We will try to extract additional information about future volatility using these models and additional volatility predictors. Further, we will investigate structure of Machine Learning methods to analyse the interaction between covariates. We can compute variable importance using accumulated local effect plots and finally check how ML techniques respond to pure noise variables. 

## Why is this important?
 We believe that covering the crisis period will help us uncover questions about the volatility during turbulent times as well as normal time. With its crucial role in asset pricing, portfolio allocation, and risk management, volatility forecasting has therefore attracted a large amount of attention. Especially during the recent times when volatility products created a havoc in the stock market in March 2020, it makes sense to forecast the volatitlity so that we are able to pick up signals in future and be able to avoid such a havoc.

## What data are we using?
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
 
## Why Machine Learning is a good option?
Conventional linear regression models fail to predict accurately when the input variables are strongly correlated or have a low signal-to-noise ratio, or the underlying structure is highly nonlinear. Machine Learning can deal with highly nonlinear structured data that often appear in volatility in financial markets. They can also extract valuable information from a large amount of data by looking at a broad feature space; linear regression models often fail to do so. Additionally, they are significantly resistant to a substantial amount of noise added to distort the original dataset, in contrast to the linear regression. So, we believe Machine Learning models would give some meaningful insights on volatility predictions.



<h1><center>Machine Learning Engineer Nanodegree Capstone Project</center></h1>

<h2><center>Predicting Stock Prices with LSTM</center></h2>

<h4><center>Tarek A. Atwan</center></h4><h4><center>August 2021</center></h4>

---

# 1. Definition

## Project Overview

​	During the COVID-19 pandemic period in 2020, there were a lot of interesting and unexpected behaviors in the stock market that have extended into 2021. The pandemic impact was more like an accelerators, propelling some companies forward at record speed while others were collapsed at plummeted as if they were hit by a tornado[^1]

​	The pandemic also shifted the consumer behavior forcing them to adapt at an accelerated speed, thus impacting many firms who were not ready to embrace such a dramatic and quick change. This drift have benefits several market sectors at the expense of others. Examples include the reliance on online shopping (e-commerce) for almost anything and everything, subscribing to video streaming and gaming services for entertainment, and phenomenon of accepting the idea that people can work remotely at the comfort of their home.

​	During the pandemic, there was another interesting phenomneon that made predicting stock market even less stable and more volatile. This was headlined in many news outlets describing the mass interest from the general public to jump into the stock market for day trading[^2]. Many of those investors were not your typical day trader or investor, they do not apply statistics analysis, or focus on fundamental analysis, nor are they interested in technical analysis or technical indicators. They were pretty much riding a wave based on gut instinct, speculations, hype, and other factors.

​	As the impact of COVID-19 on the stock market hit hard in 2020, it's repel effect still plays into 2021. In this paper, the goal is to investigate the potential of using machine learning from past data to predict future stock prices. More specifically, the intersect is to examine Long-Short Term Memory (LSTM) neural network on time series stock data to see if these proven algorithms and approaches are still valid for making predictions.

​	The paper will investigate the use of classical time series analysis techniques on hand picked stocks (top and worst performers of 2020). These classical techniques include Monte Carlo simulation[^3], Autoregressive Integrated Moving Average (ARIMA)[^4], and Vector Autoregressive (VAR)[^5]. These will help build an intuition on these statistical approaches and act as benchmark to the more complex deep learning techniques using LSTM[^6].

​	We will obtain the stock data using a AlphaVantage service to pull historical stock data. In particular, we will use a Python wrapper SDK that leverages the AlphaVantage API to make our calls to extract data for each of the selected stocks. Throughout the analysis, we will be using the adjusted closing price. AlphaVantage also allows to pull additional data such a list of Technical Indicators, Fundamental data, and Sector data. During the process, we will be comparing univariate time series techniques and multivariate time series techniques and combine additional features (signals) to test our models. The first half to he journey will focus on building a benchmark with classical time series techniques before diving and exploring LSTM models and their robustness to pick up signals from the noise. 

## Problem Statement 

The paper’s goal is to investigate the potential of predicting stock prices using historical data. Historical data in this context includes the COVID-19 2020 period which was an anomaly in itself. We explored two approaches: Historical from 2010-2021 and from 2019-2021 to see how the models behave. We hold out data from 2021 to see if the model can learn from past data to predict prices in 2021 post the COVID-19 peak impact period. 

Our base or benchmark models will include statistical models such as ARIMA, VAR, and Monte Carlo simulation. Input data will include Adjusted Closing price, RSI (Relative Strength Index), and in the case of LSTM we will feed multiple stocks that seemed to be moving together to predict one stock of interest to determine if they are good predictors. 

## Metrics

Since we predicting continue values this problem is a regression problem. We will use regression related metrics to measure and evaluate the performance of our models. 

* **Root Mean Square Error** 

$$
\Large \text{RMSE} = \sqrt{\frac{1}{n}\sum\limits_{i=1}^{n}(Y_i - \hat{Y}_i)^2}
$$

Where

$n$ = number of data points

$Y_i$ = observed values

$\hat{Y}_i$ = predicted values 

* **Mean Absolute Percentage Error**

$$
\Large \text{MAPE} = \frac{1}{n}\sum\limits_{t=1}^{n}| \frac{A_t-E_t}{A_t} |
$$

where

$n$ = number of times the summation iteration happens

$A_t$ =  observed value

$F_t$ = predicted value

* **$R^2$​ (R Squared)**

$$
\Large R^2 = 1 - \frac{RSS}{TSS}
$$

where

$RSS$ = sum of squared residuals 

$TSS$ = total sum of squares 

---

# 2. Analysis 

## Data Exploration








[^1]: Bradley, C., The impact of COVID-19 on capital markets, one year in, McKinsey & Company, https://www.mckinsey.com/business-functions/strategy-and-corporate-finance/our-insights/the-impact-of-covid-19-on-capital-markets-one-year-in
[^2]: Nova A., Many are chasing the stock market by day trading in the pandemic. It could end badly, CNBC, https://www.cnbc.com/2020/09/21/many-people-turn-to-day-trading-in-pandemic-few-will-be-a-winners.html
[^3]: Monte Carlo method, Wikipedia, https://en.wikipedia.org/wiki/Monte_Carlo_method
[^4]: Autoregressive integrated moving average, Wikipedia, https://en.wikipedia.org/wiki/Autoregressive_integrated_moving_average
[^5]: Vector autoregressive, Wikepdia, https://en.wikipedia.org/wiki/Vector_autoregression
[^6]: Long short-term memory, Wikipedia, https://en.wikipedia.org/wiki/Long_short-term_memory


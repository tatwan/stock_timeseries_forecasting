# Stock Market Prediction Proposal	

## Introduction

There has been a lot of interest in trading lately, triggered by COVID and lockdown amongst other reasons. Many analysts and traders that I talk with feel that the market now is even more unpredictable since many of the new traders do not follow the normal routine used by professionals e.g. researching financial statements, technical analysis ..etc. and are driven by either passion, gut feeling, or sometimes following the crowd as in the example of Game Stop.

## Time Series Forecasting and Machine Learning

I would like to explore and take this opportunity to dive into this deeper and determine how predictable is the market. I would like to use Time Series Forecasting and Analysis techniques like ARIMA for example, and compare it with Machine Learning and Deep Learning techniques and compare the results. 

Ideally I would like to train on past data and see how the algorithm performs (pre-COVID). Then apply it to recent data (COVID and post) and see if that the model learns applies.

## Complexity

I know that Stock market prediction is not an easy task and is an advanced topic of research. But I am hoping this attempt would be a baseline or foundation for further investigation and fine tuning. 

## Evaluation Metrics

Ideally, I will train on time slices like 2016-2019 (maybe extend to 2020), then attempt to forecast into 2020 or 2021(testing). The metrics that I will use for evaluation will be:

* Root Mean Square Error (RMSE)
* R Squared
* and Mean Absolute Percentage Error (MAPE)
* Forecast Skill (SS)

## Process

For stock market prediction/forecasting I will use:

* Hand-picked portfolio of top performing stocks (those that really took off during COVID and Post)
* S&P 500 

## Model Deployment

I will deploy the selected model using Streamlit so users can interact and pick a stock and then have the model create a forecast. 


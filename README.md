# Prophet-Challenge
Module 8 Challenge - Time Series Prediction with Prophet

## Introduction
This challenge is an introduction to the fascinating world of making predictions with data.  We are armed with the time series financial and user data for `Mercardo Libre`, the most popular e-commerce site in Latin America.  First, We will analyze the analyze the data for unusual and seasonal patterns.  We will then try to find any relationship between the search traffic and stock price patterns.  Finally, we will use a modeling tool, `Prophet`, to create a time series model that analyzes and forecasts patterns in the hourly search traffic data.

## Data Sources
1. [Google hourly search trends of `Mercardo Libre` from June 1, 2016 to September 8, 2020 in csv format](https://static.bc-edx.com/ai/ail-v-1-0/m8/lms/datasets/google_hourly_search_trends.csv)

2. [Hourly `Mercardo Libre` stock close price data from January 2, 2015 to July 31, 2020 in csv format](https://static.bc-edx.com/ai/ail-v-1-0/m8/lms/datasets/mercado_stock_price.csv)

## Components
1. Find unusual patterns in hourly Google search traffic.
2. Mine the search traffic data for seasonality.
3. Relate the search traffic to stock price patterns.
4. Create a time series model with Prophet.

## Summary of Findings
1. Google search traffic increased by 8.55% in May 2020 over the monthly median search traffic.  MercadoLibre released its quarterly financial results in May 2020.

<img src="images/Figure 1 - May 2020 Unusual Pattern.png" alt="Unusual Pattern" width="800"/>
<br><br><br>

2. Three trends are identified from the Google search traffic.
<br>
2.1 Daily search traffic increases from morning to night. It peaks at mid-night, and bottoms around 8 AM daily.

<img src="images/Figure 2 - Daily Search Pattern.png" alt="Daily Search Pattern" width="400"/>
<br><br>

2.2 Weekly search traffic is the highest from Monday to Thursday, peaking on Tuesday. It drops off quickly from Friday to Sunday.

<img src="images/Figure 3 - Weekly Search Pattern.png" alt="Weekly Search Pattern" width="400"/>
<br><br>

2.3 Annual search traffic is the highest in the first 3 months and December. Otherwise, the 22nd week and the 33rd week appear to have seasonal peaks.

<img src="images/Figure 4 - Yearly Search Pattern.png" alt="Yearly Search Pattern" width="400"/>
<br><br><br>


3. Search traffic and stock price relations
<br>
3.1 Both the stock close price and Google search trends indicate an abnormal shock pattern before March 2020, which is consistent with the narrative. The initial shock started late Feb 2020 is likely in anticipation of a global lockdown to deal with COVID-19. When WHO declared COVID-19 a Pandemic on March 11, 2020, the uncertainly was over. New customers and revenue for Mercado Libre increased over the next few months. The recovery of its stock close price appears to lag behind that of its Google search trends by approximately one month.

<img src="images/Figure 5 - Search vs Stock First Half 2020.png" alt="First Half 2020" width="600"/>
<br><br>

3.2 According to the correlation table below, there is a very weak negative correlation between the lagged search traffic and the stock volatility. There is practically no correlation between the lagged search traffic and the hourly stock return.

<img src="images/Figure 6 - Search vs Stock Correlation.png" alt="Search vs Stock Correlation" width="600"/>
<br><br><br>

4. Prophet predictions
<br>
4.1 According to the Prophet model, the near-term forecast for the Google search trends of Mercado Libre is going to decrease starting on 9/9/2020. It is likely to bottom out in about 40 days, followed by a gradual increase in the next 40 days.

<img src="images/Figure 7 - Search Forecast.png" alt="Search Forecast" width="800"/>
<br><br>

4.2 The following patterns are identified from the time series components of the model
<br>
4.2.1 The daily component plot indicates the greatest popularity is before and after mid-night.
<br>
4.2.2 The weekly component plot shows Tuesday has the most search traffic of a week.
<br>
4.2.3 According to the yearly component plot, the middle of October has the lowest search traffic in a calendar year.

<img src="images/Figure 8 - Forecast Components.png" alt="Forecast Components" width="800"/>
<br><br><br>


![Logo](https://www.crmsoftwareblog.com/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/sales-forecast-webinar-image-1-625x417.jpeg.webp)

# Retail Giant Sales Forecasting

This project uses different techniques to forecast the sales of an online supergiant store.

File  | Description
------------- | -------------
sales_forecast.ipynb  | Python code file for data preparation and forecasting
Global+Superstore+Data.csv  | The dataset for the project



## Business Problem

Global Mart is an online supergiant store that has worldwide operations. This store takes orders and delivers across the globe and deals with all the major product categories — consumer, corporate and home office.

 

As a sales manager for this store, you have to forecast the sales of the products for the next 6 months, so that you have a proper estimate and can plan your inventory and business processes accordingly.
## Data Preparation

The store dataset has the following 5 attributes and their data description is as given below:

Attributes  | Description
------------- | -------------
Order-Date  | The date on which the order was placed
Segment  | The segment to which the product belongs
Market  | The market to which the customer belongs
Sales	| Total sales value of the transaction
Profit	| Profit made on the transaction


The store caters to 7 different geographical market segments and 3 major customer segments, i.e. consumer, corporate and home as can be seen in the table below.

Market  | Segment
------------- | -------------
Africa	| Consumer
APAC (Asia Pacific)	| Corporate
Canada|	Home Office
EMEA(Middle East)	|    
EU (European Union)	 |
LATAM (Latin America) |	 
US (United States)	|  

Based on these, there are 21 unique "Market-Segments" for which the sales forecasts can be made. That is the dataset needs to be prepared such that you get the Order-Date, Sales, and Profit for the 21 market segments.

Now, due to certain unpredictable circumstances in the market, as a company, you are prioritizing only the best and most consistent market segment in terms of profitability. You want to see which market segment is the most consistently profitable. And then, you want to forecast the sales for that most consistently profitable market segment only. This way you know that the market region your company is investing in will be beneficial for the company as the forecasts will be reliable. As of now, you do not want to focus on other market segments that might have not been very consistent and profitable to your company.

 

So, not all of these 21 market segments are important from the store’s point of view. You need to find out the most consistently profitable market segment from the above and forecast the sales and demand for that single market segment only and not for all.

 

Now the question is how do you find the most profitable market segment from the 21 market segments?
## How to find the most profitable market segment?

By now, it’s clear that you only need to work on one market segment which is the most consistently profitable. To find the most consistently profitable market segment you will be using a measure called "Coefficient of Variation (CoV)". The coefficient of variation or CoV is nothing but the ratio of the standard deviation to the mean for the data that it is being calculated for.

 

But why consider the coefficient of variation here and not the standard deviation for measuring how much variation is present in the data for each of the 21 market segments? and how will the coefficient of variation lead you to the most profitable market segment for which eventually you will want to forecast the sales?

 

The coefficient of variation is a ratio of the standard deviation to the mean. Once you have prepared the data such that you have the Order-Date, Sales, and Profit against each of the 21 market segments, and not in the manner as it was in the initial dataset, you can check the standard deviation and the mean calculated on profit for all the 21 market segments and compare. You will find that these values vary a lot and hence it is meaningless to compare the 21 market segment's profits based on the standard deviation and their mean.
## Forecasting Modeling

* After splitting the data into test-train, I have decomposed the data series to understand it better. 

* Performed SARIMA, Holt-Winters’ exponential smoothing - Additive, Holt-Winters’ exponential smoothing - Multiplicative methods on the data.
## Tech Stack

**Programming Language:** Python 

**Libraries:** numpy, pandas, statsmodels, sklearn, matplotlib

**Models:** Holt-Winters’ exponential smoothing - Additive, Holt-Winters’ exponential smoothing - Multiplicative, SARIMA model

## Results

* Holt-Winters' Exponential Smoothing Technique - Additive:
![additive](https://github.com/manasiChoughule/Time-Series-Sales-Forecast/assets/25337745/7cf78a14-4a5a-4953-b7bf-c807c61d0d05)

* Holt-Winters' Exponential Smoothing Technique - Multiplicative:
![multiplitive](https://github.com/manasiChoughule/Time-Series-Sales-Forecast/assets/25337745/24ec8516-b37b-4e97-8fc4-d69d4f574c68)

* Seasonal auto regressive integrated moving average (SARIMA)
![sarima](https://github.com/manasiChoughule/Time-Series-Sales-Forecast/assets/25337745/62b3233f-bc1f-42a2-acb2-af5380e5d915)



METHOD  | RMSE  | MAPE
------------- | ------------- | -------------
Holt Winters' additive method	  | 10624.26	| 13.02
Holt Winters' multiplicative method  | 10931.27	| 17.17
Seasonal autoregressive integrated moving average (SARIMA)  | 8715.57	| 10.45

## Conclusion 

Among all the methods done above, we can conclude that the forecast done using the SARIMA method is able to predict the sales closer to the actual values




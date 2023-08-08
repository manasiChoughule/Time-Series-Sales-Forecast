# Retail Giant Sales Forecasting

![Retail Giant Sales Forecasting](https://www.crmsoftwareblog.com/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/sales-forecast-webinar-image-1-625x417.jpeg.webp)

## Table of Contents

- [Introduction](#introduction)
- [Business Problem](#business-problem)
- [Data Preparation](#data-preparation)
- [Identifying the Most Profitable Market Segment](#identifying-the-most-profitable-market-segment)
- [Forecasting Models](#forecasting-models)
- [Tech Stack](#tech-stack)
- [Results](#results)
- [Conclusion](#conclusion)

## Introduction

Welcome to the Retail Giant Sales Forecasting project repository. This project focuses on predicting the sales of an online supergiant store using advanced techniques. By forecasting sales accurately, the store can streamline inventory management, optimize business processes, and make informed strategic decisions.

## Business Problem

As the sales manager of Global Mart, an international online store, the challenge is to forecast product sales for the next 6 months. Accurate sales predictions are crucial for effective inventory management and business planning. The key objective is to identify the most consistently profitable market segment and forecast sales exclusively for that segment.

## Data Preparation

The dataset encompasses essential attributes including Order Date, Segment, Market, Sales, and Profit. The store operates across 7 geographical market segments and caters to 3 major customer segments. The primary task is to transform the data, obtaining Order Date, Sales, and Profit details for the 21 unique "Market-Segments".

## Identifying the Most Profitable Market Segment

To determine the most consistently profitable market segment, we leverage the "Coefficient of Variation (CoV)" – the ratio of standard deviation to the mean. Calculating the CoV for each market segment allows us to pinpoint the segment exhibiting the most reliable and profitable performance. Concentrating on this segment for forecasting guarantees dependable results.

## Forecasting Models

The project harnesses cutting-edge forecasting techniques to predict sales:

- **SARIMA (Seasonal AutoRegressive Integrated Moving Average)**: SARIMA captures intricate seasonality and trends in the sales data.
- **Holt-Winters' Exponential Smoothing - Additive**: This method incorporates seasonality, trend, and level components with additive adjustments.
- **Holt-Winters' Exponential Smoothing - Multiplicative**: Similar to additive, this method employs multiplicative adjustments for more complex patterns.

## Tech Stack

**Programming Language:** Python

**Libraries:** numpy, pandas, statsmodels, sklearn, matplotlib

**Models:** Holt-Winters’ Additive and Multiplicative, SARIMA

## Results

The forecasting methods were evaluated based on two metrics: Root Mean Squared Error (RMSE) and Mean Absolute Percentage Error (MAPE). The results are as follows:

| Method                                            | RMSE     | MAPE  |
|---------------------------------------------------|----------|-------|
| Holt Winters' Additive Method                     | 10624.26 | 13.02 |
| Holt Winters' Multiplicative Method               | 10931.27 | 17.17 |
| Seasonal AutoRegressive Integrated Moving Average | 8715.57  | 10.45 |

### Holt Winters' Additive Method
![additive](https://github.com/manasiChoughule/Time-Series-Sales-Forecast/assets/25337745/7cf78a14-4a5a-4953-b7bf-c807c61d0d05)

### Holt Winters' Multiplicative Method
![multiplitive](https://github.com/manasiChoughule/Time-Series-Sales-Forecast/assets/25337745/24ec8516-b37b-4e97-8fc4-d69d4f574c68)

### Seasonal AutoRegressive Integrated Moving Average
![sarima](https://github.com/manasiChoughule/Time-Series-Sales-Forecast/assets/25337745/62b3233f-bc1f-42a2-acb2-af5380e5d915)


## Conclusion

After meticulous analysis, the **Seasonal AutoRegressive Integrated Moving Average (SARIMA)** method demonstrated the closest prediction to actual sales values. We recommend this method for forecasting sales in the consistently profitable market segment. This empowers Global Mart to make informed decisions, enhance operational efficiency, and drive sustainable growth.

For comprehensive code implementation and analysis, explore the Jupyter notebook `sales_forecast.ipynb`. Access the complete dataset through `Global+Superstore+Data.csv`.

For inquiries and collaborations, reach out to us at [mchoughule96@gmail.com](mailto:mchoughule96@gmail.com).

# Review of kaggle time series competition

Inspired by [Learnings from Kaggle’s Forecasting Competitions](https://arxiv.org/pdf/2009.07701.pdf) 
by Casper Solheim Bojer & Jens Peder Meldgaard in 2020, I surveyed the top 3 solutions in the past kaggle time series
competitions since 2014 to 2022.


<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [List of competitions](#list-of-competitions)
- [Top 3 most voted EDAs](#top-3-most-voted-edas)
  - [1. Walmart Recruiting - Store Sales Forecasting](#1-walmart-recruiting---store-sales-forecasting)
  - [2. Walmart Recruiting II: Sales in Stormy Weather](#2-walmart-recruiting-ii-sales-in-stormy-weather)
  - [3. Rossmann Store Sales](#3-rossmann-store-sales)
  - [4. Web Traffic Time Series Forecasting](#4-web-traffic-time-series-forecasting)
  - [5. Corporación Favorita Grocery Sales Forecasting](#5-corporaci%C3%B3n-favorita-grocery-sales-forecasting)
  - [6. Recruit Restaurant Visitor Forecasting](#6-recruit-restaurant-visitor-forecasting)
  - [7. Google Brain - Ventilator Pressure Prediction](#7-google-brain---ventilator-pressure-prediction)
  - [8. LANL Earthquake Prediction](#8-lanl-earthquake-prediction)
  - [9. Two Sigma: Using News to Predict Stock Movements](#9-two-sigma-using-news-to-predict-stock-movements)
  - [10. ASHRAE - Great Energy Predictor III](#10-ashrae---great-energy-predictor-iii)
  - [11. University of Liverpool - Ion Switching](#11-university-of-liverpool---ion-switching)
  - [12. M5 Forecasting - Accuracy](#12-m5-forecasting---accuracy)
  - [13. Jane Street Market Prediction](#13-jane-street-market-prediction)
  - [14. Acea Smart Water Analytics](#14-acea-smart-water-analytics)
  - [15. Google Brain - Ventilator Pressure Prediction](#15-google-brain---ventilator-pressure-prediction)
  - [16. Optiver Realized Volatility Prediction](#16-optiver-realized-volatility-prediction)
  - [17. G-Research Crypto Forecasting](#17-g-research-crypto-forecasting)
  - [18. Ubiquant Market Prediction](#18-ubiquant-market-prediction)
- [Top 3 solutions](#top-3-solutions)
  - [1. Walmart Recruiting - Store Sales Forecasting](#1-walmart-recruiting---store-sales-forecasting-1)
  - [2. Walmart Recruiting II: Sales in Stormy Weather](#2-walmart-recruiting-ii-sales-in-stormy-weather-1)
  - [3. Rossmann Store Sales](#3-rossmann-store-sales-1)
  - [4. Web Traffic Time Series Forecasting](#4-web-traffic-time-series-forecasting-1)
  - [5. Corporación Favorita Grocery Sales Forecasting](#5-corporaci%C3%B3n-favorita-grocery-sales-forecasting-1)
  - [6. Recruit Restaurant Visitor Forecasting](#6-recruit-restaurant-visitor-forecasting-1)
  - [7. Google Analytics Customer Revenue Prediction](#7-google-analytics-customer-revenue-prediction)
  - [8. LANL Earthquake Prediction](#8-lanl-earthquake-prediction-1)
  - [9. Two Sigma: Using News to Predict Stock Movements](#9-two-sigma-using-news-to-predict-stock-movements-1)
  - [10. ASHRAE - Great Energy Predictor III](#10-ashrae---great-energy-predictor-iii-1)
  - [11. University of Liverpool - Ion Switching](#11-university-of-liverpool---ion-switching-1)
  - [12. M5 Forecasting - Accuracy](#12-m5-forecasting---accuracy-1)
  - [13. Jane Street Market Prediction](#13-jane-street-market-prediction-1)
  - [14. Acea Smart Water Analytics](#14-acea-smart-water-analytics-1)
  - [15. Google Brain - Ventilator Pressure Prediction](#15-google-brain---ventilator-pressure-prediction-1)
  - [16. Optiver Realized Volatility Prediction](#16-optiver-realized-volatility-prediction-1)
  - [17. G-Research Crypto Forecasting](#17-g-research-crypto-forecasting-1)
  - [18. Ubiquant Market Prediction](#18-ubiquant-market-prediction-1)
- [Analysis](#analysis)
  - [Popularity trend of methods used by top 3 rankers](#popularity-trend-of-methods-used-by-top-3-rankers)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## List of competitions

| #   | Year      | Title                                                                                                                | Data size     |
|-----|-----------|----------------------------------------------------------------------------------------------------------------------|---------------|
| 1   | 2014      | [Walmart Recruiting - Store Sales Forecasting](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)  | 3.22MB        |
| 2   | 2015      | [Walmart Recruiting II: Sales in Stormy Weather](https://www.kaggle.com/c/walmart-recruiting-sales-in-stormy-weather) | 9MB           |
| 3   | 2015      | [Rossmann Store Sales](https://www.kaggle.com/c/rossmann-store-sales)                                                | 39.85MB       |
| 4   | 2017      | [Web Traffic Time Series Forecasting](https://www.kaggle.com/c/web-traffic-time-series-forecasting/overview)         | 611.85MB      |
| 5   | 2018      | [Corporación Favorita Grocery Sales Forecasting](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/overview) | 479.88MB      |
| 6   | 2018      | [Recruit Restaurant Visitor Forecasting](https://www.kaggle.com/c/recruit-restaurant-visitor-forecasting/overview)   | 27.3MB        |
| 7   | 2018      | [Google Analytics Customer Revenue Prediction](https://www.kaggle.com/c/ga-customer-revenue-prediction/overview)     | 35.9GB        |
| 8   | 2019      | [LANL Earthquake Prediction](https://www.kaggle.com/c/LANL-Earthquake-Prediction/overview)                           | 10.42GB       |
| 9   | 2019      | [Two Sigma: Using News to Predict Stock Movements](https://www.kaggle.com/c/two-sigma-financial-news/overview)       | Not available |
| 10  | 2019      | [ASHRAE - Great Energy Predictor III](https://www.kaggle.com/c/ashrae-energy-prediction/overview)                    | 2.61GB        |
| 11  | 2020      | [University of Liverpool - Ion Switching](https://www.kaggle.com/c/liverpool-ion-switching/overview)                 | 146.08MB      |
| 12  | 2020      | [M5 Forecasting - Accuracy](https://www.kaggle.com/c/m5-forecasting-accuracy/overview)                               | 450.47MB      |
| 13  | 2020-2021 | [Jane Street Market Prediction](https://www.kaggle.com/c/jane-street-market-prediction/overview)                     | Not available |
| 14  | 2020-2021 | [Acea Smart Water Analytics](https://www.kaggle.com/c/acea-water-prediction/overview)                                | 3.45MB        |
| 15  | 2021      | [Google Brain - Ventilator Pressure Prediction](https://www.kaggle.com/c/ventilator-pressure-prediction/overview)    | 698.79MB      |
| 16  | 2022      | [Optiver Realized Volatility Prediction](https://www.kaggle.com/c/optiver-realized-volatility-prediction/overview) | 2.73GB        |
| 17  | 2022      | [G-Research Crypto Forecasting](https://www.kaggle.com/c/g-research-crypto-forecasting)                              | 3.12GB        |
| 18  | 2022      | [Ubiquant Market Prediction](https://www.kaggle.com/c/ubiquant-market-prediction)                                    | 18.55GB       |

## Top 3 most voted EDAs
To learn the characteristic of data given in each competition, EDA is one of the best way.   
So top 3 most voted EDAs are listed.


### 1. Walmart Recruiting - Store Sales Forecasting
1. []()
2. []()
3. []()

### 2. Walmart Recruiting II: Sales in Stormy Weather
1. []()
2. []()
3. []()

### 3. Rossmann Store Sales
1. []()
2. []()
3. []()

### 4. Web Traffic Time Series Forecasting
1. []()
2. []()
3. []()

### 5. Corporación Favorita Grocery Sales Forecasting
1. []()
2. []()
3. []()

### 6. Recruit Restaurant Visitor Forecasting
1. []()
2. []()
3. []()

### 7. Google Brain - Ventilator Pressure Prediction
1. [Ventilator Pressure Prediction: EDA, FE and models](https://www.kaggle.com/artgor/ventilator-pressure-prediction-eda-fe-and-models)
2. [🔥EDA +FE+TabNet 🧠🧠[Weights and Biases]](https://www.kaggle.com/usharengaraju/eda-fe-tabnet-weights-and-biases)
3. [Ventilator Pressure: EDA and simple submission](https://www.kaggle.com/carlmcbrideellis/ventilator-pressure-eda-and-simple-submission)

### 8. LANL Earthquake Prediction
1. []()
2. []()
3. []()

### 9. Two Sigma: Using News to Predict Stock Movements
1. []()
2. []()
3. []()

### 10. ASHRAE - Great Energy Predictor III
1. []()
2. []()
3. []()

### 11. University of Liverpool - Ion Switching
1. []()
2. []()
3. []()

### 12. M5 Forecasting - Accuracy
1. []()
2. []()
3. []()

### 13. Jane Street Market Prediction
1. []()
2. []()
3. []()

### 14. Acea Smart Water Analytics
1. []()
2. []()
3. []()

### 15. Google Brain - Ventilator Pressure Prediction
1. []()
2. []()
3. []()

### 16. Optiver Realized Volatility Prediction
1. [https://www.kaggle.com/chumajin/optiver-realized-eda-for-starter-english-version](https://www.kaggle.com/chumajin/optiver-realized-eda-for-starter-english-version)
2. [Optiver Realized Volatility Prediction - EDA](https://www.kaggle.com/gunesevitan/optiver-realized-volatility-prediction-eda)
3. [Optiver; EDA XGBoost starter(日本語,Japanese)](https://www.kaggle.com/matsuosan/optiver-eda-xgboost-starter-japanese)

### 17. G-Research Crypto Forecasting
1. [📊 G-Research Plots + EDA 📊](https://www.kaggle.com/odins0n/g-research-plots-eda)
2. [To The Moon 🚀 [G-Research Crypto Forecasting EDA]](https://www.kaggle.com/iamleonie/to-the-moon-g-research-crypto-forecasting-eda)
3. [📈📊[G-crypto] Interactive Dashboard + Indicators](https://www.kaggle.com/toomuchsauce/g-crypto-interactive-dashboard-indicators)

### 18. Ubiquant Market Prediction
1. [EDA- target analysis](https://www.kaggle.com/lucamassaron/eda-target-analysis)
2. [Ubiquant EDA and Baseline](https://www.kaggle.com/ilialar/ubiquant-eda-and-baseline)
3. [🔥The most advanced analytics🔥](https://www.kaggle.com/kartushovdanil/the-most-advanced-analytics)


## Top 3 solutions

### 1. Walmart Recruiting - Store Sales Forecasting

| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code        | Discussion |
|-----|---------|------------------------|-------------------|-------------|------------------|---------------------|----------|---------------------|-----------------------|--------------------|
| 1   |         |                        |                   |             |                  |                     |          |                     |  https://github.com/davidthaler/Walmart_competition_code | https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/discussion/8125#44434   |
| 2   |         |                        |                   |             |                  |                     |          |                     |                       | https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/discussion/8023#43811   |
| 3   |         |                        |                   |             |                  |                     |          |                     | https://ideone.com/pUw773 | https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/discussion/8023#43821   |

### 2. Walmart Recruiting II: Sales in Stormy Weather

| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |


### 3. Rossmann Store Sales
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |


### 4. Web Traffic Time Series Forecasting
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |


### 5. Corporación Favorita Grocery Sales Forecasting
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |


### 6. Recruit Restaurant Visitor Forecasting
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |


### 7. Google Analytics Customer Revenue Prediction
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |


### 8. LANL Earthquake Prediction
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |


### 9. Two Sigma: Using News to Predict Stock Movements
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |


### 10. ASHRAE - Great Energy Predictor III
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |


### 11. University of Liverpool - Ion Switching
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |


### 12. M5 Forecasting - Accuracy
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction      | speed up   | libraries and tools    | Code    | Discussion                                                                                                    |
|-----|---------|------------------------|-------------------|-------------|--------------------|-------------------------------|------------|------------------------|---------|---------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   |             |                    |                               |            |                        |         | [1st place solution](https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/163684#913208)                                                                                                          |
| 2   |         |                        |                   |             |                    |                               |            |                        |         | [2nd place solution](https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/164599#917890)                                                                                                          |
| 3   |         |                        |                   |             |                    |                               |            |                        |         | [3rd place solution - NN approach](https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/164374#916793) |

### 13. Jane Street Market Prediction
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                   | Discussion                    |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|------------------------|-------------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 2   |         |                        |                   |             |                     |                          |          |                     |                        |                               |
| 3   |         |                        |                   |             |                     |                          |          |                     |                        |                               |

### 14. Acea Smart Water Analytics
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                 | Discussion               |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|----------------------|--------------------------|
| 1   |         |                        |                   |             |                     |                          |          |                     | []()                 |  []()                    |
| 2   |         |                        |                   |             |                     |                          |          |                     | []()                 |  []()                    |
| 3   |         |                        |                   |             |                     |                          |          |                     | []()                 |  []()                    |

### 15. Google Brain - Ventilator Pressure Prediction
| Pos | methods | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                | Discussion |
|-----|---------|------------------------|-------------------|-------------|---------------------|--------------------------|----------|---------------------|---------------------|-----|
| 1   |         |                        |                   |             |                     |                          |          |                     | [[#1 Solution] LSTM CNN transformer (1 fold)](https://www.kaggle.com/shujun717/1-solution-lstm-cnn-transformer-1-fold) | [Winner's Writeup!](https://www.kaggle.com/c/ventilator-pressure-prediction/discussion/285256#1570087)|
| 2   |         |                        |                   |             |                     |                          |          |                     | []()                | [#2 Solution: The inverse of a PID controller](https://www.kaggle.com/c/ventilator-pressure-prediction/discussion/285283#1570285)|
| 3   |         |                        |                   |             |                     |                          |          |                     | []()                | [[3rd Place] Single model scored 0.0975 w/o PID controller](https://www.kaggle.com/c/ventilator-pressure-prediction/discussion/285330#1570563)|


### 16. Optiver Realized Volatility Prediction
| Pos | methods             | Ensemble method        | data split method | pre-process | feature engineering | dimensionality reduction | speed up | libraries and tools | Code                                                                                                       | Discussion |
|-----|------------------------------|------------------------|-------------------|-------------|------------------|---------------------|----------|---------------------|------------------------------------------------------------------------------------------------------------|--------------------|
| 1   | LightGBM<br/>MLP<br/>CNN     | equally weighd average | GroupKFold        |minmax_scale | Nearest-Neighbor | t-SNE               | joblib   |                     | [1st place (public 2nd place) solution](https://www.kaggle.com/nyanpn/1st-place-public-2nd-place-solution) |                    |
| 3   | LightGBM<br/>MLP<br/> TabNet |  equally weighd average |                   |minmax_scale<br/>QuantileTransformer |KMeans            |                     | joblib     |                     | [Third Place Solution](https://www.kaggle.com/eduardopeynetti/third-place-solution)                                           |                    |


### 17. G-Research Crypto Forecasting
Ongoing

### 18. Ubiquant Market Prediction
Ongoing

## Analysis


### Popularity trend of methods used by top 3 rankers

- Table

| Method   | 2014 | 2015 | 2016 | 2017 | 2018 | 2019 | 2020 | 2021 | 2022 |
|----------|------|------|------|------|------|------|------|------|------|
| NN       | TD   |      |      |      |      |      |      |      |      |
| LightGBM | TD   |      |      |      |      |      |      |      |      |
|          |      |      |      |      |      |      |      |      |      |


- Chart








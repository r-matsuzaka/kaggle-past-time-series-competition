# Review of kaggle time series competition

Inspired by [Learnings from Kaggle’s Forecasting Competitions](https://arxiv.org/pdf/2009.07701.pdf) 
by Casper Solheim Bojer & Jens Peder Meldgaard in 2020, I surveyed the top 3 solutions in the past kaggle time series
competitions since 2014 to 2024.

If you find new time series competitions, please tell me by issues.

## ❤️ Support This Project
If you find this project helpful, please consider supporting it with a small donation!

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://www.buymeacoffee.com/matsuzakaryo)
[![GitHub Sponsor](https://img.shields.io/badge/GitHub%20Sponsors-EA4AAA?style=for-the-badge&logo=github-sponsors&logoColor=white)](https://github.com/sponsors/r-matsuzaka)
[![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/ryom939384)


<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [List of competitions](#list-of-competitions)
- [Top 3 most voted EDAs](#top-3-most-voted-edas)
  - [1. Walmart Recruiting - Store Sales Forecasting](#1-walmart-recruiting---store-sales-forecasting)
  - [2. Walmart Recruiting II: Sales in Stormy Weather](#2-walmart-recruiting-ii-sales-in-stormy-weather)
  - [3. Rossmann Store Sales](#3-rossmann-store-sales)
  - [4. Predicting Red Hat Business Value](#4-predicting-red-hat-business-value)
  - [5. Web Traffic Time Series Forecasting](#5-web-traffic-time-series-forecasting)
  - [6. TalkingData AdTracking Fraud Detection Challenge](#6-talkingdata-adtracking-fraud-detection-challenge)
  - [7. Corporación Favorita Grocery Sales Forecasting](#7-corporaci%C3%B3n-favorita-grocery-sales-forecasting)
  - [8. Recruit Restaurant Visitor Forecasting](#8-recruit-restaurant-visitor-forecasting)
  - [9. Google Analytics Customer Revenue Prediction](#9-google-analytics-customer-revenue-prediction)
  - [10. LANL Earthquake Prediction](#10-lanl-earthquake-prediction)
  - [11. Two Sigma: Using News to Predict Stock Movements](#11-two-sigma-using-news-to-predict-stock-movements)
  - [12. ASHRAE - Great Energy Predictor III](#12-ashrae---great-energy-predictor-iii)
  - [13. University of Liverpool - Ion Switching](#13-university-of-liverpool---ion-switching)
  - [14. M5 Forecasting - Accuracy](#14-m5-forecasting---accuracy)
  - [15. Jane Street Market Prediction](#15-jane-street-market-prediction)
  - [16. Acea Smart Water Analytics](#16-acea-smart-water-analytics)
  - [17. Google Brain - Ventilator Pressure Prediction](#17-google-brain---ventilator-pressure-prediction)
  - [18. Optiver Realized Volatility Prediction](#18-optiver-realized-volatility-prediction)
  - [19. G-Research Crypto Forecasting](#19-g-research-crypto-forecasting)
  - [20. Ubiquant Market Prediction](#20-ubiquant-market-prediction)
  - [21. American Express - Default Prediction](#21-american-express---default-prediction)
  - [22. GoDaddy - Microbusiness Density Forecasting](#22-godaddy---microbusiness-density-forecasting)
- [Top 3 solutions](#top-3-solutions)
  - [1. Walmart Recruiting - Store Sales Forecasting](#1-walmart-recruiting---store-sales-forecasting-1)
  - [2. Walmart Recruiting II: Sales in Stormy Weather](#2-walmart-recruiting-ii-sales-in-stormy-weather-1)
  - [3. Rossmann Store Sales](#3-rossmann-store-sales-1)
  - [4. Predicting Red Hat Business Value](#4-predicting-red-hat-business-value-1)
  - [5. Web Traffic Time Series Forecasting](#5-web-traffic-time-series-forecasting-1)
  - [6. TalkingData AdTracking Fraud Detection Challenge](#6-talkingdata-adtracking-fraud-detection-challenge-1)
  - [7. Corporación Favorita Grocery Sales Forecasting](#7-corporaci%C3%B3n-favorita-grocery-sales-forecasting-1)
  - [8. Recruit Restaurant Visitor Forecasting](#8-recruit-restaurant-visitor-forecasting-1)
  - [9. Google Analytics Customer Revenue Prediction](#9-google-analytics-customer-revenue-prediction-1)
  - [10. LANL Earthquake Prediction](#10-lanl-earthquake-prediction-1)
  - [11. Two Sigma: Using News to Predict Stock Movements](#11-two-sigma-using-news-to-predict-stock-movements-1)
  - [12. ASHRAE - Great Energy Predictor III](#12-ashrae---great-energy-predictor-iii-1)
  - [13. University of Liverpool - Ion Switching](#13-university-of-liverpool---ion-switching-1)
  - [14. M5 Forecasting - Accuracy](#14-m5-forecasting---accuracy-1)
  - [15. Jane Street Market Prediction](#15-jane-street-market-prediction-1)
  - [16. Acea Smart Water Analytics](#16-acea-smart-water-analytics-1)
  - [17. Google Brain - Ventilator Pressure Prediction](#17-google-brain---ventilator-pressure-prediction-1)
  - [18. Optiver Realized Volatility Prediction](#18-optiver-realized-volatility-prediction-1)
  - [19. G-Research Crypto Forecasting](#19-g-research-crypto-forecasting-1)
  - [20. Ubiquant Market Prediction](#20-ubiquant-market-prediction-1)
  - [21. American Express - Default Prediction](#21-american-express---default-prediction-1)
  - [22. GoDaddy - Microbusiness Density Forecasting](#22-godaddy---microbusiness-density-forecasting-1)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## List of competitions

| #   | Year      | Title                                                                                                                    | Data size |
|-----|-----------|--------------------------------------------------------------------------------------------------------------------------|---------|
| 1   | 2014      | [Walmart Recruiting - Store Sales Forecasting](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)      | 3.22MB  |
| 2   | 2015      | [Walmart Recruiting II: Sales in Stormy Weather](https://www.kaggle.com/c/walmart-recruiting-sales-in-stormy-weather)    | 9MB     |
| 3   | 2015      | [Rossmann Store Sales](https://www.kaggle.com/c/rossmann-store-sales)                                                    | 39.85MB |
| 4   | 2016      | [Predicting Red Hat Business Value](https://www.kaggle.com/competitions/predicting-red-hat-business-value/overview)      | 26.74MB |
| 5   | 2017      | [Web Traffic Time Series Forecasting](https://www.kaggle.com/c/web-traffic-time-series-forecasting/overview)             | 611.85MB |
| 6   | 2018      | [TalkingData AdTracking Fraud Detection Challenge](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/data) | 11.27GB |
| 7   | 2018      | [Corporación Favorita Grocery Sales Forecasting](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/overview)   | 479.88MB |
| 8   | 2018      | [Recruit Restaurant Visitor Forecasting](https://www.kaggle.com/c/recruit-restaurant-visitor-forecasting/overview)       | 27.3MB  |
| 9   | 2018      | [Google Analytics Customer Revenue Prediction](https://www.kaggle.com/c/ga-customer-revenue-prediction/overview)         | 35.9GB  |
| 10  | 2019      | [LANL Earthquake Prediction](https://www.kaggle.com/c/LANL-Earthquake-Prediction/overview)                               | 10.42GB |
| 11  | 2019      | [Two Sigma: Using News to Predict Stock Movements](https://www.kaggle.com/c/two-sigma-financial-news/overview)           | Not available |
| 12  | 2019      | [ASHRAE - Great Energy Predictor III](https://www.kaggle.com/c/ashrae-energy-prediction/overview)                        | 2.61GB  |
| 13  | 2020      | [University of Liverpool - Ion Switching](https://www.kaggle.com/c/liverpool-ion-switching/overview)                     | 146.08MB |
| 14  | 2020      | [M5 Forecasting - Accuracy](https://www.kaggle.com/c/m5-forecasting-accuracy/overview)                                   | 450.47MB |
| 15  | 2020-2021 | [Jane Street Market Prediction](https://www.kaggle.com/c/jane-street-market-prediction/overview)                         | Not available |
| 16  | 2020-2021 | [Acea Smart Water Analytics](https://www.kaggle.com/c/acea-water-prediction/overview)                                    | 3.45MB  |
| 17  | 2021      | [Google Brain - Ventilator Pressure Prediction](https://www.kaggle.com/c/ventilator-pressure-prediction/overview)        | 698.79MB |
| 18  | 2022      | [Optiver Realized Volatility Prediction](https://www.kaggle.com/c/optiver-realized-volatility-prediction/overview)       | 2.73GB  |
| 19  | 2022      | [G-Research Crypto Forecasting](https://www.kaggle.com/c/g-research-crypto-forecasting)                                  | 3.12GB  |
| 20  | 2022      | [Ubiquant Market Prediction](https://www.kaggle.com/c/ubiquant-market-prediction)                                        | 18.55GB |
| 21  | 2022      | [American Express - Default Prediction](https://www.kaggle.com/competitions/amex-default-prediction)                     | 50.31 GB |
| 22  | 2022-2023 | [GoDaddy - Microbusiness Density Forecasting](https://www.kaggle.com/competitions/godaddy-microbusiness-density-forecasting) |  10.93 MB |


## Top 3 most voted EDAs
To learn the characteristic of data given in each competition, EDA is one of the best way.   
So top 3 most voted EDAs are listed.


### 1. [Walmart Recruiting - Store Sales Forecasting](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [EDA and Store Sales Predictions using XGB](https://www.kaggle.com/yasirhussain1987/eda-and-store-sales-predictions-using-xgb)
2. [Walmart prediction - (1) EDA with time and space](https://www.kaggle.com/yepp2411/walmart-prediction-1-eda-with-time-and-space)
3. [Wallmart Sales - EDA - feat eng [Future Update]](https://www.kaggle.com/maxdiazbattan/wallmart-sales-eda-feat-eng-future-update)

### 2. [Walmart Recruiting II: Sales in Stormy Weather](https://www.kaggle.com/c/walmart-recruiting-sales-in-stormy-weather)
[> Go to the top](#Review-of-kaggle-time-series-competition)

NA

### 3. [Rossmann Store Sales](https://www.kaggle.com/c/rossmann-store-sales)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Time Series Analysis and Forecasts with Prophet](https://www.kaggle.com/elenapetrova/time-series-analysis-and-forecasts-with-prophet)
2. [EDA and forecasting with RFRegressor_FINAL_UPDATED](https://www.kaggle.com/stefanozakher94/eda-and-forecasting-with-rfregressor-final-updated)
3. [How Does New Competition Affect Sales?](https://www.kaggle.com/ggep22/how-does-new-competition-affect-sales)

### 4. [Predicting Red Hat Business Value](https://www.kaggle.com/competitions/predicting-red-hat-business-value)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Time Travel (EDA)](https://www.kaggle.com/code/anokas/time-travel-eda)
2. [Redhat EDA](https://www.kaggle.com/code/apapiu/redhat-eda)
3. [RedHat Hack in plain English (EDA)](https://www.kaggle.com/code/dmi3kno/redhat-hack-in-plain-english-eda)

### 5. [Web Traffic Time Series Forecasting](https://www.kaggle.com/c/web-traffic-time-series-forecasting/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Wiki Traffic Forecast Exploration - WTF EDA](https://www.kaggle.com/headsortails/wiki-traffic-forecast-exploration-wtf-eda)
2. [Web Traffic Time Series Forecasting (EDA)](https://www.kaggle.com/bodamanojkumar/web-traffic-time-series-forecasting-eda)
3. [Wikipedia Web traffic EDA](https://www.kaggle.com/mtao94/wikipedia-web-traffic-eda)

### 6. [TalkingData AdTracking Fraud Detection Challenge](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/data)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [TalkingData EDA plus time patterns](https://www.kaggle.com/yuliagm/talkingdata-eda-plus-time-patterns)
2. [TalkingData EDA and Class Imbalance](https://www.kaggle.com/kailex/talkingdata-eda-and-class-imbalance)
3. [TalkingData: EDA to Model Evaluation | LB: 0.9683](https://www.kaggle.com/pranav84/talkingdata-eda-to-model-evaluation-lb-0-9683)

### 7. [Corporación Favorita Grocery Sales Forecasting](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Shopping for Insights - Favorita EDA](https://www.kaggle.com/headsortails/shopping-for-insights-favorita-eda)
2. [Memory optimization and EDA on entire dataset](https://www.kaggle.com/jagangupta/memory-optimization-and-eda-on-entire-dataset)
3. [Grocery EDA Dirty XGBoost, Arima,ETS,Prophet](https://www.kaggle.com/ambarish/grocery-eda-dirty-xgboost-arima-ets-prophet)

### 8. [Recruit Restaurant Visitor Forecasting](https://www.kaggle.com/c/recruit-restaurant-visitor-forecasting/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Be my guest - Recruit Restaurant EDA](https://www.kaggle.com/headsortails/be-my-guest-recruit-restaurant-eda)
2. [Exhaustive Weather EDA/File Overview](https://www.kaggle.com/huntermcgushion/exhaustive-weather-eda-file-overview)
3. [Recruit Restaurant EDA](https://www.kaggle.com/fabiendaniel/recruit-restaurant-eda)

### 9. [Google Analytics Customer Revenue Prediction](https://www.kaggle.com/c/ga-customer-revenue-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [R EDA for GStore + GLM + KERAS + XGB](https://www.kaggle.com/kailex/r-eda-for-gstore-glm-keras-xgb)
2. [Google Analytics EDA + LightGBM + Screenshots](https://www.kaggle.com/erikbruin/google-analytics-eda-lightgbm-screenshots)
3. [A Very Extensive GStore Exploratory Analysis](https://www.kaggle.com/captcalculator/a-very-extensive-gstore-exploratory-analysis)


### 10. [LANL Earthquake Prediction](https://www.kaggle.com/c/LANL-Earthquake-Prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Earthquakes FE. More features and samples](https://www.kaggle.com/artgor/earthquakes-fe-more-features-and-samples)
2. [LANL Earthquake EDA and Prediction](https://www.kaggle.com/gpreda/lanl-earthquake-eda-and-prediction)
3. [Masters Final Project: EDA](https://www.kaggle.com/vettejeep/masters-final-project-eda)

### 11. [Two Sigma: Using News to Predict Stock Movements](https://www.kaggle.com/c/two-sigma-financial-news/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [EDA, feature engineering and everything](https://www.kaggle.com/artgor/eda-feature-engineering-and-everything)
2. [👨‍🔬 Bird Eye 👀 view of Two Sigma + NN Approach](https://www.kaggle.com/ashishpatel26/bird-eye-view-of-two-sigma-nn-approach)
3. [Simple EDA - Two Sigma](https://www.kaggle.com/pestipeti/simple-eda-two-sigma)

### 12. [ASHRAE - Great Energy Predictor III](https://www.kaggle.com/c/ashrae-energy-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [🔌⚡ASHRAE -Start Here: A GENTLE Introduction](https://www.kaggle.com/caesarlupum/ashrae-start-here-a-gentle-introduction)
2. [EDA for ASHRAE](https://www.kaggle.com/nroman/eda-for-ashrae)
3. [A deep dive EDA into ALL variables](https://www.kaggle.com/jaseziv83/a-deep-dive-eda-into-all-variables)

### 13. [University of Liverpool - Ion Switching](https://www.kaggle.com/c/liverpool-ion-switching/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Ion Switching Competition : Signal EDA 🧪](https://www.kaggle.com/tarunpaparaju/ion-switching-competition-signal-eda)
2. [EDA - Ion Switching](https://www.kaggle.com/pestipeti/eda-ion-switching)
3. [Simple EDA-Model](https://www.kaggle.com/siavrez/simple-eda-model)

### 14. [M5 Forecasting - Accuracy](https://www.kaggle.com/c/m5-forecasting-accuracy/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Back to (predict) the future - Interactive M5 EDA](https://www.kaggle.com/headsortails/back-to-predict-the-future-interactive-m5-eda)
2. [M5 Competition : EDA + Models 📈](https://www.kaggle.com/tarunpaparaju/m5-competition-eda-models)
3. [Time Series Forecasting-EDA, FE & Modelling📈](https://www.kaggle.com/anshuls235/time-series-forecasting-eda-fe-modelling)

### 15. [Jane Street Market Prediction](https://www.kaggle.com/c/jane-street-market-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Jane Street: EDA of day 0 and feature importance](https://www.kaggle.com/carlmcbrideellis/jane-street-eda-of-day-0-and-feature-importance)
2. [Jane_street_Extensive_EDA & PCA starter 📊⚡](https://www.kaggle.com/muhammadmelsherbini/jane-street-extensive-eda-pca-starter)
3. [EDA / A Quant's Prespective](https://www.kaggle.com/hamzashabbirbhatti/eda-a-quant-s-prespective)

### 16. [Acea Smart Water Analytics](https://www.kaggle.com/c/acea-water-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Acea Smart Water: Full EDA & Prediction](https://www.kaggle.com/maksymshkliarevskyi/acea-smart-water-full-eda-prediction)
2. [EDA: Quenching the Thirst for Insights](https://www.kaggle.com/iamleonie/eda-quenching-the-thirst-for-insights)
3. [Quick EDA | Reporting & Data Understanding](https://www.kaggle.com/ekrembayar/quick-eda-reporting-data-understanding)

### 17. [Google Brain - Ventilator Pressure Prediction](https://www.kaggle.com/c/ventilator-pressure-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Ventilator Pressure Prediction: EDA, FE and models](https://www.kaggle.com/artgor/ventilator-pressure-prediction-eda-fe-and-models)
2. [🔥EDA +FE+TabNet 🧠🧠[Weights and Biases]](https://www.kaggle.com/usharengaraju/eda-fe-tabnet-weights-and-biases)
3. [Ventilator Pressure: EDA and simple submission](https://www.kaggle.com/carlmcbrideellis/ventilator-pressure-eda-and-simple-submission)

### 18. [Optiver Realized Volatility Prediction](https://www.kaggle.com/c/optiver-realized-volatility-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [Optiver Realized: EDA for starter(English version)](https://www.kaggle.com/chumajin/optiver-realized-eda-for-starter-english-version)
2. [Optiver Realized Volatility Prediction - EDA](https://www.kaggle.com/gunesevitan/optiver-realized-volatility-prediction-eda)
3. [Optiver; EDA XGBoost starter(日本語,Japanese)](https://www.kaggle.com/matsuosan/optiver-eda-xgboost-starter-japanese)

### 19. [G-Research Crypto Forecasting](https://www.kaggle.com/c/g-research-crypto-forecasting)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [📊 G-Research Plots + EDA 📊](https://www.kaggle.com/odins0n/g-research-plots-eda)
2. [To The Moon 🚀 [G-Research Crypto Forecasting EDA]](https://www.kaggle.com/iamleonie/to-the-moon-g-research-crypto-forecasting-eda)
3. [📈📊[G-crypto] Interactive Dashboard + Indicators](https://www.kaggle.com/toomuchsauce/g-crypto-interactive-dashboard-indicators)

### 20. [Ubiquant Market Prediction](https://www.kaggle.com/c/ubiquant-market-prediction)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [EDA- target analysis](https://www.kaggle.com/lucamassaron/eda-target-analysis)
2. [Ubiquant EDA and Baseline](https://www.kaggle.com/ilialar/ubiquant-eda-and-baseline)
3. [🔥The most advanced analytics🔥](https://www.kaggle.com/kartushovdanil/the-most-advanced-analytics)

### 21. [American Express - Default Prediction](https://www.kaggle.com/c/ubiquant-market-prediction)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [AMEX EDA which makes sense ⭐️⭐️⭐️⭐️⭐️](https://www.kaggle.com/code/ambrosm/amex-eda-which-makes-sense)
2. [AMEX Default Prediction EDA & LGBM Baseline](https://www.kaggle.com/code/kellibelcher/amex-default-prediction-eda-lgbm-baseline)
3. [American Express EDA](https://www.kaggle.com/code/datark1/american-express-eda)

### 22. [GoDaddy - Microbusiness Density Forecasting](https://www.kaggle.com/competitions/godaddy-microbusiness-density-forecasting)
[> Go to the top](#Review-of-kaggle-time-series-competition)

1. [TBD]()
2. [TBD]()
3. [TBD]()


## Top 3 solutions

### 1. [Walmart Recruiting - Store Sales Forecasting](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods | FE | Ensemble | Split | Code | Discussion |
|-----|---------|-----|----------|------|------|------------|
| 1   | Time Series Models:<br>• STLF/ETS<br>• STLF/ARIMA<br>• Seasonal ARIMA<br>• Fourier ARIMA | • SVD preprocessing<br>• Time series decomposition<br>• Correlation-based NN pooling<br>• Holiday period adjustment | Average of 6 time series models:<br>• 3 simple models<br>• 3 advanced models | Department-wise pooling across stores | [💻](https://github.com/davidthaler/Walmart_competition_code) | [🔊](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/discussion/8125#) |
| 2 | Statistical Methods:<br>• ARIMA with STL decomposition<br>• ETS with STL decomposition<br>• Naive method with STL decomposition<br>• UCM<br><br>Machine Learning Methods:<br>• Random Forest<br>• Linear Regression<br>• K Nearest Regression<br>• Principal Component Regression | • Used week of the year (1-52)<br>• Filled missing values with 0<br>• Different holiday weighting for<br>stores with high growth rate vs.<br>stores without high growth | Weighted average<br>and trimmed<br>mean of 6<br>methods* | Individual models<br>for each store-<br>department<br>combination<br>(~3600 total) | [💻](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting/discussion/8095) | [🔊](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/discussion/8023#43811) |
| 3 | Simple year-over-year approach (no statistical or ML models):<br>• Prior year sales as base predictor<br>• Holiday week alignment<br>• Weighted average of prior weeks<br>• Store & department trend factors<br>• Manual trend coefficients | • Calendar date matching between years<br>• Special handling for moving holidays<br>• Store-specific trend factors<br>• Department-specific trend factors<br>• Minimal "warm day" adjustment | None - single<br>model with<br>minor adjustments | Individual<br>predictions<br>for each store-<br>department<br>combination | [💻](https://ideone.com/pUw773) | [🔊](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/discussion/8023#43821) |

### 2. [Walmart Recruiting II: Sales in Stormy Weather](https://www.kaggle.com/c/walmart-recruiting-sales-in-stormy-weather)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods | FE | Ensemble | Split | Code | Discussion |
|-----|---------|-----|----------|------|------|------------|
| 1   | PPR (Projection Pursuit Regression) for curve fitting + Lasso regression with vowpal wabbit | • Weekday, weekend flags, holiday flags<br>• Item/store numbers<br>• Date features (year, month, day)<br>• Black Friday period flags<br>• Weather features (precipitation>0.2, temperature departure>8 or <-8)<br>• Moving average<br>• Handling of consecutive zeros<br>• Feature interactions (AB, AC, BM, CM, BK, CK) | Single model | • Excluded item/stores with all zeros<br>• Excluded data from 2013-12-25<br>• Excluded data where moving average was zero<br>• Excluded dates with too many consecutive zeros on both sides | [💻](https://github.com/threecourse/kaggle-walmart-recruiting-sales-in-stormy-weather) | [🔊](https://www.kaggle.com/c/walmart-recruiting-sales-in-stormy-weather/discussion/14452#80451) |
| 2   | - | - | - | - | NA | NA |
| 3   | - | - | - | - | NA | NA |                                                                                                              |


### 3. [Rossmann Store Sales](https://www.kaggle.com/c/rossmann-store-sales)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|---------------------------|----------------------------------------|------------------------|-------------------|------|---------------------------------------------------------------------------------------------------------------|
| 1   |                           |                                        |                        |                   | NA   | [🔊](https://www.kaggle.com/c/rossmann-store-sales/discussion/17896#101318) |
| 2   |                           |                                        |                        |                   | NA   | NA                                                                                                            |
| 3   |                           |                                        |                        |                   | [💻](https://www.kaggle.com/c/rossmann-store-sales/discussion/17974#101792) | [🔊](https://github.com/entron/entity-embedding-rossmann)                              |


### 4. [Predicting Red Hat Business Value](https://www.kaggle.com/competitions/predicting-red-hat-business-value)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods | FE | Ensemble | Split | Code | Discussion |
|-----|---------|-----|----------|------|------|------------|
| 1   | Two-level approach:<br>• 1st level: XGBoost classifier on aggregated data<br>• 2nd level: XGBoost with leakage exploitation | • TF-IDF features for categorical variables<br>• Group level aggregations<br>• Group_1 ID value<br>• Number of activities/people in group<br>• Min/max dates<br>• First/last activity in timeline | Average of:<br>• Best LB model<br>• Best CV model | • Removed group_1=17304 (30% of train data)<br>• Used Distinct operator for group_1's with 3000+ rows<br>• 5-fold unstratified CV based on people file | NA | [🔊](https://www.kaggle.com/competitions/predicting-red-hat-business-value/discussion/23786) |
| 2   | Mixture of three models:<br>• Logistic regression<br>• kNN<br>• XGBoost (based on public scripts)<br>+ Probabilistic interpolation model for groups | • Histogram-based features (fuzzy binary encoding)<br>• Date-based probabilistic interpolation<br>• Leaderboard feedback | Weighted average:<br>• 0.4 (linear model)<br>• 0.25 (kNN)<br>• 0.25 (public script)<br>• 0.1 (0.5 constant) | NA | NA | [🔊](https://www.kaggle.com/competitions/predicting-red-hat-business-value/discussion/23824) |
| 3   | XGBoost + extensive group_1 and date trick exploitation | • Modified leave-one-out encoding for char_10<br>• Group_1 as continuous feature<br>• Time-based confidence levels for leak exploitation<br>• Group-person level leak simulation for training data | Post-processing:<br>• 90% weight to most extreme prediction within a group<br>• 10% weight to raw prediction<br>• Rule-based overrides for ML shortcomings | NA | NA | [🔊](https://www.kaggle.com/competitions/predicting-red-hat-business-value/discussion/23803) |

### 5. [Web Traffic Time Series Forecasting](https://www.kaggle.com/c/web-traffic-time-series-forecasting/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|---------------------------|----------------------------------------|------------------------|-------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 1   |                           |                                        |                        |                   | [💻](https://github.com/Arturus/kaggle-web-traffic)          | [🔊](https://www.kaggle.com/c/web-traffic-time-series-forecasting/discussion/43795#245823)                              |
| 2   |                           |                                        |                        |                   | [💻](https://github.com/jfpuget/Kaggle/tree/master/WebTrafficPrediction) | [🔊](https://www.kaggle.com/c/web-traffic-time-series-forecasting/discussion/39395)                                     |
| 3   |                           |                                        |                        |                   | [💻](https://gist.github.com/thousandvoices/7d01f366a388516359915a4b090e29d4) | [🔊](https://www.kaggle.com/c/web-traffic-time-series-forecasting/discussion/39367#223730) |


### 6. [TalkingData AdTracking Fraud Detection Challenge](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/data)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|---------------------------|----------------------------------------|------------------------|-------------------|------|--------------------------------------------------------------------------------------------------------------------------------------|
| 1   |                           |                                        |                        |                   | NA   | [🔊](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/discussion/56475#326680)                        |
| 2   |                           |                                        |                        |                   | NA   | [🔊](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/discussion/56328#325630)             |
| 3   |                           |                                        |                        |                   | NA   | [🔊](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/discussion/56262) |

### 7. [Corporación Favorita Grocery Sales Forecasting](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|---------------------------|----------------------------------------|------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| 1   |                           |                                        |                        |                   | [💻](https://www.kaggle.com/shixw125/1st-place-lgb-model-public-0-506-private-0-511) <br/> <br/> [💻](https://www.kaggle.com/shixw125/1st-place-nn-model-public-0-507-private-0-513) | [🔊](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/discussion/47582#269355)          |
| 2   |                           |                                        |                        |                   | NA                                                                                                                                                                                                                                                                              | [🔊](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/discussion/47568#269198) |
| 3   |                           |                                        |                        |                   | NA                                                                                                                                                                                                                                                                              | [🔊](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/discussion/47560#269132) |


### 8. [Recruit Restaurant Visitor Forecasting](https://www.kaggle.com/c/recruit-restaurant-visitor-forecasting/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|---------------------------|----------------------------------------|----------------------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| 1   | LightGBM                  |                                        | -                                            | -                                         | [💻](https://www.kaggle.com/pureheart/1st-place-lgb-model-public-0-470-private-0-502) <br/> <br/> [💻](https://www.kaggle.com/plantsgo/solution-public-0-471-private-0-505/script) | NA                                        |
| 2   | -                         |                                        | -                                            | -                                         | NA                                                                                                                                                                                                                                                                  | NA                                        |
| 3   | -                         |                                        | -                                            | -                                         | NA                                                                                                                                                                                                                                                                  | NA                                        |


### 9. [Google Analytics Customer Revenue Prediction](https://www.kaggle.com/c/ga-customer-revenue-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|---------------------------|----------------------------------------|----------------------------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 1   |                           |                                        |                                              |                                           | [💻](https://www.kaggle.com/kostoglot/winning-solution?scriptVersionId=10911396#L144) | [🔊](https://www.kaggle.com/c/ga-customer-revenue-prediction/discussion/82614#482360) |
| 2   |                           |                                        |                                              |                                           | NA                                                                                                  | [🔊](https://www.kaggle.com/c/imaterialist-challenge-fashion-2018/discussion/57934)     |
| 3   | -                         |                                        | -                                            | -                                         | NA                                                                                                  | NA                                                                                                                          |


### 10. [LANL Earthquake Prediction](https://www.kaggle.com/c/LANL-Earthquake-Prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|---------------------------|----------------------------------------|------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| 1   |                           |                                        |                        |                   | [💻](https://www.kaggle.com/ilu000/1-private-lb-kernel-lanl-lgbm) <br/> <br/> [💻](https://www.kaggle.com/dkaraflos/1-geomean-nn-and-6featlgbm-2-259-private-lb/notebook) | [🔊](https://www.kaggle.com/c/LANL-Earthquake-Prediction/discussion/94390#542982) |
| 2   |                           |                                        |                        |                   | NA                                                                                                                                                                                                                                                | [🔊](https://www.kaggle.com/c/LANL-Earthquake-Prediction/discussion/94369#542827) |
| 3   |                           |                                        |                        |                   | NA                                                                                                                                                                                                                                                | [🔊](https://www.kaggle.com/c/LANL-Earthquake-Prediction/discussion/94459#543607)     |


### 11. [Two Sigma: Using News to Predict Stock Movements](https://www.kaggle.com/c/two-sigma-financial-news/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

NA

### 12. [ASHRAE - Great Energy Predictor III](https://www.kaggle.com/c/ashrae-energy-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp;                                                                              | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|--------------------------------------------------------------------------------------------------------|----------------------------------------|------------------------|-------------------|------|--------------------------------------------------------------------------------------------------------------------|
| 1   | CatBoost<br/> <br/>LightGBM<br/> <br/>MLP                                                              |                                        |                        |                   | NA   | [🔊](https://www.kaggle.com/c/ashrae-energy-prediction/discussion/124709#711401) |
| 2   | XGBoost<br/> <br/>LightGBM<br/> <br/>Catboost<br/> <br/>Feed-forward Neural Network |                                        |                        |                   | NA   | [🔊](https://www.kaggle.com/c/ashrae-energy-prediction/discussion/123481#704834)                   |
| 3   | CNN<br/> <br/>LightGBM<br/> <br/>Catboost                                                                                                 |                                        |                        |                   | NA   | [🔊](https://www.kaggle.com/c/ashrae-energy-prediction/discussion/124984#713104)                 |


### 13. [University of Liverpool - Ion Switching](https://www.kaggle.com/c/liverpool-ion-switching/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|---------------------------|----------------------------------------|------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   |                           |                                        |                        |                   | NA                                                                                                                  | [🔊](https://www.kaggle.com/c/liverpool-ion-switching/discussion/153940#862403)                                                                                                                          |
| 2   |                           |                                        |                        |                   | [💻](https://www.kaggle.com/stdereka/2nd-place-solution-preprocessing-tricks) | [🔊](https://www.kaggle.com/c/liverpool-ion-switching/discussion/153991#862688) <br/> <br/>[🔊](https://www.kaggle.com/c/liverpool-ion-switching/discussion/155919#872833) |
| 3   |                           |                                        |                        |                   | NA                                                                                                                  | [🔊](https://www.kaggle.com/c/indoor-location-navigation/discussion/240161#1313777) <br/> <br/>[🔊](https://www.kaggle.com/c/liverpool-ion-switching/discussion/153734#861458)       |


### 14. [M5 Forecasting - Accuracy](https://www.kaggle.com/c/m5-forecasting-accuracy/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp;| FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|--------------------------|----------------------------------------|------------------------|-------------------|------|---------------------------------------------------------------------------------------------------------------|
| 1   | LightGBM                 |                                        |                        |                   | NA   | [💻](https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/163684#913208)               |
| 2   | LightGBM                 |                                        |                        |                   | NA   | [💻](https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/164599#917890)               |
| 3   | DeepAR                   |                                        |                        |                   | NA   | [💻](https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/164374#916793) |

### 15. [Jane Street Market Prediction](https://www.kaggle.com/c/jane-street-market-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|---------------------------|----------------------------------------|----------------------------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| 1   | XGBoost<br/> <br/>NN      |                                        |                                              |                   | [💻](https://www.kaggle.com/vikazrajpurohit/jane-street-1st-on-leaderboard-notebook) | NA                                                                                   |
| 3   | 49 layers MLPs            | No                                     | 15 ensembles of NN                           |                   | NA                                                                                                                         | [🔊](https://www.kaggle.com/c/jane-street-market-prediction/discussion/224713#1232146) |

NA for Pos #2

### 16. [Acea Smart Water Analytics](https://www.kaggle.com/c/acea-water-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

NA

### 17. [Google Brain - Ventilator Pressure Prediction](https://www.kaggle.com/c/ventilator-pressure-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp;     | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|-------------------------------|----------------------------------------|------------------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | LSTM<br/> <br/>Transformer    |                                        | single architecture                            | KFold              | [💻](https://www.kaggle.com/shujun717/1-solution-lstm-cnn-transformer-1-fold) | [🔊](https://www.kaggle.com/c/ventilator-pressure-prediction/discussion/285256#1570087)                                              |
| 2   | Stacked LSTM                  |                                        | ensembled by 7 models                          | KFold              | NA                                                                                                                     | [🔊](https://www.kaggle.com/c/ventilator-pressure-prediction/discussion/285283#1570285)                   |
| 3   | Conv1d<br/> <br/>Stacked LSTM |                                        | random seed average                            | Stratified K-Folds | NA                                                                                                                     | [🔊](https://www.kaggle.com/c/ventilator-pressure-prediction/discussion/285330#1570563) |


### 18. [Optiver Realized Volatility Prediction](https://www.kaggle.com/c/optiver-realized-volatility-prediction/overview)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp;               | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                 | Discussion                                                                                           |
|-----|-----------------------------------------|----------------------------------------|----------------------------------|------------------|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 1   | LightGBM<br/> <br/>MLP<br/> <br/>CNN    |                                        | equally weighd average           | GroupKFold       | [💻](https://www.kaggle.com/nyanpn/1st-place-public-2nd-place-solution) | [🔊](https://www.kaggle.com/c/optiver-realized-volatility-prediction/discussion/274970#1526710) |
| 3   | LightGBM<br/> <br/>MLP<br/> <br/>TabNet |                                        | equally weighd average           | KFold            | [💻](https://www.kaggle.com/eduardopeynetti/third-place-solution)                        | [🔊](https://www.kaggle.com/c/optiver-realized-volatility-prediction/discussion/278588#1545008)                     |

NA for Pos #2

### 19. [G-Research Crypto Forecasting](https://www.kaggle.com/c/g-research-crypto-forecasting)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                                                                       | Discussion                                                                                |
|-----|---------------------------|----------------------------------------|----------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 1   | -                         | -                                      | -                                            | -                                         | NA                                                                                                                                         | NA                                                                                        |
| 2   | LightGBM                  |                                        | Single model                                 |                                           | NA                                                                                                                                         | [🔊](https://www.kaggle.com/competitions/g-research-crypto-forecasting/discussion/323098) |
| 3   | LightGBM                  |                                        | Single model                                 |                                           | [💻](https://www.kaggle.com/code/sugghi/training-3rd-place-solution) [💻](https://www.kaggle.com/code/sugghi/inference-3rd-place-solution) | [🔊](https://www.kaggle.com/competitions/g-research-crypto-forecasting/discussion/323703) |

### 20. [Ubiquant Market Prediction](https://www.kaggle.com/c/ubiquant-market-prediction)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;     | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;                         | Code | Discussion                                                                             |
|-----|---------------------------|----------------------------------------|--------------------------------------------------|-------------------------------------------------------------------|------|----------------------------------------------------------------------------------------|
| 1   | LightGBM<br/> <br/>TABNET |                                        | Average of (LGBM x 5 Folds) + (TABNET x 5 Folds) | PurgedGroupTimeSeries<br/> <br/>TimeSerieseSplit <br/> <br/>KFold | NA   | [🔊](https://www.kaggle.com/competitions/ubiquant-market-prediction/discussion/338220) |
| 2   | LightGBM                  |                                        | -                                                | Purged K-FOLD cross validation with embargo                       | NA   | [🔊](https://www.kaggle.com/competitions/ubiquant-market-prediction/discussion/338615) |
| 3   | 6 layers transformer      |                                        | 5 seeds ensemble                                 | -                                                                 | NA   | [🔊](https://www.kaggle.com/competitions/ubiquant-market-prediction/discussion/338561)   |

### 21. [American Express - Default Prediction](https://www.kaggle.com/competitions/amex-default-prediction)
[> Go to the top](#Review-of-kaggle-time-series-competition)

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code                                                                                   | Discussion                                                                          |
|-----|---------------------------|----------------------------------------|----------------------------------------------|-------------------------------------------|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| 1   | LightGBM<br/> <br/>GRU    |                                        | Ensembled by 4 models                        |                                           | [💻](https://github.com/jxzly/Kaggle-American-Express-Default-Prediction-1st-solution) | [🔊](https://www.kaggle.com/competitions/amex-default-prediction/discussion/348111) |
| 2   | LGB/XGB/CTB<br/> <br/>NN  |                                        |                                              |                                           | NA                                                                                     | [🔊](https://www.kaggle.com/competitions/amex-default-prediction/discussion/347637) |
| 3   | LGB/CTB                   |                                        | Ensembled by 3 models                        |                                           | NA                                                                                     | [🔊](https://www.kaggle.com/competitions/amex-default-prediction/discussion/349741)                                                                                |

### 22. [GoDaddy - Microbusiness Density Forecasting](https://www.kaggle.com/competitions/godaddy-microbusiness-density-forecasting)
[> Go to the top](#Review-of-kaggle-time-series-competition)

Ongoing

| Pos | Methods&emsp;&emsp;&emsp; | FE&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Ensemble&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Split&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; | Code | Discussion |
|-----|---------------------------|----------------------------------------|----------------------------------------------|-------------------------------------------|------|------------|
| 1   | Linear regression         |                                        |                                              |                                           | [💻](https://www.kaggle.com/code/kaggleqrdl/first-place-code)| [🔊](https://www.kaggle.com/competitions/godaddy-microbusiness-density-forecasting/discussion/395131)|
| 2   |                           |                                        |                                              |                                           |      |            |
| 3   |                           |                                        |                                              |                                           |      |            |

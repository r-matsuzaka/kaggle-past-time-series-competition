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
  - [5. TalkingData AdTracking Fraud Detection Challenge](#5-talkingdata-adtracking-fraud-detection-challenge)
  - [6. Corporación Favorita Grocery Sales Forecasting](#6-corporaci%C3%B3n-favorita-grocery-sales-forecasting)
  - [7. Recruit Restaurant Visitor Forecasting](#7-recruit-restaurant-visitor-forecasting)
  - [8. Google Analytics Customer Revenue Prediction](#8-google-analytics-customer-revenue-prediction)
  - [9. LANL Earthquake Prediction](#9-lanl-earthquake-prediction)
  - [10. Two Sigma: Using News to Predict Stock Movements](#10-two-sigma-using-news-to-predict-stock-movements)
  - [11. ASHRAE - Great Energy Predictor III](#11-ashrae---great-energy-predictor-iii)
  - [12. University of Liverpool - Ion Switching](#12-university-of-liverpool---ion-switching)
  - [13. M5 Forecasting - Accuracy](#13-m5-forecasting---accuracy)
  - [14. Jane Street Market Prediction](#14-jane-street-market-prediction)
  - [15. Acea Smart Water Analytics](#15-acea-smart-water-analytics)
  - [16. Google Brain - Ventilator Pressure Prediction](#16-google-brain---ventilator-pressure-prediction)
  - [17. Optiver Realized Volatility Prediction](#17-optiver-realized-volatility-prediction)
  - [18. G-Research Crypto Forecasting](#18-g-research-crypto-forecasting)
  - [19. Ubiquant Market Prediction](#19-ubiquant-market-prediction)
- [Top 3 solutions](#top-3-solutions)
  - [1. Walmart Recruiting - Store Sales Forecasting](#1-walmart-recruiting---store-sales-forecasting-1)
  - [2. Walmart Recruiting II: Sales in Stormy Weather](#2-walmart-recruiting-ii-sales-in-stormy-weather-1)
  - [3. Rossmann Store Sales](#3-rossmann-store-sales-1)
  - [4. Web Traffic Time Series Forecasting](#4-web-traffic-time-series-forecasting-1)
  - [5. TalkingData AdTracking Fraud Detection Challenge](#5-talkingdata-adtracking-fraud-detection-challenge-1)
  - [6. Corporación Favorita Grocery Sales Forecasting](#6-corporaci%C3%B3n-favorita-grocery-sales-forecasting-1)
  - [7. Recruit Restaurant Visitor Forecasting](#7-recruit-restaurant-visitor-forecasting-1)
  - [8. Google Analytics Customer Revenue Prediction](#8-google-analytics-customer-revenue-prediction-1)
  - [9. LANL Earthquake Prediction](#9-lanl-earthquake-prediction-1)
  - [10. Two Sigma: Using News to Predict Stock Movements](#10-two-sigma-using-news-to-predict-stock-movements-1)
  - [11. ASHRAE - Great Energy Predictor III](#11-ashrae---great-energy-predictor-iii-1)
  - [12. University of Liverpool - Ion Switching](#12-university-of-liverpool---ion-switching-1)
  - [13. M5 Forecasting - Accuracy](#13-m5-forecasting---accuracy-1)
  - [14. Jane Street Market Prediction](#14-jane-street-market-prediction-1)
  - [15. Acea Smart Water Analytics](#15-acea-smart-water-analytics-1)
  - [16. Google Brain - Ventilator Pressure Prediction](#16-google-brain---ventilator-pressure-prediction-1)
  - [17. Optiver Realized Volatility Prediction](#17-optiver-realized-volatility-prediction-1)
  - [18. G-Research Crypto Forecasting](#18-g-research-crypto-forecasting-1)
  - [19. Ubiquant Market Prediction](#19-ubiquant-market-prediction-1)
- [Analysis](#analysis)
  - [Popularity trend of methods used by top 3 rankers](#popularity-trend-of-methods-used-by-top-3-rankers)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## List of competitions

| #   | Year      | Title                                                                                                                  | Data size |
|-----|-----------|------------------------------------------------------------------------------------------------------------------------|-----------|
| 1   | 2014      | [Walmart Recruiting - Store Sales Forecasting](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)    | 3.22MB    |
| 2   | 2015      | [Walmart Recruiting II: Sales in Stormy Weather](https://www.kaggle.com/c/walmart-recruiting-sales-in-stormy-weather)  | 9MB       |
| 3   | 2015      | [Rossmann Store Sales](https://www.kaggle.com/c/rossmann-store-sales)                                                  | 39.85MB   |
| 4   | 2017      | [Web Traffic Time Series Forecasting](https://www.kaggle.com/c/web-traffic-time-series-forecasting/overview)           | 611.85MB  |
| 5   | 2018      | [TalkingData AdTracking Fraud Detection Challenge](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/data)| 11.27GB   |
| 6   | 2018      | [Corporación Favorita Grocery Sales Forecasting](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/overview) | 479.88MB  |
| 7   | 2018      | [Recruit Restaurant Visitor Forecasting](https://www.kaggle.com/c/recruit-restaurant-visitor-forecasting/overview)     | 27.3MB    |
| 8   | 2018      | [Google Analytics Customer Revenue Prediction](https://www.kaggle.com/c/ga-customer-revenue-prediction/overview)       | 35.9GB    |
| 9   | 2019      | [LANL Earthquake Prediction](https://www.kaggle.com/c/LANL-Earthquake-Prediction/overview)                             | 10.42GB   |
| 10  | 2019      | [Two Sigma: Using News to Predict Stock Movements](https://www.kaggle.com/c/two-sigma-financial-news/overview)         | Not available |
| 11  | 2019      | [ASHRAE - Great Energy Predictor III](https://www.kaggle.com/c/ashrae-energy-prediction/overview)                      | 2.61GB    |
| 12  | 2020      | [University of Liverpool - Ion Switching](https://www.kaggle.com/c/liverpool-ion-switching/overview)                   | 146.08MB  |
| 13  | 2020      | [M5 Forecasting - Accuracy](https://www.kaggle.com/c/m5-forecasting-accuracy/overview)                                 | 450.47MB  |
| 14  | 2020-2021 | [Jane Street Market Prediction](https://www.kaggle.com/c/jane-street-market-prediction/overview)                       | Not available |
| 15  | 2020-2021 | [Acea Smart Water Analytics](https://www.kaggle.com/c/acea-water-prediction/overview)                                  | 3.45MB    |
| 16  | 2021      | [Google Brain - Ventilator Pressure Prediction](https://www.kaggle.com/c/ventilator-pressure-prediction/overview)      | 698.79MB  |
| 17  | 2022      | [Optiver Realized Volatility Prediction](https://www.kaggle.com/c/optiver-realized-volatility-prediction/overview)     | 2.73GB    |
| 18  | 2022      | [G-Research Crypto Forecasting](https://www.kaggle.com/c/g-research-crypto-forecasting)                                | 3.12GB    |
| 19  | 2022      | [Ubiquant Market Prediction](https://www.kaggle.com/c/ubiquant-market-prediction)                                      | 18.55GB   |

## Top 3 most voted EDAs
To learn the characteristic of data given in each competition, EDA is one of the best way.   
So top 3 most voted EDAs are listed.


### 1. [Walmart Recruiting - Store Sales Forecasting](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [EDA and Store Sales Predictions using XGB](https://www.kaggle.com/yasirhussain1987/eda-and-store-sales-predictions-using-xgb)
2. [Walmart prediction - (1) EDA with time and space](https://www.kaggle.com/yepp2411/walmart-prediction-1-eda-with-time-and-space)
3. [Wallmart Sales - EDA - feat eng [Future Update]](https://www.kaggle.com/maxdiazbattan/wallmart-sales-eda-feat-eng-future-update)

### 2. [Walmart Recruiting II: Sales in Stormy Weather](https://www.kaggle.com/c/walmart-recruiting-sales-in-stormy-weather)
[> Go to top](#Review-of-kaggle-time-series-competition)

NA

### 3. [Rossmann Store Sales](https://www.kaggle.com/c/rossmann-store-sales)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [Time Series Analysis and Forecasts with Prophet](https://www.kaggle.com/elenapetrova/time-series-analysis-and-forecasts-with-prophet)
2. [EDA and forecasting with RFRegressor_FINAL_UPDATED](https://www.kaggle.com/stefanozakher94/eda-and-forecasting-with-rfregressor-final-updated)
3. [How Does New Competition Affect Sales?](https://www.kaggle.com/ggep22/how-does-new-competition-affect-sales)

### 4. [Web Traffic Time Series Forecasting](https://www.kaggle.com/c/web-traffic-time-series-forecasting/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [Wiki Traffic Forecast Exploration - WTF EDA](https://www.kaggle.com/headsortails/wiki-traffic-forecast-exploration-wtf-eda)
2. [Web Traffic Time Series Forecasting (EDA)](https://www.kaggle.com/bodamanojkumar/web-traffic-time-series-forecasting-eda)
3. [Wikipedia Web traffic EDA](https://www.kaggle.com/mtao94/wikipedia-web-traffic-eda)

### 5. [TalkingData AdTracking Fraud Detection Challenge](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/data)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [TalkingData EDA plus time patterns](https://www.kaggle.com/yuliagm/talkingdata-eda-plus-time-patterns)
2. [TalkingData EDA and Class Imbalance](https://www.kaggle.com/kailex/talkingdata-eda-and-class-imbalance)
3. [TalkingData: EDA to Model Evaluation | LB: 0.9683](https://www.kaggle.com/pranav84/talkingdata-eda-to-model-evaluation-lb-0-9683)

### 6. [Corporación Favorita Grocery Sales Forecasting](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [Shopping for Insights - Favorita EDA](https://www.kaggle.com/headsortails/shopping-for-insights-favorita-eda)
2. [Memory optimization and EDA on entire dataset](https://www.kaggle.com/jagangupta/memory-optimization-and-eda-on-entire-dataset)
3. [Grocery EDA Dirty XGBoost, Arima,ETS,Prophet](https://www.kaggle.com/ambarish/grocery-eda-dirty-xgboost-arima-ets-prophet)

### 7. [Recruit Restaurant Visitor Forecasting](https://www.kaggle.com/c/recruit-restaurant-visitor-forecasting/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [Be my guest - Recruit Restaurant EDA](https://www.kaggle.com/headsortails/be-my-guest-recruit-restaurant-eda)
2. [Exhaustive Weather EDA/File Overview](https://www.kaggle.com/huntermcgushion/exhaustive-weather-eda-file-overview)
3. [Recruit Restaurant EDA](https://www.kaggle.com/fabiendaniel/recruit-restaurant-eda)

### 8. [Google Analytics Customer Revenue Prediction](https://www.kaggle.com/c/ga-customer-revenue-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [R EDA for GStore + GLM + KERAS + XGB](https://www.kaggle.com/kailex/r-eda-for-gstore-glm-keras-xgb)
2. [Google Analytics EDA + LightGBM + Screenshots](https://www.kaggle.com/erikbruin/google-analytics-eda-lightgbm-screenshots)
3. [A Very Extensive GStore Exploratory Analysis](https://www.kaggle.com/captcalculator/a-very-extensive-gstore-exploratory-analysis)


### 9. [LANL Earthquake Prediction](https://www.kaggle.com/c/LANL-Earthquake-Prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [Earthquakes FE. More features and samples](https://www.kaggle.com/artgor/earthquakes-fe-more-features-and-samples)
2. [LANL Earthquake EDA and Prediction](https://www.kaggle.com/gpreda/lanl-earthquake-eda-and-prediction)
3. [Masters Final Project: EDA](https://www.kaggle.com/vettejeep/masters-final-project-eda)

### 10. [Two Sigma: Using News to Predict Stock Movements](https://www.kaggle.com/c/two-sigma-financial-news/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [EDA, feature engineering and everything](https://www.kaggle.com/artgor/eda-feature-engineering-and-everything)
2. [👨‍🔬 Bird Eye 👀 view of Two Sigma + NN Approach](https://www.kaggle.com/ashishpatel26/bird-eye-view-of-two-sigma-nn-approach)
3. [Simple EDA - Two Sigma](https://www.kaggle.com/pestipeti/simple-eda-two-sigma)

### 11. [ASHRAE - Great Energy Predictor III](https://www.kaggle.com/c/ashrae-energy-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [🔌⚡ASHRAE -Start Here: A GENTLE Introduction](https://www.kaggle.com/caesarlupum/ashrae-start-here-a-gentle-introduction)
2. [EDA for ASHRAE](https://www.kaggle.com/nroman/eda-for-ashrae)
3. [A deep dive EDA into ALL variables](https://www.kaggle.com/jaseziv83/a-deep-dive-eda-into-all-variables)

### 12. [University of Liverpool - Ion Switching](https://www.kaggle.com/c/liverpool-ion-switching/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [Ion Switching Competition : Signal EDA 🧪](https://www.kaggle.com/tarunpaparaju/ion-switching-competition-signal-eda)
2. [EDA - Ion Switching](https://www.kaggle.com/pestipeti/eda-ion-switching)
3. [Simple EDA-Model](https://www.kaggle.com/siavrez/simple-eda-model)

### 13. [M5 Forecasting - Accuracy](https://www.kaggle.com/c/m5-forecasting-accuracy/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [Back to (predict) the future - Interactive M5 EDA](https://www.kaggle.com/headsortails/back-to-predict-the-future-interactive-m5-eda)
2. [M5 Competition : EDA + Models 📈](https://www.kaggle.com/tarunpaparaju/m5-competition-eda-models)
3. [Time Series Forecasting-EDA, FE & Modelling📈](https://www.kaggle.com/anshuls235/time-series-forecasting-eda-fe-modelling)

### 14. [Jane Street Market Prediction](https://www.kaggle.com/c/jane-street-market-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [Jane Street: EDA of day 0 and feature importance](https://www.kaggle.com/carlmcbrideellis/jane-street-eda-of-day-0-and-feature-importance)
2. [Jane_street_Extensive_EDA & PCA starter 📊⚡](https://www.kaggle.com/muhammadmelsherbini/jane-street-extensive-eda-pca-starter)
3. [EDA / A Quant's Prespective](https://www.kaggle.com/hamzashabbirbhatti/eda-a-quant-s-prespective)

### 15. [Acea Smart Water Analytics](https://www.kaggle.com/c/acea-water-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [Acea Smart Water: Full EDA & Prediction](https://www.kaggle.com/maksymshkliarevskyi/acea-smart-water-full-eda-prediction)
2. [EDA: Quenching the Thirst for Insights](https://www.kaggle.com/iamleonie/eda-quenching-the-thirst-for-insights)
3. [Quick EDA | Reporting & Data Understanding](https://www.kaggle.com/ekrembayar/quick-eda-reporting-data-understanding)

### 16. [Google Brain - Ventilator Pressure Prediction](https://www.kaggle.com/c/ventilator-pressure-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [Ventilator Pressure Prediction: EDA, FE and models](https://www.kaggle.com/artgor/ventilator-pressure-prediction-eda-fe-and-models)
2. [🔥EDA +FE+TabNet 🧠🧠[Weights and Biases]](https://www.kaggle.com/usharengaraju/eda-fe-tabnet-weights-and-biases)
3. [Ventilator Pressure: EDA and simple submission](https://www.kaggle.com/carlmcbrideellis/ventilator-pressure-eda-and-simple-submission)

### 17. [Optiver Realized Volatility Prediction](https://www.kaggle.com/c/optiver-realized-volatility-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [https://www.kaggle.com/chumajin/optiver-realized-eda-for-starter-english-version](https://www.kaggle.com/chumajin/optiver-realized-eda-for-starter-english-version)
2. [Optiver Realized Volatility Prediction - EDA](https://www.kaggle.com/gunesevitan/optiver-realized-volatility-prediction-eda)
3. [Optiver; EDA XGBoost starter(日本語,Japanese)](https://www.kaggle.com/matsuosan/optiver-eda-xgboost-starter-japanese)

### 18. [G-Research Crypto Forecasting](https://www.kaggle.com/c/g-research-crypto-forecasting)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [📊 G-Research Plots + EDA 📊](https://www.kaggle.com/odins0n/g-research-plots-eda)
2. [To The Moon 🚀 [G-Research Crypto Forecasting EDA]](https://www.kaggle.com/iamleonie/to-the-moon-g-research-crypto-forecasting-eda)
3. [📈📊[G-crypto] Interactive Dashboard + Indicators](https://www.kaggle.com/toomuchsauce/g-crypto-interactive-dashboard-indicators)

### 19. [Ubiquant Market Prediction](https://www.kaggle.com/c/ubiquant-market-prediction)
[> Go to top](#Review-of-kaggle-time-series-competition)

1. [EDA- target analysis](https://www.kaggle.com/lucamassaron/eda-target-analysis)
2. [Ubiquant EDA and Baseline](https://www.kaggle.com/ilialar/ubiquant-eda-and-baseline)
3. [🔥The most advanced analytics🔥](https://www.kaggle.com/kartushovdanil/the-most-advanced-analytics)


## Top 3 solutions

<style scoped>
table {
  font-size: 13px;
}
</style>

### 1. [Walmart Recruiting - Store Sales Forecasting](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                     |
|-----|---------|------------------------|-------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| 1   |         |                        |                   | [Kaggle-Walmart Sales Forecasting](https://github.com/davidthaler/Walmart_competition_code) | [First Place Entry](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/discussion/8125#) |
| 2   |         |                        |                   | NA                                                                                          | [Thank You and #2 rank model](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/discussion/8023#43811) |
| 3   |         |                        |                   | [Kaggle Walmart recruiting competition](https://ideone.com/pUw773)                          | [I used an almost brain dead technique:](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/discussion/8023#43821) |

### 2. [Walmart Recruiting II: Sales in Stormy Weather](https://www.kaggle.com/c/walmart-recruiting-sales-in-stormy-weather)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                                                                   | <div style="width:350px">Discussion</div>                                                                       |
|-----|---------|------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | [kaggle-walmart-recruiting-sales-in-stormy-weather](https://github.com/threecourse/kaggle-walmart-recruiting-sales-in-stormy-weather) | [First Place Entry](https://www.kaggle.com/c/walmart-recruiting-sales-in-stormy-weather/discussion/14452#80451) |
| 2   |         |                        |                   | NA                                                                                                                                    | NA                                                                                                              |
| 3   |         |                        |                   | NA                                                                                                                                    | NA                                                                                                              |


### 3. [Rossmann Store Sales](https://www.kaggle.com/c/rossmann-store-sales)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                     |
|-----|---------|------------------------|-------------------|------|---------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | NA   | [Congratulations to the other winners](https://www.kaggle.com/c/rossmann-store-sales/discussion/17896#101318) |
| 2   |         |                        |                   | NA   | NA                                                                                                            |
| 3   |         |                        |                   | [Code sharing, 3rd place, category embedding <br/>with deep neural network](https://www.kaggle.com/c/rossmann-store-sales/discussion/17974#101792) | [entity-embedding-rossmann](https://github.com/entron/entity-embedding-rossmann)                              |


### 4. [Web Traffic Time Series Forecasting](https://www.kaggle.com/c/web-traffic-time-series-forecasting/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                                               |
|-----|---------|------------------------|-------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | [kaggle-web-traffic](https://github.com/Arturus/kaggle-web-traffic)          | [1st place solution](https://www.kaggle.com/c/web-traffic-time-series-forecasting/discussion/43795#245823)                              |
| 2   |         |                        |                   | [Kaggle](https://github.com/jfpuget/Kaggle/tree/master/WebTrafficPrediction) | [My bet (2nd place)](https://www.kaggle.com/c/web-traffic-time-series-forecasting/discussion/39395)                                     |
| 3   |         |                        |                   | [gist:7d01f366a388516359915a4b090e29d4](https://gist.github.com/thousandvoices/7d01f366a388516359915a4b090e29d4) | [My approach was a linear combination of medians](https://www.kaggle.com/c/web-traffic-time-series-forecasting/discussion/39367#223730) |


### 5. [TalkingData AdTracking Fraud Detection Challenge](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/data)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                                            |
|-----|---------|------------------------|-------------------|------|--------------------------------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | NA   | [1st place solution](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/discussion/56475#326680)                        |
| 2   |         |                        |                   | NA   | [[2nd Place Solution] from PPP](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/discussion/56328#325630)             |
| 3   |         |                        |                   | NA   | [My brief summary,a mainly NN based solution(3th)](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/discussion/56262) |

### 6. [Corporación Favorita Grocery Sales Forecasting](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                          |
|-----|---------|------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | [1st Place LGB Model(public:0.506, private:0.511)](https://www.kaggle.com/shixw125/1st-place-lgb-model-public-0-506-private-0-511) <br/> <br/> [1st Place NN Model(public:0.507, private:0.513)](https://www.kaggle.com/shixw125/1st-place-nn-model-public-0-507-private-0-513) | [1st place solution](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/discussion/47582#269355)          |
| 2   |         |                        |                   | NA                                                                                                                                                                                                                                                                              | [2nd place solution overview](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/discussion/47568#269198) |
| 3   |         |                        |                   | NA                                                                                                                                                                                                                                                                              | [3rd place solution overview](https://www.kaggle.com/c/favorita-grocery-sales-forecasting/discussion/47560#269132) |


### 7. [Recruit Restaurant Visitor Forecasting](https://www.kaggle.com/c/recruit-restaurant-visitor-forecasting/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div> |
|-----|---------|------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| 1   |         |                        |                   | [1st Place LGB Model(public:0.470, private:0.502)](https://www.kaggle.com/pureheart/1st-place-lgb-model-public-0-470-private-0-502) <br/> <br/> [solution(public:0.471,private:0.505 )](https://www.kaggle.com/plantsgo/solution-public-0-471-private-0-505/script) | NA                                        |
| 2   |         |                        |                   | NA                                                                                                                                                                                                                                                                  | NA                                        |
| 3   |         |                        |                   | NA                                                                                                                                                                                                                                                                  | NA                                        |


### 8. [Google Analytics Customer Revenue Prediction](https://www.kaggle.com/c/ga-customer-revenue-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                                   |
|-----|---------|------------------------|-------------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | [Winning_solution](https://www.kaggle.com/kostoglot/winning-solution?scriptVersionId=10911396#L144) | [Winning solution (link to kernel inside)](https://www.kaggle.com/c/ga-customer-revenue-prediction/discussion/82614#482360) |
| 2   |         |                        |                   | NA                                                                                                  | [[2nd place solution] stacking with CNN](https://www.kaggle.com/c/imaterialist-challenge-fashion-2018/discussion/57934)     |
| 3   |         |                        |                   | NA                                                                                                  | NA                                                                                                                          |


### 9. [LANL Earthquake Prediction](https://www.kaggle.com/c/LANL-Earthquake-Prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                         |
|-----|---------|------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | [#1 private LB kernel LANL lgbm](https://www.kaggle.com/ilu000/1-private-lb-kernel-lanl-lgbm) <br/> <br/> [#1-Geomean NN and 6FeatLGBM<br/> [2.259 Private LB]](https://www.kaggle.com/dkaraflos/1-geomean-nn-and-6featlgbm-2-259-private-lb/notebook) | [1st place solution](https://www.kaggle.com/c/LANL-Earthquake-Prediction/discussion/94390#542982) |
| 2   |         |                        |                   | NA                                                                                                                                                                                                                                                | [2nd place solution](https://www.kaggle.com/c/LANL-Earthquake-Prediction/discussion/94369#542827) |
| 3   |         |                        |                   | NA                                                                                                                                                                                                                                                | [3rd place memo](https://www.kaggle.com/c/LANL-Earthquake-Prediction/discussion/94459#543607)     |


### 10. [Two Sigma: Using News to Predict Stock Movements](https://www.kaggle.com/c/two-sigma-financial-news/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

NA

### 11. [ASHRAE - Great Energy Predictor III](https://www.kaggle.com/c/ashrae-energy-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                          |
|-----|---------|------------------------|-------------------|------|--------------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | NA   | [1st Place Solution Team Isamu & Matt](https://www.kaggle.com/c/ashrae-energy-prediction/discussion/124709#711401) |
| 2   |         |                        |                   | NA   | [2nd Place Solution](https://www.kaggle.com/c/ashrae-energy-prediction/discussion/123481#704834)                   |
| 3   |         |                        |                   | NA   | [[3rd Place] Solution](https://www.kaggle.com/c/ashrae-energy-prediction/discussion/124984#713104)                 |


### 12. [University of Liverpool - Ion Switching](https://www.kaggle.com/c/liverpool-ion-switching/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                                                                                                                                                |
|-----|---------|------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | NA                                                                                                                  | [1st (or 16th) place short write up](https://www.kaggle.com/c/liverpool-ion-switching/discussion/153940#862403)                                                                                                                          |
| 2   |         |                        |                   | [2nd place solution. Preprocessing tricks](https://www.kaggle.com/stdereka/2nd-place-solution-preprocessing-tricks) | [2nd place solution](https://www.kaggle.com/c/liverpool-ion-switching/discussion/153991#862688) <br/> <br/>[2nd place solution (UPD: full code is disclosed)](https://www.kaggle.com/c/liverpool-ion-switching/discussion/155919#872833) |
| 3   |         |                        |                   | NA                                                                                                                  | [3rd place solution](https://www.kaggle.com/c/indoor-location-navigation/discussion/240161#1313777) <br/> <br/>[Brief 3rd place solution (Kha Vo view)](https://www.kaggle.com/c/liverpool-ion-switching/discussion/153734#861458)       |


### 13. [M5 Forecasting - Accuracy](https://www.kaggle.com/c/m5-forecasting-accuracy/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                     |
|-----|---------|------------------------|-------------------|------|---------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | NA   | [1st place solution](https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/163684#913208)               |
| 2   |         |                        |                   | NA   | [2nd place solution](https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/164599#917890)               |
| 3   |         |                        |                   | NA   | [3rd place solution - NN approach](https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/164374#916793) |

### 14. [Jane Street Market Prediction](https://www.kaggle.com/c/jane-street-market-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                                                 |
|-----|---------|------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 1   |         |                        |                   | [Jane Street 1st on LeaderBoard Notebook](https://www.kaggle.com/vikazrajpurohit/jane-street-1st-on-leaderboard-notebook) | NA                                                                                                                                        |
| 3   |         |                        |                   | NA                                                                                                                         | [3rd place solution: Ensembles of deep (49 layer) MLPs](https://www.kaggle.com/c/jane-street-market-prediction/discussion/224713#1232146) |
NA for Pos #2

### 15. [Acea Smart Water Analytics](https://www.kaggle.com/c/acea-water-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

NA

### 16. [Google Brain - Ventilator Pressure Prediction](https://www.kaggle.com/c/ventilator-pressure-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                                                           |
|-----|-----------------------------|------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | LSTM<br/> <br/>Transformer  | single architecture                            | KFold         | [[#1 Solution] LSTM CNN transformer (1 fold)](https://www.kaggle.com/shujun717/1-solution-lstm-cnn-transformer-1-fold) | [Winner's Writeup!](https://www.kaggle.com/c/ventilator-pressure-prediction/discussion/285256#1570087)                                              |
| 2   | Stacked LSTM                | ensembled by 7 models                          | KFold         | NA                                                                                                                     | [#2 Solution: The inverse of a PID controller](https://www.kaggle.com/c/ventilator-pressure-prediction/discussion/285283#1570285)                   |
| 3   | Conv1d<br/> <br/>Stacked LSTM | random seed average                            | Stratified K-Folds| NA                                                                                                                     | [[3rd Place] Single model scored 0.0975 w/o<br/> PID controller](https://www.kaggle.com/c/ventilator-pressure-prediction/discussion/285330#1570563) |


### 17. [Optiver Realized Volatility Prediction](https://www.kaggle.com/c/optiver-realized-volatility-prediction/overview)
[> Go to top](#Review-of-kaggle-time-series-competition)

| Pos | <div style="width:100px">Methods</div>  | <div style="width:130px">Ensemble</div> | <div style="width:120px">Data split</div> | <div style="width:320px">Code</div>                                                         | <div style="width:350px">Discussion</div>                                                                                           |
|-----|-----------------------------------------|-----------------------------------------------|-------------------------------------------|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 1   | LightGBM<br/> <br/>MLP<br/> <br/>CNN    | equally weighd average                        | GroupKFold                                | [1st place (public 2nd place) solution](https://www.kaggle.com/nyanpn/1st-place-public-2nd-place-solution) | [1st Place Solution - Nearest Neighbors](https://www.kaggle.com/c/optiver-realized-volatility-prediction/discussion/274970#1526710) |
| 3   | LightGBM<br/> <br/>MLP<br/> <br/>TabNet | equally weighd average                        | KFold                                     | [Third Place Solution](https://www.kaggle.com/eduardopeynetti/third-place-solution)                        | [3rd Place Solution](https://www.kaggle.com/c/optiver-realized-volatility-prediction/discussion/278588#1545008)                     |


NA for Pos #2

### 18. [G-Research Crypto Forecasting](https://www.kaggle.com/c/g-research-crypto-forecasting)
[> Go to top](#Review-of-kaggle-time-series-competition)

Ongoing

### 19. [Ubiquant Market Prediction](https://www.kaggle.com/c/ubiquant-market-prediction)
[> Go to top](#Review-of-kaggle-time-series-competition)

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








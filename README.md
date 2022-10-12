# Application-of-Time-Series-Forecasting-in-Real-Estate-Valuation


> The project involves a real-world dataset, the work is categorized into three main parts:

- Notebook 1: EDA & Feature Engineering.
- Notebook 2: Static Modeling for Producing Time Series
- Notebook 2: Mean-Point Time Series Modeling
  
We will be working with a dataset of Tokyo real estate trades published by Ministry of Land, 
Infrastructure, Transport and Tourism of Japan (MLIT). 
The dataset is originally reported in Japanese language and was translated by a Kaggle contributor. In addition to the trades data, 
we will be incorporating the housing consumer price index for Japan.
After EDA & feature engineering we will proceed to with two different approaches to model the prices, the approaches in a nutshell:

- Static Modeling for Producing Time Series: We will produce static models for every quarter of every year. Then predict the price of an instance, using all quarter models. The result is a predicted time series which will then be forecasted into the future using an LSTM. It should be noted that the timestamps ['Year’, ‘Quarter'] are not features in this approach.


- Mean-Point Time Series Modeling: The pipeline is built to take an instance X, and produce a time series that best represents X. The time series is then forecasted using baseline models and an LSTM model. The catch in this approach is that the time series produced does not come from model predictions (as in the approach in notebook 2), rather it is produced by sampling from the full dataset based on certain criteria.

The columns we will be working with initially:

```
The data is collected from the following sources:
```
![image](https://user-images.githubusercontent.com/92155597/195355657-2dd2ac52-1797-47a1-94dc-b852c4f9eab5.png)

#### • For Trades data: https://www.kaggle.com/datasets/nishiodens/japan-real-estate-transaction-prices
#### • For Housing Consumer Price index: https://fred.stlouisfed.org/series/JPNCPGRHO01IXOBQ

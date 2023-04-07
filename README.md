# Favorita Supermarket Forecasting  Advanced Time series Analysis
Kaggle competition in Advanced Time Series Forecasting best model 70th!! place at the time.


## FbProphet model.


Models were running in parallel.
Developing multiple FbProphet models with additional regressors , hyperparameter tuning and default methods.
FbProphet is very hard on RAM memory especialy since prophet is using some ARIMA code under the hood.
Couple of FbProphet models can quickly fill up RAM memory if running in parallel. So it's better to split them depending on what type of model is beeing trained.
Since this problem has 1782 distinct models, every store has it's own family product model. In one case I splilt them in 5 separete section and another in 3.
All models are trained in Google Colab using paid packages for resources.
FbProhet models are set to be trained in parallel , Colab had 54 CPU cores. 
Array with 1782 DataFrames is created and splited 5 or 3 times depending on a model. Had to delete trained models because of large memory consumption.


## Custom Models and EDA


EDA was used for time series analysis and for feature engineering. Same data was used for trainig FbProphet models.
Multiple Custom Models are developed with treir analysis.
Pipelines are created for each model.
UpGini was used for external data.

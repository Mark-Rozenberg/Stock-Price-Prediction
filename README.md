# Stock-Price-Prediction

### **Project Name**
Prediction of AugWind company stock price using search data from google trends and different Python time series forecasting techniques

### **Data Origin**
This project based on a dataset combined from two sources:
  1. Google trends
  2. Tel-Aviv stock exchange site

### **Data Description**
The data is relevant from 11/5/2020 up to 12/2/2021, a bit more than a year. The time frequency is daily.\
**Variables:**\
'Date' - format mm/dd/yyyy\
'Aug_Price' - AugWind (1105907) stock price in new israeli shekels (0.01 NIS)\
'Aug_Volume' - AugWind stock daily turnover (NIS Thousands)\
'Search' - Google Trends search interest rate (search word= ‘אוגווינד’, AugWind in hebrew, search region = Israel, web search only)\
Note: the data presented by google is with weekly frequency\
'CleanTec_Price' - Tel-Aviv clean Tech Index (184) in points\
'CleanTec_Volume' - Tel-Aviv clean Tech Index daily turnover (NIS Thousands)\

### **Analysis Description**
Step 1 – data preparation: set date indexes. Fill empty cells using the pandas ffill method. Due to the fact that the 'Search' variable is with weekly frequency the method is necessary. 

Step 2 – simple data exploration using a correlation matrix between all the variables to find strongly correlated variables. Graphical exploration of trend and seasonality components of AugWind stock price.

Step 3 – fitting 5 different model for prediction:
  1. Simple linear regression, without features (explanatory variables)
  2. Simple linear regression, with features 
  3. ARIMA (SARIMAX), without features
  4. ARIMA (SARIMAX), with features
  5. LSTM - PyTorch\

Note: the data was splitted to train up to the 11/1/2021 and test from 11/2/2021

Step 4 – comparing the prediction results using common metrics and graphical representation

### **Discussion**
LSTM model was the most efficient in predicting. The ARIMA model combined with features did very well with scores close to LSTM. There are techniques to find the most appropriate AR and MA parameters for the ARIMA model. With some configuration of the models parameters the results can be improved.

### **KeyWords**
Forecasting, Prediction, Stock prices, AugWind, Linear Regression, ARIMA, SARIMAX, LSTM, PyTorch, Google Trends


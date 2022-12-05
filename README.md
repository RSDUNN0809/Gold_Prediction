# Gold_Prediction

### Project Intro/Objective

In this study, the topic that will be investigated and forecasted will be gold prices in the financial market(s). For this time series forecast, the gold prices will be retrieved as daily time series data from November 12, 2012 to November 12, 2022. The prediction of the gold prices forecasted will be evaluated with common external indicators and/or factors that will allow the determination of a relationship that may or may not exist with the price of gold. Such indicators include Money supply, US dollar index, Unemployment rate, Internet web hits of gold, Dow Jones Industrial Average, Silver prices, and Federal funds rate. While gold has maintained its value throughout history, the interest for this project is the intention to research and identify key relationships of gold pricing with the selected external information which will lead indications on the best times to invest in gold for future investors.

### Partners/Contributors

* Ryan Dunn
* Amin Fesharaki
* Kyle Esteban Dalope

### Methods Used

* Time Series Analysis
* Predicitve Modeling
* ARIMA
* Logistic Regression 
* Facebook Prophet

### Technologies

* R
* Excel

### Project Description 

For this study, all work and processing was conducted through the programming language and environment of R. The selected dataset for the gold prices, Gold.csv, has been sourced from Nasdaq which contained 2549 features with six variables which include Date, Close/Last, Volume, Open, High, and Low; however, only Data and Close/Last were used in this study. As each of the .csv files were imported, the initial steps were to identify any key identifiers, trends, seasonality, and distributions that may have existed through the process of exploratory data analysis. All datasets were downloaded at the 5-year level, covering the periods of November 2017 to November 2022. Table A1 overviews all of the .csv files that contained all of the datasets of interest with a brief description for each along with their sources.

All predictor datasets were left joined onto the Gold.csv file by date; however, not all data was available at the daily level. For some predictor variables, such as the unemployment rate, data is only updated monthly. To address this misalignment in data granularity, the MIN and MAX date of each dataset was captured, and a date object was created which contained all days in between. By using the mutate function and na_locf functions in base R, the most recent value for a given predictor variable was used to fill in all daily date ranges until a new value was found. This enabled the data to be downloaded at various levels and mutated into a daily level that was able to be joined onto the daily gold data. Each data attribute was then normalized for the purposes of comparing trends on a single axis and for potential use in predictive models that require the data be on the same scale.  


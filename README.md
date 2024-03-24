## Table of Content
- [Overview](#overview)
- [Motivation](#motivation)
- [Technical Aspect](#technical-aspect)
- [Installation](#installation)
- [Report & Codes](#report--codes)

## Overview
Recent assertions indicate a rise in violent crimes in the UK, prompting significant government intervention and strategic responses. Analysis of crime data from various UK police forces spanning December 2010 to April 2013 was conducted through time series analysis. Despite visual indications suggesting a decrease in violent crime during this period, a more comprehensive statistical investigation, including decomposition into trend, seasonality, and noise components, revealed a different perspective. A Seasonal ARIMA (SARIMA) model was employed to forecast future violent crime behavior, demonstrating high accuracy and performance.

## Motivation
This project aims to employ Correlation, Regression, and Time Series analyses to rigorously investigate the interrelations between variables including violent crime rates, firearm offenses, and drug-related crimes in the UK. The study seeks to validate claims of rising violent crime rates and forecast future crime levels for informed policymaking.

## Technical Aspect
To initialize the data pipeline, the crime data was downloaded from the above-mentioned website and imported in a csv.gz format to a Sparksession using Jupyter notebook. A Sparksession allows for the creation of dataframes, registering dataframe tables and querying of tables using SQL in Pyspark.

### Data Processing
The dataset comprising 65,078,250 rows and 12 columns, collected from December 2010 to April 2013, underwent meticulous review and manipulation using appropriate Pyspark functions. Missing values, identified as NA, were dropped to prevent bias in subsequent analyses.

### Data Extraction
Filtered and extracted data subsets were transformed into Pandas dataframes to facilitate conversion of string date types to datetime, enabling indexation for time series analysis.

[Find the Data for this project HERE](https://data.police.uk/)

### Time Series Analysis
A time series analysis was conducted to evaluate crime rate trends in the UK. The analysis revealed a decreasing trend in violent crime rates over time, with occasional spikes. To prepare the data for statistical modeling, stationarity was ensured through differencing. The Augmented Dickey-Fuller test confirmed the need for differencing to achieve stationarity

![image](https://github.com/Mattdozie/Forecasting-Future-Trends-SARIMA-Modeling-of-Violent-Crime-in-the-UK/assets/100968289/e18550d5-275b-4a5c-9361-20db3e01779b)


![image](https://github.com/Mattdozie/Forecasting-Future-Trends-SARIMA-Modeling-of-Violent-Crime-in-the-UK/assets/100968289/f5e05a44-e1ca-4d3f-9c4a-bca3fbb258f5)

![image](https://github.com/Mattdozie/Forecasting-Future-Trends-SARIMA-Modeling-of-Violent-Crime-in-the-UK/assets/100968289/8928e772-fbd5-42ca-b72f-2dfd0c2bf713)


### Seasonal ARIMA Model
The Seasonal ARIMA model, designed to manage seasonality in time series data, was applied for forecasting UK crime rates. Despite its simplicity and interpretability, SARIMA's requirement for significant data amounts and assumption of linear relationships were noted limitations.

## Installation
<div>
<img src="https://img.shields.io/badge/-Spark_SQL-E25A1C?&style=for-the-badge&logo=Apache-Spark&logoColor=white" />
<img src="https://img.shields.io/badge/-PySpark-E25A1C?&style=for-the-badge&logo=Apache-Spark&logoColor=white" />
<img src="https://img.shields.io/badge/-NumPy-013243?&style=for-the-badge&logo=NumPy&logoColor=white" />
<img src="https://img.shields.io/badge/-Seaborn-388E3C?&style=for-the-badge&logo=Seaborn&logoColor=white" />
<img src="https://img.shields.io/badge/-Matplotlib-377EB8?&style=for-the-badge&logo=Python&logoColor=white" />
<img src="https://img.shields.io/badge/-Pandas-150458?&style=for-the-badge&logo=Pandas&logoColor=white" />
<img src="https://img.shields.io/badge/-OpenCV-5C3EE8?&style=for-the-badge&logo=OpenCV&logoColor=white" />
<img src="https://img.shields.io/badge/-Statsmodels-007ACC?&style=for-the-badge" />
<img src="https://img.shields.io/badge/-itertools-007ACC?&style=for-the-badge" />
</div>

## Report & Codes
The final [Report and codes for this project can be found HERE](insert_link_here)

Plot above shows the model making prediction beyond the original data date, two years into the future.

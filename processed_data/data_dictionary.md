# Data Dictionary

## Descriptive and Diagnostic Analytics (Power BI)

For descriptive and diagnostic analytics, the datasets are kept separate and modeled individually in Power BI. 
This document provides definitions and descriptions of all datasets and variables used in the USD/CAD exchange rate analysis project.

The datasets are divided into two categories:
1. Individual datasets used for descriptive and diagnostic analytics in Power BI.
2. A combined dataset (FX_Master) used for predictive analytics in Python.

### CPI.csv

| Dataset Name | Column Name | Description | Data Type | Data Source |
|--------------|-------------|-------------|----------|-------------|
| CPI.csv | Date | Observation date of inflation data | Date | Statistics Canada |
| CPI.csv | Inflation_Canada | CPI inflation rate for Canada | Decimal | Statistics Canada |
| CPI.csv | Inflation_US | CPI inflation rate for United States | Decimal | US Bureau of Labor Statistics |
| CPI.csv | Inflation_Spread | Difference between inflation rates | Decimal | Calculated |

### FX_Rate.csv

| Dataset Name | Column Name | Description | Data Type | Data Source |
|--------------|-------------|-------------|----------|-------------|
| FX_Rate.csv | Date | Exchange rate observation date | Date | Bank of Canada |
| FX_Rate.csv | USD_CAD_FX | USD/CAD exchange rate | Decimal | Bank of Canada |

### GDP.csv

| Dataset Name | Column Name | Description | Data Type | Data Source |
|--------------|-------------|-------------|----------|-------------|
| GDP.csv | Date | GDP observation date | Date | Statistics Canada |
| GDP.csv | GDP_Spread | GDP growth rate difference | Decimal | Calculated |

### Gold_Rate.csv

| Dataset Name | Column Name | Description | Data Type | Data Source |
|--------------|-------------|-------------|----------|-------------|
| Gold_Rate.csv | Date | Gold price observation date | Date | Commodity markets |
| Gold_Rate.csv | Gold_USD | Gold price per ounce | Decimal | Commodity markets |

### Oil_Rates.csv

| Dataset Name | Column Name | Description | Data Type | Data Source |
|--------------|-------------|-------------|----------|-------------|
| Oil_Rates.csv | Date | Oil price observation date | Date | Commodity markets |
| Oil_Rates.csv | Oil_USD | Oil price per barrel | Decimal | Commodity markets |

### Policy Rate Difference.csv

| Dataset Name | Column Name | Description | Data Type | Data Source |
|--------------|-------------|-------------|----------|-------------|
| Policy Rate Difference.csv | Date | Policy rate observation date | Date | Federal Reserve |
| Policy Rate Difference.csv | Policy_Spread | Difference between interest rates | Decimal | Calculated |

### Trade_Balance.csv

| Dataset Name | Column Name | Description | Data Type | Data Source |
|--------------|-------------|-------------|----------|-------------|
| Trade_Balance.csv | Date | Trade balance observation date | Date | Government trade data |
| Trade_Balance.csv | Trade_Balance | Trade balance value in CAD | Decimal | Government trade data |

---

## Predictive Analytics Dataset

For predictive analytics, a combined dataset named **FX_Master.csv** was created by merging the relevant variables from the individual datasets.

| Column Name | Description | Data Type | Example Value | Source |
|-------------|-------------|----------|---------------|--------|
| Date | Observation date for macroeconomic indicators and exchange rate values | Date | 2018-01-31 | Combined datasets |
| GDP_Spread | Difference between US and Canadian GDP growth rates | Decimal | 0.0124 | Calculated from GDP dataset |
| Gold_USD | Price of gold per ounce in US dollars | Decimal | 1347.90 | Commodity market data |
| Inflation_Spread | Difference between US and Canadian inflation rates (CPI based) | Decimal | 0.0045 | Calculated from CPI dataset |
| Oil_USD | Global crude oil price per barrel in US dollars | Decimal | 63.69 | Global commodity markets |
| Policy_Spread | Difference between US Federal Reserve interest rate and Bank of Canada policy rate | Decimal | 0.29 | Calculated from policy rate dataset |
| Trade_Balance | Trade balance value between Canada and the United States | Decimal | 3427.40 | Government trade statistics |
| USD_CAD_FX | Exchange rate representing the value of the US Dollar relative to the Canadian Dollar | Decimal | 1.2427 | Bank of Canada |


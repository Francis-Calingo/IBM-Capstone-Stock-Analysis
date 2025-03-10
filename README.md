# CapstoneProject-StockAnalysis

## Table of Contents
* [Introduction](#introduction)
* [Code and Resources Used](#code-and-resources-used)
* [Methodology](#methodology)
  * [Step 1: Defining Graph Function](#step-1-defining-graph-function)
  * [Step 2: Use yfinance to Extract Tesla Stock Data](#step-2-use-yfinance-to-extract-tesla-stock-data)
  * [Step 3: Webscraping to Extract Tesla Revenue Data](#step-3-webscraping-to-extract-tesla-revenue-data)
  * [Step 4: Use yfinance to Extract GameStop Stock Data](#step-4-use-yfinance-to-extract-gamestop-stock-data)
  * [Step 5: Webscraping to Extract GameStop Revenue Data](#step-5-webscraping-to-extract-gamestop-revenue-data)
  * [Step 6: Plotting Tesla and GameStop Stock Graphs](#step-6-plotting-tesla-and-gamestop-stock-graphs)
* [Discussion](#discussion)

## Introduction
  <ul>
    <li>Performed data visualizations and geospatial analysis of settlement patterns of immigrants (permanent and non-permanent) in Canada.</li>
    <li>National, provincial and territorial, and census metropolitan area [CMA] breakdown</li>
    <li>Scraped data from Statistics Canada. (census data and quarterly estimates)</li>
    <li>Performed feature engineering on some variables to create new variables.</li>
    <li>Downloaded shapefile of Canada's provincial and territorial boundaries to create choropleth map.</li>
    <li>N.B. 1: Some of the data from Statistics Canada are estimates based on 25% sampling.</li>
    <li>N.B. 2: For the purpose of this analysis, the Ottawa-Gatineau CMA was broken up into two parts: its Ontario and Quebec part, rendering the analysis of the "Top 25" CMAs Top 26.</li>
    <li>N.B. 3: Statistics Canada's definition of "recent immigrants" is those that migrated to Canada within the last 5 years of a census year (e.g., 2016-2021, 2011-2016, 2006-2011, etc.)</li>
  </ul>
  
## Code and Resources Used
  <ul>
    <li><b>IDEs Used:</b> Google Colab, Jupyter Notebook</li>
    <li><b>Python Version:</b> 3.10.12</li>
    <li><b>Libraries and Packages:</b> yfinance, pandas, requests, BeautifulSoup, plotly.graph_objects, make_subplots</li>
  </ul>

## Methodology

### Step 1: Defining Graph Function
Define a function where the inputs will draw upon the stock data that is to be taken from the stock data from the yfinance library later. Below is the code snippet:
![image](https://github.com/user-attachments/assets/f75d8f04-a80e-480d-804c-f188ee740bbf)

### Step 2: Use yfinance to Extract Tesla Stock Data
Use the following:
<ul>
  <li>Tesla = yf.Ticker("TSLA")</li>
  <li>Tesla_data = Tesla.history(period="max")</li>
  <li>Tesla_data.reset_index(inplace=True)</li>
  <li>Tesla_data.head()</li>
</ul>

This will generate the first 5 rows of the data:
![image](https://github.com/user-attachments/assets/e14d8101-098a-4341-a529-899027684d3e)

### Step 3: Webscraping to Extract Tesla Revenue Data

### Step 4: Use yfinance to Extract GameStop Stock Data

### Step 5: Webscraping to Extract GameStop Revenue Data

### Step 6: Plotting Tesla and GameStop Stock Graphs
![image](https://github.com/user-attachments/assets/87d24e6e-47c4-44e3-9ba5-bde0a0c44a3c)

![image](https://github.com/user-attachments/assets/ba18cff1-86d2-4e66-9c35-ce50ade6b0aa)


![image](https://github.com/user-attachments/assets/cd349126-5d06-488a-8128-6a158befa284)

![image](https://github.com/user-attachments/assets/09381ab0-0502-426a-9330-4857f6f77c94)

## Discussion


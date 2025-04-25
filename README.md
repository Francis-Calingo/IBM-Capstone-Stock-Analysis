# IBM Data Science Professional Certificate Capstone Project: Stock Price and Revenue Analysis

## Table of Contents
* [Introduction](#introduction)
* [Code and Setup](#code-and-setup)
* [Methodology](#methodology)
  * [Step 1: Defining Graph Function](#step-1-defining-graph-function)
  * [Step 2: Use yfinance to Extract Tesla Stock Data](#step-2-use-yfinance-to-extract-tesla-stock-data)
  * [Step 3: Webscraping to Extract Tesla Revenue Data](#step-3-webscraping-to-extract-tesla-revenue-data)
  * [Step 4: Use yfinance to Extract GameStop Stock Data](#step-4-use-yfinance-to-extract-gamestop-stock-data)
  * [Step 5: Webscraping to Extract GameStop Revenue Data](#step-5-webscraping-to-extract-gamestop-revenue-data)
  * [Step 6: Plotting Tesla and GameStop Stock Graphs](#step-6-plotting-tesla-and-gamestop-stock-graphs)
* [Discussion](#discussion)

<details><summary><h2>Introduction</h2></summary> 
  <ul>
    <li>Extracted, analyzed, and visualized Tesla and GameStop stock data using yfinance, BeautifulSoup, and plotly.</li>
    <li>Part of IBM's Data Science Professional Certificate Program.</li>
  </ul>

[<b>Back to Table of Contents</b>](#table-of-contents)
</details>

<details><summary><h2>Code and Setup</h2></summary> 
  <ul>
    <li><b>IDEs Used:</b> Google Colab, Jupyter Notebook</li>
    <li><b>Python Version:</b> 3.10.12</li>
    <li><b>Libraries and Packages:</b> yfinance, pandas, requests, BeautifulSoup, plotly.graph_objects, make_subplots</li>
  </ul>

If you'd like to fork or run this locally:

```bash
git clone https://github.com/Francis-Calingo/IBM-Capstone-Stock-Analysis.git
cd IBM-Capstone-Stock-Analysis
```
To install the necessary Python libraries and packages:
```bash
pip install -r requirements.txt
```

[<b>Back to Table of Contents</b>](#table-of-contents)
</details>


<details><summary><h2>Methodology</h2></summary> 

### Step 1: Defining Graph Function
Define a function where the inputs will draw upon the stock data that is to be taken from the stock data from the yfinance library later. Below is the code snippet:
![image](https://github.com/user-attachments/assets/f75d8f04-a80e-480d-804c-f188ee740bbf)

### Step 2: Use yfinance to Extract Tesla Stock Data
Use the following method:
<ul>
  <li>Tesla = yf.Ticker("TSLA")</li>
  <li>Tesla_data = Tesla.history(period="max")</li>
  <li>Tesla_data.reset_index(inplace=True)</li>
  <li>Tesla_data.head()</li>
</ul>

This will generate the first 5 rows of the data:
![image](https://github.com/user-attachments/assets/e14d8101-098a-4341-a529-899027684d3e)

### Step 3: Webscraping to Extract Tesla Revenue Data
Use the following method:
<ul>
  <li>1: Use 'requests' library to download fromt the following link, then save the text of the response as a variable: https://www.google.com/url?q=https%3A%2F%2Fcf-courses-data.s3.us.cloud-object-storage.appdomain.cloud%2FIBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork%2Flabs%2Fproject%2Frevenue.htm</li>
  <li>2: Use the library 'beautiful_soup' to parse the html data using a parser.</li>
  <li>3: Using either BeautifulSoup or read_html to extract the Tesla Revenue table, then store it in a dataframe. Example code snippet:</li>
</ul>
![image](https://github.com/user-attachments/assets/9880b015-4359-4f94-96aa-b93716cd2d33)


The result:
![image](https://github.com/user-attachments/assets/6f3a6ba1-5c8f-4031-b1e7-3ea567b8ec24)

### Step 4: Use yfinance to Extract GameStop Stock Data
Execute a code snippet similar to that from Step 2, with "GME" as the stock code. The result:
![image](https://github.com/user-attachments/assets/8cbce554-c77b-4de4-ad75-56a920a34712)

### Step 5: Webscraping to Extract GameStop Revenue Data
Execute a code snippet similar to that from Step 4, but for the GameStop stock, The result:
![image](https://github.com/user-attachments/assets/e744cfea-5ab6-48a4-9810-d1f49cfca5c4)

### Step 6: Plotting Tesla and GameStop Stock Graphs

Tesla stock and revenue data:
![image](https://github.com/user-attachments/assets/87d24e6e-47c4-44e3-9ba5-bde0a0c44a3c)

![image](https://github.com/user-attachments/assets/ba18cff1-86d2-4e66-9c35-ce50ade6b0aa)


GameStop stock and revenue data:
![image](https://github.com/user-attachments/assets/cd349126-5d06-488a-8128-6a158befa284)

![image](https://github.com/user-attachments/assets/09381ab0-0502-426a-9330-4857f6f77c94)

[<b>Back to Table of Contents</b>](#table-of-contents)
</details>


<details><summary><h2>Discussion</h2></summary> 
It appears that Tesla's stock exploded around the 2020s, which is to be expected as the popularity of electric vehicles continue to increase from the increased production and shift in government policies to encourage EV production as part of their efforts to mitigate climate change:
 
![image](https://github.com/user-attachments/assets/c11ed9a6-b73f-4c75-97b2-d18466dd6dbb)

In similar fashion, revenue has increased over time:
![image](https://github.com/user-attachments/assets/6a0a9249-c943-48a9-b5f6-3d21d18b2a96)


GameStop's plots present an interesting story. We can observe a drastic spike on GameStop's stocks, which we would expect, given that on January 2021, users of r/wallstreetbets, a Reddit subreddit, initiated a short squeeze (rapid increase of the price of an undervalued stock due to sellers buying the stock in excess) on GameStop by driving up the price of the stock, resulting in a massive spike in its stock value over the next few days:
![image](https://github.com/user-attachments/assets/c4f5f7be-6d17-4302-b115-d49f6519b49b)

There is unfortunately no readily available data from yfinance on GameStop's revenue during that same time period:
![image](https://github.com/user-attachments/assets/f8faed49-5ffb-41d1-ac55-fb2446736169)

These are just two of countless examples of external events (anticipated or not) having significant effects on stock prices and revenues. Consumer behavioural trends and government policies could help people predict stock performance, although as events such as the COVID-19 outbreak and the GameStop Short Squeeze demonstrate that unexpected events could be just as, if not more, impactful on stocks.

[<b>Back to Table of Contents</b>](#table-of-contents)
</details>


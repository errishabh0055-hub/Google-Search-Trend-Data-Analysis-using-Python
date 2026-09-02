# 📊 Google Search Trend Data Analysis using Python

## 📌 Project Overview

This project analyzes **Google Search Trends data using Python and PyTrends**. The project directly retrieves search-interest data from Google Trends based on a selected keyword and uses Python libraries to clean, analyze, and visualize the data.

For this analysis, the keyword **"BMW"** is used to understand how search interest varies over time and across different regions.

The main goal of this project is to demonstrate how Python can be used to collect real-world search trend data and convert it into meaningful insights through data analysis and visualization.

---

## 🚀 Key Features

* 📥 Directly fetch Google Trends data using **PyTrends**
* 🔎 Analyze search interest for a selected keyword
* 🌍 Analyze **region/country-wise search interest**
* 📅 Analyze search trends over the **last 12 months**
* 📊 Create visualizations using Python
* 📈 Sort and identify regions with the highest search interest
* 📋 Use Pandas for data manipulation and analysis
* 🎨 Use Seaborn, Matplotlib, and Plotly for visualization

---

## 🛠️ Technologies & Libraries

* **Python**
* **PyTrends** – Google Trends data collection
* **Pandas** – Data manipulation and analysis
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Plotly** – Interactive visualization
* **Jupyter Notebook** – Development and analysis environment

---

## 📦 Installation

Install the required Python libraries:

```bash
pip install pytrends pandas matplotlib seaborn plotly
```

---

## 🔄 How It Works

### 1. Import Libraries

The project uses Python data-analysis and visualization libraries along with PyTrends.

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
from pytrends.request import TrendReq
```

### 2. Connect to Google Trends

PyTrends is initialized using `TrendReq`.

```python
pytrends = TrendReq(hl='en-US', tz=360)
```

### 3. Define the Keyword

The keyword can be changed according to the analysis requirement.

```python
keyword = "bmw"
```

### 4. Request Google Trends Data

The project requests Google Trends data for the selected keyword over the previous 12 months.

```python
pytrends.build_payload(
    [keyword],
    cat=0,
    timeframe='today 12-m',
    geo='',
    gprop=''
)
```

### 5. Analyze Regional Interest

The project retrieves region-wise search interest and identifies the top regions.

```python
region_data = pytrends.interest_by_region()

region_data = region_data.sort_values(
    by=keyword,
    ascending=False
).head(15)
```

---

## 📊 Analysis Performed

The project focuses on:

### 🔹 Search Interest Over Time

Google Trends search-interest data can be analyzed to identify:

* Increasing search interest
* Decreasing search interest
* Search peaks
* Search patterns over the selected period

### 🔹 Regional Search Interest

The project compares search interest between regions and extracts the **top 15 regions** with the highest interest for the selected keyword.

This can help identify where a particular topic, product, or brand is receiving comparatively higher search attention.

---

## 📈 Visualizations

The project uses:

* **Matplotlib**
* **Seaborn**
* **Plotly**

to transform the Google Trends data into easy-to-understand charts and visualizations.

---

## 💡 Use Cases

This type of Google Search Trend analysis can be useful for:

* 📢 Digital marketing
* 🔍 Keyword research
* 📈 Market research
* 🚗 Automotive industry analysis
* 🛒 Product research
* 🌐 SEO research
* 📊 Business intelligence
* 📱 Content strategy
* 📅 Identifying search trends

---

## ⚠️ Important Note

Google Trends provides **relative search-interest data**, not absolute search-volume numbers. The values represent search interest relative to the highest point within the selected query, time period, and geography.

PyTrends retrieves data from Google Trends programmatically, so availability and behavior may depend on Google's current service and rate limits.

---

## 📁 Project Structure

```text
Google-Search-Data-Analysis/
│
├── google search keyword analysis.ipynb
└── README.md
```

---

## 🎯 Project Objective

The objective of this project is to demonstrate practical **data collection, data manipulation, exploratory analysis, and visualization skills using Python** by working with real-world Google search trend data.

---

## 👨‍💻 Author

**Rishabh Parashar**

Python | Data Analysis | Data Visualization

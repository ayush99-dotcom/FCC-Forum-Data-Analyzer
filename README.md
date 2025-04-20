# 📊 Forum Page View Analysis

This project analyzes **daily page views** on the FreeCodeCamp forum using time series data. It includes data cleaning and visualizations built with **Matplotlib** and **Seaborn**.

## 📁 Overview

- **Goal**: Visualize trends and distributions in page views over time.
- **Tools**: Python, Pandas, Matplotlib, Seaborn, Jupyter Notebook

## 🧹 Data Cleaning

Outliers in the top and bottom 2.5% of daily page views were removed using:

```python
df = df[(df['value'] > df['value'].quantile(0.025)) & 
        (df['value'] < df['value'].quantile(0.975))]
```

## 📊 Visualizations

The notebook generates the following visualizations:

### 1. 📈 Line Plot
Shows daily page views over time with date on the x-axis and views on the y-axis.

### 2. 📊 Bar Plot
Displays average monthly page views grouped by year to show seasonal patterns.

### 3. 📦 Box Plots
- **Year-wise**: Distribution of views for each year.
- **Month-wise**: Seasonal distribution of views across months.

## 📁 Dataset
https://github.com/ayush99-dotcom/FCC-Forum-Data-Analyzer/blob/main/fcc-forum-pageviews.csv
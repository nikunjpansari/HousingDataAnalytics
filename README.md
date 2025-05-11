# Housing Data Analytics using Google BigQuery

An end-to-end walkthrough of building a Housing Data analytics solution in Power BI, sourcing data from Google BigQuery, performing transformations, modeling with DAX, and creating interactive visuals.

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Prerequisites](#prerequisites)  
3. [Create Free Google Cloud Account](#create-free-google-cloud-account)  
3. [SQL in BigQuery for Data Understanding & Transformations](#sql-in-bigquery-for-data-understanding--transformations)  
4. [Data Cleaning in Power Query Editor](#data-cleaning-in-power-query-editor)  
5. [Data Modeling & DAX Measures](#data-modeling--dax-measures)  
   - [YOY Sales Growth](#yoy-sales-growth)  
   - [Offer Price Column](#offer-price-column)  
   - [Median Sales Price Change by Region](#median-sales-price-change-by-region)  
   - [Units Sold (Latest Year & Quarter)](#units-sold-latest-year--quarter)  
   - [Last 12 Month Sales](#last-12-month-sales)  
   - [Sales by Region](#sales-by-region)  
   - [Total YTD Sales](#total-ytd-sales)  
   - [Offer to SQM Ratio](#offer-to-sqm-ratio)  
   - [Age Column](#age-column)  
6. [Report Development](#report-development)  
   - [Sales Performance Page](#sales-performance-page)  
   - [Scatter Plot: Offer Price vs. SQM Price](#scatter-plot-offer-price-vs-sqm-price)  
   - [Median Change by Region Chart](#median-change-by-region-chart)  
   - [Donut Chart on Sales Performance](#donut-chart-on-sales-performance)  
   - [Key Influencers Visual](#key-influencers-visual)  
   - [Clustered Bar: Avg Offer vs. Purchase Price](#clustered-bar-avg-offer-vs-purchase-price)  
   - [House Type Analysis](#house-type-analysis)  
7. [Publish to Power BI Service](#publish-to-power bi-service)  

---

## Project Overview

This project demonstrates how to:  
- Provision a **free Google Cloud** account and load a CSV housing dataset into **BigQuery**.  
- Use **SQL** in BigQuery for initial profiling and transformations.  
- Clean and shape data in **Power Query Editor**.  
- Define robust **DAX measures** to power interactive visuals.  
- Build a **Power BI** report with advanced charts, slicers, and Key Influencers analysis.  
- **Publish** the finalized report to the Power BI Service for sharing and collaboration.

---

## Prerequisites

- Microsoft Power BI Desktop (latest version)  
- Google Cloud Platform account (free tier)  
- Basic familiarity with SQL, Power Query M, and DAX  

---

## 1. Create Free Google Cloud Account

1. Go to the [Google Cloud Free Tier](https://cloud.google.com/free) page.  
2. Sign up and activate your \$300 free credit.  
3. Enable the **BigQuery API** in the Google Cloud Console.  

---

## 2. SQL in BigQuery for Data Understanding & Transformations

- **Load Data into BigQuery & Connect to Power BI**  
- Use the BigQuery editor to run the required queries. Transformations (e.g., parsing dates, deriving regions) can also be performed in SQL before loading into Power BI.

## 3. Understanding & Cleaning Data with Power Query Editor

- Remove erroneous or duplicate rows  
- Change data types: Date, Decimal, Text  
- Split or merge columns (e.g., address parsing)  
- Fill or replace nulls with meaningful defaults

## 4. Data Modeling & DAX Measures

- Different measures can be referred from the **metrics DAX** file

## 5. Report Development

### Sales Performance Page
- Table visual: **Total YTD Sales**, **YOY Growth**

### Donut Chart
- Sales distribution by region

### Scatter Plot: Offer Price vs. SQM Price
- **X-axis**: `sqm_price`  
- **Y-axis**: `Offer Price`  
- **Tooltips**: `region`, `house_type`, `purchase_price`

### Median Change by Region Chart
- Bar chart comparing median YoY price change for each region

### Donut Chart on Sales Performance
- Slice by region showing proportion of total sales

### Key Influencers Visual
- Identify which fields (e.g., `sqm`, `year_build`, `region`) most influence `purchase_price`

### Clustered Bar: Avg Offer vs. Purchase Price
- Compare `AVERAGE(Offer Price)` and `AVERAGE(purchase_price)` by year or region

### House Type Analysis
- Multiple visuals (bar, stacked column) breaking down metrics by `house_type`

## 7. Publish to Power BI Service

1. In Power BI Desktop: **Home** → **Publish** → select workspace  
2. Configure permissions, data refresh schedule, and dashboard tiles  
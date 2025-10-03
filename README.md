# CarSales-PowerBI

## Project Overview:
This project uses the Vehicle Sales and Market Trends Dataset to provide insights into the automotive resale market. The dataset shows the transactional and vehicle-specific information, including model, condition rating, Manheim Market Report (MMR) values, sale prices, sale dates and more. This information is valuable to those who want to view year over year % growth (YoY%) , sales trends, market values vs company sales(profits),etc. ((context and goals. speak from the pov of a data analyst.))


## Data Structure Overview:
The Vehicle sales data model is showed below. It highlights:
- The main fact table with its columns and data types
- Relationships to supporting tables
- Data was cleaned and prepared using Microsoft Excel, Python scripts, and Power Query before analysis.

<img width="810" height="517" alt="image" src="https://github.com/user-attachments/assets/49a5a1f8-bdb7-4ceb-9f9a-ca179c28375b" />


## Executive Summary:
Key Performance Indicators (KPIs) track total purchase costs and their monthly distribution through a simple line graph. A map visual identifies supplier locations, with interactive tooltips showing total orders and purchase costs per country.

Highlights:
((Month-over-Month (MoM) Purchase Cost Growth: +0.07%
MoM Orders Growth: +0.05%
During the summer, a dip in company sales caused a temporary slowdown in warehouse activity. As demand recovered, franchisees increased orders, prompting higher purchase volumes to replinish warehouse stock.))

<img width="1406" height="792" alt="image" src="https://github.com/user-attachments/assets/d608c4dc-290e-4715-8f50-4fd9fb376969" />


## Insights Deep Dive:


## Recommendations:


## Tech Stack:
Microsoft Excel CSV: Used to store the data

Python: Data cleaning used Extraction of unique tables into separate CSV files for analysis

Power BI Desktop: Main platform for data visualization and reporting/ - Dashboard creation for interactive market insights and stakeholder storytelling

Exploratory Data Analysis (EDA) with Power BI and matplotlib/seaborn.

Power Query: Data transformation and preparation

DAX (Data Analysis Expressions): Creation of KPIs and dynamic filters

Data Modeling: Establishing relationships between tables for accurate filtering


## Source: https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data


## Personal Note



-----


Executive Summary:
Key Performance Indicators (KPIs) track total purchase costs and their monthly distribution through a simple line graph. A map visual identifies supplier locations, with interactive tooltips showing total orders and purchase costs per country.

Highlights:
Month-over-Month (MoM) Purchase Cost Growth: +0.07%
MoM Orders Growth: +0.05%
During the summer, a dip in company sales caused a temporary slowdown in warehouse activity. As demand recovered, franchisees increased orders, prompting higher purchase volumes to replinish warehouse stock.

image
Recommendations:
Supplier Page:
Displays Minster insights using a slicer filter

The pie chart shows the share of total purchase cost by product

The bar chart highlights monthly pallet orders by product

The table provides detailed information for further analysis

Category Page:
Focuses on the category chilled products

KPI cards summarize purchase costs, total orders, & late/on-time deliveries

The line and bar chart tracks monthly trends using orders and purchase costs



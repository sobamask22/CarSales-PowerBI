# CarSales-PowerBI

## Project Overview:
The car sales analytics project uses the Vehicle Sales and Market Trends Dataset to provide insights within the automotive resale market. The dataset contains transactional and vehicle-specific information such as model, condition rating, Manheim Market Report(MMR) values, sale prices, sale dates and more.

These data points enable stakeholders to explore key metrics such as year-over-year (YoY) growth, sales trends, market valuations, and brand-level performance.

The objective is to utilize visualization tools and calculated measures to produce business critical insights related to revenue and sales. These visualizations support decision makers to Monitor performance across time periods, Understand geographic and transmission type revenue distribution, Identify high-margin products, Track seasonal sales patterns, and more.


## Data Structure:
The Vehicle sales data model is showed below. It highlights:
- The main fact table with its columns and data types
- Relationships to supporting tables
- Data was cleaned and prepared using Microsoft Excel, Python scripts, and Power Query before analysis.

<img width="810" height="517" alt="image" src="https://github.com/user-attachments/assets/49a5a1f8-bdb7-4ceb-9f9a-ca179c28375b" />


## Executive Summary:
### Overview:
The overview page highlights a total revenue of £2.54 billion and total sales volume of 186 thousand units. Year-over-year comparisons indicate a slight decline in performance, with revenue decreasing by 0.06% and total sales falling by 0.18% between 2013 and 2014.

The dashboard includes a comparison between the total MMR value of acquired products and their sale value, providing insight into the margin performance.

A breakdown of revenue by vehicle make identifies the top five contributors, with Ford leading at £454.13 million. Supporting visuals include a heatmap illustrating revenue intensity by state and a donut chart showing revenue distribution by transmission. Automatic transmissions generate the highest revenue at £1.05 billion.

Monthly sales data from 2010 to 2014 is visualized through a line chart, revealing seasonal fluctuations. Sales typically rise from January to February, decline sharply through April, rebound between May and June, dip again in July, and reach their lowest levels from September to November before recovering in December.

<img width="1400" height="791" alt="image" src="https://github.com/user-attachments/assets/70eb184c-e3d7-438a-8f18-7d566226b194" />

### Sales Trend:


<img width="1408" height="787" alt="image" src="https://github.com/user-attachments/assets/6dc71d28-8e42-425c-b72e-794c0785e3f2" />

### Product Performance:
bmw

### Highlights:
- Year over Year Performance: Revenue declined by 0.06%, while total sales saw a 0.18% decrease between 2013 and 2014.
- Seasonal Sales Trends: The line chart reveals a recurring dip in sales every April, followed by a spike in June and a gradual decline toward year-end.
- Top Revenue Generating makes: The line chart reveals a recurring dip in sales every April, followed by a spike in June and a gradual decline toward year-end.
- Transmission Type Breakdown: - Sales by transmission type show automatic vehicles as the most popular, accounting for 77 thousand units sold.
- MMR vs Actual Revenue: A comparative analysis highlights the difference between the Manheim Market Report (MMR) values of all vehicles and their actual sale revenue.
- Geographical Sales Distribution: A map visualization displays the states where vehicles were sold, offering insight into regional market activity.


## Tech Stack:
- Microsoft Excel CSV: Used as the storage format for importing and exporting structured datasets

- Python: Used for data cleaning and preprocessing, including the extraction of unique tables into separate CSV files for targeted analysis

- Power BI Desktop: Main platform for data visualization and reporting. Enables interactive dashboard creation to support market insights

- Power Query: Used for Data transformation, cleaning and preparation prior to modelling

- DAX (Data Analysis Expressions): Used to create calculated measures, KPIs, and dynamic filters for enhanced interactivity and analytical depth

- Data Modeling: Establishing relationships between tables for accurate filtering


## Source: https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data


## Personal Note

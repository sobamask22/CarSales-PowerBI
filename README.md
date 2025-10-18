# CarSales-PowerBI

## Project Overview:
- The car sales analytics project uses the Vehicle Sales and Market Trends Dataset to provide insights within the automotive resale market. The dataset contains transactional and vehicle-specific information such as model, condition rating, Manheim Market Report(MMR) values, sale prices, sale dates and more.

- These data points enable stakeholders to explore key metrics such as year-over-year (YoY) growth, sales trends, market valuations, and brand-level performance.

- The objective is to utilize visualization tools and calculated measures to produce business critical insights related to revenue and sales. These visualizations support decision makers to Monitor performance across time periods, Understand geographic and transmission type revenue distribution, Identify high-margin products, Track seasonal sales patterns, and more.

<br>

## Data Preperation and Modelling:
One of the main challenges I faced during this project was the inconsistency of the dataset. With over 186,000 rows, manually reviewing the data would be an extremely daunting. Issues include empty rows and missing values, excess table regions and duplicate entries in categorical columns.

My cleaning approach: To tackle these issues efficiently, I used Python in Visual Studio Code and Power Query in Power BI:

**Step 1:** Load and Inspect Data
- Imported the CSV file using its file path and displayed the top rows
  
<img width="1815" height="482" alt="image" src="https://github.com/user-attachments/assets/3f12f601-6741-4fce-a95d-3f6202cc8ad1" />

**Step 2:** Explore Unique Values
- Exported a CSV containing unique values from the target column
- This helped me quickly identify inconsistent entries and duplicates

<img width="782" height="506" alt="image" src="https://github.com/user-attachments/assets/505021aa-280c-448f-b36e-8c1f26a0fb91" />

**Step 3:** Replace Values with Python
- Used df.replace() to standardize inconsistent entries (e.g., all variations of “Ford”)
- Used df.replace() to handle null values in specific columns

<img width="1067" height="605" alt="image" src="https://github.com/user-attachments/assets/d202165c-5162-4560-88c2-d02d8cc40888" />

**Step 4:** Re-run and Validate
- Re-executed the code block to update the dataset
- Regenerated the unique values sheet to confirm replacements were successful
  
**Step 5:** Trim Excess Table Regions
- In Power BI, I used Power Query to remove unnecessary rows and columns that extended beyond the actual data
- This ensured a clean, structured dataset that didn’t interfere with visualizations or calculations

<br>

## Executive Summary:
### Overview:
- The overview page highlights a total revenue of £2.54 billion and total sales volume of 186 thousand units. Year-over-year comparisons indicate a slight decline in performance, with revenue decreasing by 0.06% and total sales falling by 0.18% between 2013 and 2014. The line chart on the Kpi Cards shows the revenue and sales change between 2013 and 2014.

- The dashboard includes a comparison between the total MMR value of acquired products and their sale value, providing insight into the margin performance.

- A breakdown of revenue by vehicle make identifies the top five contributors, with Ford leading at £454.13 million. Supporting visuals include a map illustrating sales by state and a donut chart showing revenue distribution by transmission. Automatic transmissions generate the highest revenue at £1.05 billion.

- Monthly sales data from 2010 to 2014 is visualized through a line chart, revealing seasonal fluctuations. Sales typically rise from January to February, decline sharply through April, rebound between May and June, dip again in July, and reach their lowest levels from September to November before recovering in December.

<img width="1154" height="649" alt="image" src="https://github.com/user-attachments/assets/0ef33e21-78d6-4b2d-93d4-78bbc47310c2" />

### Sales Trend:
- **Peak Revenue Year:** 2013 was the highest-performing year, recording £572.24 million in revenue, 32.8 thousand units sold, and an average sale value of £17.5k per unit. Interactive slicers allow users to filter results by state, transmission type, and vehicle color for deeper analysis.

- **Sales Trend Insight:** A visual breakdown of the top 10 car makes by revenue is presented, along with year-over-year (YoY) changes in both revenue and sales indicated by trend arrows. Notably, Mercedes and Infiniti experienced a decline in YoY sales volume but an increase in YoY revenue, suggesting that higher value or newer vehicles were sold compared to 2012.

- **Monthly Sales Analysis:** The dashboard also displays monthly revenue and sales figures for 2013, accompanied by YoY trend arrows to highlight performance shifts compared to 2012.

<img width="1152" height="651" alt="image" src="https://github.com/user-attachments/assets/ac94234e-c012-4823-b4d4-1a0541349a73" />

### Brand Performance:
- This dashboard provides a focused analysis of car brand performance, with dynamic filtering enabled via a slicer. In the current view, BMW is selected, allowing for targeted insights across multiple dimensions:

- **Vehicle Condition:** Cars with a condition rating below 20 represent just 0.2% of total BMW sales and Vehicles with an odometer reading under 40,000 miles account for 0.4%, indicating a low share of low-mileage inventory.

- **Revenue Trend:** A line chart visualizes BMW’s revenue trajectory over five years. Monthly tooltips provide specific insights, allowing users to hover and view exact revenue values per month.

- **Transmission Type Distribution:** A pie chart illustrates the breakdown of BMW sales by transmission type. Automatic at 83.4% being the dominant preference among buyers, Sedan at 12.5% and Manual being the least at 4.1%.

- **Sale Heatmap:** A heatmap pinpoints brand sales locations. The color intensity reflects sales volume meaning darker regions indicate higher concentration of transactions.
  
<img width="1145" height="644" alt="image" src="https://github.com/user-attachments/assets/7bd98617-2e7b-4070-b535-372746f77d8c" />

### Highlights:
- **Overview:** £2.54B Total Revenue across 186K units sold
    
- **Year over Year Performance:** Revenue declined by 0.06%, while total sales saw a 0.18% decrease between 2013 and 2014.
  
- **Seasonal Sales Trends:** The line chart reveals a recurring dip in sales every April, followed by a spike in June and a gradual decline toward year-end.
  
- **Transmission Type Breakdown:** Sales by transmission type show automatic vehicles as the most popular, accounting for 77 thousand units sold.
  
- **MMR vs Actual Revenue:** A comparative analysis highlights the difference between the Manheim Market Report (MMR) values of all vehicles and their actual sale revenue.
  
- **Geographical Sales Distribution:** A map visualization displays the states where vehicles were sold, offering insight into regional market activity.

<br>

## Measures Created and Used:
All calculated measures were created using Dax Formula and stored in a dedicated measures table. This design choice improves clarity, helps maintenance and supports better documentation especially in complex models.

**Total Revenue:** Calculates the SUM of revenue across all transactions. This measure reflects overall earnings and can be filtered by time periods for trend analysis.

**Total Sales:** Counts the total number of rows in the dataset, with each row representing a sale. Since there’s no order ID column therefore each row count serves as an individual sale.

**Average Cost of Orders:** Divides Total Revenue by Total Sales to calculate the average spend per sale. This is useful for checking performance across categories like car brands or specific years.

**YoY% Change:** Calculates Year over Year percentage change by comparing values across consecutive years. For example, Total Revenue 2013 against Total Revenue 2012 or Total Sales 2011 against Total Sales 2010. This helps identify growth trends or declines over time.

**Sale of Car Condition < 25:** Evaluates vehicle quality per sale by checking the Condition column for values below 25. It returns the percentage of total sales that fall into this condition bracket.

**Odometer < 40,000:** Calculates the percentage of vehicles sold with odometer readings under 40,000 miles. Useful for identifying low mileage inventory.
MMR Total: Sums the Manheim Market Report (MMR) values, which represent benchmark market prices. This measure is essential for comparing actual sale prices against market expectations.

<br>

## Why I chose Power BI:
### Seamless Integration with Excel:
Power BI integrates effortlessly with Excel, making it easy to import, transform, and visualize spreadsheets. Since both tools are part of the Microsoft ecosystem, they share familiar interfaces and functionalities which is ideal for users transitioning from Excel to more advanced analytics.

### Cost-Effective and Accessible:
I used the free Power BI Desktop version, which offers robust features for individual development. For collaboration and sharing, the Pro license is $14/month, making it accessible for teams and small businesses.

### User-Friendly:
Power BI’s drag-and-drop interface simplifies report building. It includes guided modelling, which prevents users from placing incompatible elements in the wrong areas. Reducing errors and improving usability for both beginners and advanced users.

### Data Modelling:
Power BI excels in data modelling through:
- DAX (Data Analysis Expressions) for custom calculations
- Power Query for advanced data transformation
- Support for multi-table relationships for enabling complex models

<br>

## Why Specific Visuals?
**Line Chart:** The line chart is ideal for visualizing trends across time periods. In my dashboard, it displays monthly values across multiple years, allowing users to compare performance year over year. Each line represents a different year, making it easy to spot seasonal patterns. For example, revenue and sales.

**Pie Chart:** Pie charts work best when dealing with a small number of distinct categories. I use them to show how each category contributes to a whole, making percentage comparisons intuitive. For example, transmission types
Maps: Maps are powerful for displaying location-based data without overwhelming the user with text. Instead of listing sales by region, I use map visuals to highlight activity across geographic areas. Users can apply slicers by year and hover over specific regions to see detailed metrics.

**Gauge:** The gauge visual is effective for comparing actual values against benchmarks or targets. It provides a clear, immediate sense of performance status. For example, MMR value against actual sale price.

<br>

## Tech Stack:
- **Microsoft Excel CSV:** Used as the storage format for importing and exporting structured datasets

- **Python:** Used for data cleaning and preprocessing, including the extraction of unique tables into separate CSV files for targeted analysis

- **Power BI Desktop:** Main platform for data visualization and reporting. Enables interactive dashboard creation to support market insights

- **Power Query:** Used for Data transformation, cleaning and preparation prior to modelling

- **DAX (Data Analysis Expressions):** Used to create calculated measures, KPIs, and dynamic filters for enhanced interactivity and analytical depth

- **Data Modeling:** Establishing relationships between tables for accurate filtering

<br>

## Source:
https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data

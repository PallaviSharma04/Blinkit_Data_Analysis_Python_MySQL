
<img align="left" width = "70" src="https://cdn.pnggallery.com/wp-content/uploads/blinkit-logo-01.png"/>

# Blinkit Sales Data Analysis

## Table of Contents
- [Project Overview](#project-overview)
- [Project Goals](#project-goals)
- [Dataset](#dataset)
- [Tools & Technology](#tools-and-technology)
- [Data Schema](#data-schema)
- [Entity Relationship Diagram](#entity-relationship-diagram)
- [Analytical Approach](#analytical-approach)
- [Recommendations](#business-recommendations)

## Project Overview
Blinkit is an online grocery delivery service, and this project aims to analyze its sales data to extract meaningful insights. The dataset consists of various aspects such as customer details, orders, delivery performance, and product details. The analysis involved data cleaning, exploratory data analysis(EDA) and deriving insights into customer behavior, potential improvements in delivery and sales performance and identifying trends. SQL was used for efficient querying and data extraction, while Python libraries such as Pandas, Matplotlib and Seaborn were utilized for in-depth analysis and visualization.

## Project Goals
The primary objectives of this analysis are:

- Identify the best-selling products and sales trends.
- Evaluate delivery performance and identify potential areas for improvement.
- Understand customer purchasing patterns and preferences.
- Provide business recommendations for enhancing customer experience and operational efficiency

## Dataset
- **Data Source**: Public Dataset from <a href="https://www.kaggle.com/datasets/akxiit/blinkit-sales-dataset/data?select=blinkit_delivery_performance.csv">Kaggle</a>
           - <a href="https://github.com/PallaviSharma04/Blinkit_Data_Analysis_Python_MySQL/tree/main/Data%20Files">Blinkit Sales Dataset </a>
- **Data Range** : Mar 2023 to Nov 2024

## Tools and Technology
The following tools were used for data analysis:
- **Python** (for data processing and analysis)
- **Pandas** (for data manipulation)
- **Seaborn & Matplotlib** (for data visualization)
- **SQLAlchemy** (for querying data using SQL in Python)
- **Jupyter Notebook** (for exploratory analysis)

## Data Schema
The dataset comprises six CSV files containing various details:
- **Orders**: Contains details of customer orders, including order date, total amount, and delivery status.
- **Order Items**: Lists the products included in each order along with quantity and pricing details.
- **Products**: Provides product specific information such as category, brand, price, and margin percentage.
- **Customers**: Stores customer details, including demographics, total orders, and average order value.
- **Delivery Performance**: Tracks delivery times, distances, and reasons for any delays.
- **Customer Feedback**: Captures customer ratings, reviews, and sentiment analysis.
- **Inventory**: Contains details of the inventory including date, received stocks and damaged stocks.

## Entity Relationship Diagram
![Blinkit_ER_Diagram](https://github.com/user-attachments/assets/0d5a1823-a321-49c7-8636-842665eb2046)

## Analytical Approach
The analysis was conducted through the following steps:

### 1: Data Acquisition
- Downloaded the Blinkit Sales Dataset using the Kaggle API.
- Extracted the zip file and read the extracted csv files into Pandas DataFrames.

### 2: Data Cleaning and Wrangling
- Checked for missing, duplicate and inconsistent values.
- Removed missing or duplicate entries.
- Standardized data types and formatted date/time columns.
- Added necessary columns for comprehensive analysis.

### 3: SQL Integration for Data Retrieval
- Connected Python with MySQL using SQLAlchemy.
- Loaded the cleaned Pandas DataFrames into MySQL tables for efficient storage and querying.

### 4: Exploratory Data Analysis (EDA)

#### 4.1: Sales Insights
- *The Key Performance Indicators(KPIs) for the business are sumarrized below:*

![Screenshot 2025-03-17 152910](https://github.com/user-attachments/assets/d89d9b1f-6e4a-4d33-a633-af99199c7e2b)
- *Here are the insights from the yearly sales trends:*

![Screenshot 2025-03-17 154622](https://github.com/user-attachments/assets/a87b8e50-a0a3-4b03-9886-fb4b8a39a817)
> The bar chart shows that total sales in 2024(5.54M) are slightly higher than in 2023(5.46M), suggesting an upward trend in sales performance. This could be due to increased demand, better marketing strategies, or other business improvements. The difference, though small, highlights a positive growth trajectory, which could be further analyzed by examining monthly sales patterns. 

- *Monthly Sales Trends:*
![MonthlySalesTrends](https://github.com/user-attachments/assets/91907aa9-5e77-4d35-aee2-4ec54c128c48)
> The sales trend in 2023 saw a notable rise after March, staying consistently above the 2024 trend for most of the year. In contrast, 2024 exhibited a stable pattern until October, when a sharp decline occurred, likely due to missing data. This dip helps explain why, despite 2023 having higher monthly sales, the overall yearly totals in the bar chart were nearly identical, with 2024 slightly ahead. It indicates that while 2023 had a stronger mid-year performance, 2024 experienced steady growth until the data gap occurred.

- *Now, let's examine whether the sales trends are linked to order trends by analyzing the monthly order data.*
![MonthlyOrderCountTrends](https://github.com/user-attachments/assets/8686385c-a0bc-4924-9e65-8de03d379553)
> The trends in monthly order counts align closely with those of monthly sales, reinforcing the connection that both order volume and total sales moved together throughout the period. The correlation between order count and sales trends indicates that higher revenue in 2024 was likely due to consistent demand.

- *Next, let's analyze the quarterly cumulative sales totals.*
![Running](https://github.com/user-attachments/assets/ab57a724-16a1-41b1-b912-1038882e9ca1)
> The quarterly cumulative sales trend demonstrates consistent growth across all quarters, reflecting a steady rise in overall sales over time. This trend aligns with the yearly bar chart, where 2024 shows slightly higher total sales than 2023. The monthly trends also support this, as despite occasional fluctuations, likely due to missing data, the overall upward trajectory indicates improving business performance. If all data were available, it's likely that 2024 would surpass 2023 in total sales for the year. The absence of declines or plateaus further suggests that sales have been steadily increasing each quarter.

- *Top 10 and Bottom 10 areas in terms of total sales:*
![TopBottom](https://github.com/user-attachments/assets/5d5a52b7-fb0b-40b4-ba16-93604a4c4f07)
> The graph above shows that Orai, followed by Deoghar, Nadiyal, and others, are the top-performing areas in terms of sales, while Cuttack, Gopalpur, and Vasai-Virar are among the bottom 10, showing lower sales performance.

#### 4.2: Product Insights
- *The top five best-selling products by quantity sold are pet treats, toilet cleaners, dish soaps, vitamins, and cough syrup which are predominantly sourced from the Household Care, Pharmacy, and Pet Care categories.*
- *The categories with the largest number of products are Dairy & Breakfast, Fruits & Vegetables, Household Care, and Snacks & Munchies. In contrast, Baby Care has the fewest products and sales, indicating lower consumer demand.*
- *The majority of products are priced between 500-1000, which aligns with the top-selling categories, suggesting that consumers prefer mid-range pricing.*
- *Next, let's analyze the total number of products sold per category to see if it correlates with the variety or number of products available in each category:*
![Products_Category](https://github.com/user-attachments/assets/660ce45a-940a-40f8-8a4e-cf68ef26fd4b)
> We can observe that Dairy & Breakfast, followed by Household Care, are the best-selling categories. Although these categories offer the most variety of products, the number of products does not always correlate with higher sales. For example, Fruits & Vegetables, which has the second-largest product variety, does not appear in the top four best-selling categories.

- *Yearly comparison of product category performance:*
![Products_CategorySales](https://github.com/user-attachments/assets/adf648c0-3c5e-41bb-910d-77c7f35dfde7)
> Yearly sales comparisons reveal that Dairy & Breakfast, Household Care, and Pet Care lead in revenue, while Instant & Frozen Food and Baby Care trail behind. This indicates that while Dairy & Breakfast, Household Care, and Pet Care excel in sales volume and revenue, the product variety within these categories may not be fully aligned with consumer demand.

#### 4.3: Delivery Insights


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
Blinkit is an online grocery delivery service, and this project aims to analyze its sales data to extract meaningful insights. The dataset consists of various aspects such as customer details, orders, delivery performance, and product details. By leveraging data analytics, we identify trends, customer behavior, and potential improvements in delivery and sales performance.

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

**1: Data Loading and Cleaning**
- Removed missing or duplicate entries.
- Standardized date formats for consistency.
- Added necessary columns for comprehensive analysis.

**2: Exploratory Data Analysis (EDA)**
Analyzed sales trends over time.

Identified best-selling products and customer preferences.

Evaluated customer ratings and sentiment from feedback.

Examined delivery performance metrics to identify delays and inefficiencies.

**3: SQL Queries for Insights**

Used SQL queries in Python to extract key insights such as:

Most popular products by sales volume

Average order value by customer segment

Order frequency trends over months

Delivery efficiency and delay reasons

5.4 Visualization

Sales trends were visualized using time-series plots.

Customer ratings were analyzed using bar charts.

Delivery time performance was evaluated using histograms and scatter plots.

Product popularity was shown using pie charts and treemaps.

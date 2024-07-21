# Retail Sales Analysis Project Using Python and SQL
### Introduction

This repository hosts an end-to-end data analytics project that utilizes Python and SQL to analyze a retail orders dataset. The project focuses on extracting, transforming, and loading (ETL) data, cleaning and processing it using pandas, and performing analytical queries in SQL Server to derive insights.

### Setup and Data Acquisition

#### Environment Setup
- **Tools Used**: Python libraries (`pandas`, `sqlalchemy`, `kaggle`), SQL Server (`SQLEXPRESS`), and ODBC driver (`ODBC DRIVER 17 FOR SQL SERVER`).

#### Data Acquisition
- **Kaggle Dataset**: The dataset (`retail-orders`) was downloaded using the Kaggle API as a CSV file (`orders.csv`).

### Data Processing and Cleaning

#### Loading and Initial Exploration
- **Loading Data**: The CSV file was loaded into a pandas DataFrame (`df`), handling null values marked as 'Not Available' or 'unknown'.

#### Data Transformation
- **Column Renaming**: Columns were transformed to lowercase and spaces were replaced with underscores for consistency.
- **Derived Metrics**: New columns like `profit` were calculated based on existing data (`sale_price` and `cost_price`).

#### Data Type Conversion
- **Date Conversion**: `order_date` was converted from string to datetime format for easier manipulation and analysis.

#### Dropping Irrelevant Columns
- **Column Removal**: Unnecessary columns such as `list_price`, `cost_price`, and `discount_percent` were dropped from the DataFrame.

### Loading Data into SQL Server

#### Connecting and Loading Data
- **SQLAlchemy Connection**: Established a connection to SQL Server using `sqlalchemy` and loaded the cleaned DataFrame (`df`) into a table named `df_orders`.

### SQL Queries and Analysis

#### Analytical Queries
- **Top Revenue Generating Products**: Identified the top 10 products by total sales (`sale_price`).
- **Top Selling Products by Region**: Determined the top 5 products by sales in each region using window functions.
- **Month-over-Month Sales Growth**: Compared sales growth between 2022 and 2023 for each month.
- **Highest Sales Month for Each Category**: Found the month with the highest sales for each category.
- **Highest Profit Growth by Sub-Category**: Identified the sub-category with the highest profit growth from 2022 to 2023.

### Conclusion

This repository provides a detailed walkthrough of the data analytics project, from data acquisition and cleaning to SQL analysis and insights generation. It serves as a practical example of integrating Python and SQL for data-driven decision-making in retail analytics.

---

# Retail_Order_Analysis_Project

Project Overview
This project demonstrates a comprehensive data analytics workflow, covering every stage from automated data extraction to advanced SQL-based business analysis
. The primary objective was to build a robust ETL (Extract, Transform, Load) pipeline to process a retail orders dataset and extract actionable insights for business decision-making
.

Technical Stack

- Python: Utilized for automated data extraction, cleaning, and preprocessing
.
- Libraries: pandas for data manipulation, sqlalchemy for database connection, kaggle for data retrieval via API, and zipfile for file management
.
- Database: Microsoft SQL Server for efficient data storage and advanced analytical querying
.
- Environment: Developed using Jupyter Notebook within the Anaconda Navigator environment
.

Data Workflow

1. Data Extraction

Kaggle API Integration: Automated the retrieval of the retail orders dataset directly from Kaggle using the public API and a secure JSON token
.
File Handling: Programmatically extracted the dataset from a compressed ZIP format into a CSV file for processing
.


2. Data Transformation (Cleaning in Python)

Null Value Management: Identified placeholder strings like "Not Available" and "Unknown" during data ingestion and converted them into proper null values
.
Schema Standardization: Cleaned column names by converting them to lower case and replacing spaces with underscores to ensure database compatibility
.
Feature Engineering: Developed new business metrics, including the exact discount value, the final sale price (list price minus discount), and total profit (sale price minus cost)
.
Data Typing: Converted the order_date column from an object/string format into a standardized datetime format
.
Dimensionality Reduction: Streamlined the dataset by dropping redundant columns such as cost_price, list_price, and discount_percentage once the final metrics were derived
.


3. Data Loading
   
Database Integration: Established a connection to SQL Server using the SQLAlchemy library and appropriate ODBC drivers
.
Optimized Table Schema: Manually defined a table schema with optimized data types (e.g., using INT and specific VARCHAR lengths) to ensure memory efficiency
.
Data Ingestion: Loaded the processed data into the database using the append method, preserving the integrity of the predefined schema
.

Analytical Insights (SQL)

- Product Performance: Identified the top 10 highest revenue-generating products in the dataset
.
- Regional Trends: Determined the top 5 highest-selling products within each specific geographical region
.
- Year-over-Year Growth: Conducted a month-over-month sales comparison between 2022 and 2023
.
- Category Peaks: Pinpointed the specific months that recorded the highest sales for every individual product category
.
- Growth Drivers: Established that the Supplies subcategory saw the highest growth by percentage (80%), while Machines achieved the highest absolute profit growth of $35,000 when comparing 2023 to 2022.


## Project Report: Sales Data Processing, Transformation, and Analysis of Global electronics dataset

### Project Objective
The goal of this project is to process, transform, and analyze sales, customer, product, and store data for Global Electronics. The final deliverable is a structured MySQL database, with additional insights generated through SQL queries and a power Bi dashboard.

---

### Steps Overview

#### 1. Data Import and Initial Setup

- Imported datasets from CSV files:
  - `Customers.csv`
  - `Sales.csv`
  - `Products.csv`
  - `Stores.csv`
  
- Used Python’s `pandas` library for initial data loading and processing.

---

#### 2. Data Merging

- Merged datasets to create a unified DataFrame (`merged_df`) with relevant information.
- Performed **left joins** on common keys like `CustomerKey`, `ProductKey`and`StoreKey`.

---

#### 3. Handling Missing and Duplicate Data

- **Missing Data**: Filled in missing `State Code` values for `Napoli` and assessed other missing fields.
- **Duplicate Data**: Identified and removed duplicate records to ensure data integrity.

---

#### 4. Data Cleaning and Transformation

- Renamed columns for consistency.
- Converted cost-related columns to numerical formats to enable financial calculations.
- Derived key metrics:
  - `Gross Profit`
---

#### 5. Outlier Detection

- Calculated z-scores for numerical columns to identify potential outliers.
- Marked outliers based on a z-score threshold of 3.

---

#### 6. Column Removal and Final Transformations

- Removed irrelevant columns to streamline the dataset.
- Converted `Order Date` and `Birthday` columns to datetime formats.
- Calculated `customer_age` based on the difference between `Order Date` and `Birthday`.

---

#### 7. Database Setup and Data Insertion

- Created a MySQL database (`project2`) and inserted the cleaned data into a structured table.
- Modified column names to SQL-friendly formats.
- Managed missing values before insertion.

---

#### 8. Data Export and Analytical Queries

- Exported the final dataset to a CSV file for further analysis.
- Executed SQL queries on the MySQL database to generate various reports, such as:
  - **Total Gross Profit by Country**: Identifies countries with the highest profitability.
  - **Average Customer Age by Country**: Provides age insights to understand customer demographics.
  - **Product Quantity Sold by Type**: Highlights popular product subcategories.
  - **Top Revenue-Generating Brands**: Ranks brands by total revenue.
  - **Orders by Gender and Country**: Shows order distribution across gender and location.
  - **Gross Profit by Store Type**: Compares profitability between online and physical stores.
  - **Monthly Sales Analysis**: Evaluates seasonal trends in gross profit.
  - **Top Products by Age Group**: Reveals product preferences across age groups.

---

### Conclusion
The project successfully imported, merged, cleaned, and transformed sales-related data, making it ready for in-depth analysis and insights extraction in MySQL. The analytical reports generated provide valuable insights into profitability by country, customer age distribution, top products, and store performance, enabling data-driven decisions for the company.













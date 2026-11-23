
# 📊 Sales Data Transformation and Data Modeling using Power BI

A Power BI project focused on importing, cleaning, transforming, merging, grouping, and modeling sales datasets using Power Query Editor and Power BI Desktop.

## 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Data Sources & Architecture](#-data-sources--architecture)
- [Data Transformation ETL](#-data-transformation-etl)
- [Data Model](#-data-model)
- [Grouping and Aggregation](#-grouping-and-aggregation)
- [Project Outcomes](#-project-outcomes)
- [Repository Contents](#-repository-contents)
- [How to Use](#-how-to-use)
- [Tools and Technologies](#-tools-and-technologies)

---

## 🎯 Project Overview

- **Project Name:** Power BI Assignment 1 – Data Transformation and Data Modeling
- **Business Problem:** Raw sales and order datasets need to be cleaned, organized, and structured for meaningful data analysis.
- **Objective:** To perform data import, transformation, data cleaning, merging, grouping, aggregation, and relationship creation using Microsoft Power BI.
- **Target Audience:** Data Analysts, Business Intelligence Professionals, and Sales Teams.
- **Project Type:** Data Transformation and Data Modeling.

## 🗃️ Data Sources & Architecture

Three CSV datasets were used in this project:

| Dataset | Description |
|---|---|
| List of Orders.csv | Contains customer, order date, city, state, and order information. |
| Order Details.csv | Contains order IDs, product categories, sub-categories, quantity, amount, and profit. |
| Sales Target.csv | Contains monthly sales targets and corresponding dates. |

- **Source Format:** CSV files
- **Data Import Tool:** Power BI Desktop
- **Data Preparation Tool:** Power Query Editor
- **Storage Mode:** Import Mode

## ⚙️ Data Transformation (ETL)

All required data transformations were performed using Power Query Editor.

### 1. Data Import
- Imported List of Orders.csv.
- Imported Order Details.csv.
- Imported Sales Target.csv.

### 2. Row Limiting and Data Types
- Restricted List of Orders to the first 500 rows.
- Changed Order Date to Date data type.
- Changed Amount and Target to Fixed Decimal Number.

### 3. Text Formatting
- Applied Capitalize Each Word formatting to the CustomerName column.

### 4. Custom Column Creation
- Merged City and State columns to create a new Location column.
- Created Profit Margin using Profit divided by Amount.
- Changed Profit Margin to Percentage data type.

**Profit Margin Formula:**

```powerquery
[Profit] / [Amount]
```

### 5. Conditional Column Creation

Created a Profit Status column to classify profit values into three categories:

- Loss
- Break-Even
- Profit

**Conditional Logic:**

```powerquery
if [Profit] < 0 then "Loss"
else if [Profit] = 0 then "Break-Even"
else "Profit"
```

### 6. Data Merging

- Merged List of Orders and Order Details using Order ID.
- Selected Left Outer Join.
- Expanded the required columns from Order Details.
- Created a new table named Orders Data.

### 7. Handling Missing Values and Duplicates

- Used Column Quality to inspect data quality.
- Checked Valid, Error, and Empty values.
- Checked for completely duplicated rows across all columns.
- No completely duplicated rows were identified in the checked tables.
- No missing values or errors were identified in the checked tables.

### 8. Sorting and Filtering

- Sorted Order Date in descending order.
- Applied a Location filter to analyse orders from Tamil Nadu.

## 🧠 Data Model

Relationships were established between the original tables using common columns.

### Relationship 1: List of Orders and Order Details

- **First Table:** List of Orders
- **Second Table:** Order Details
- **Relationship Column:** Order ID

### Relationship 2: Order Details and Sales Target

- **First Table:** Order Details
- **Second Table:** Sales Target
- **Relationship Column:** Category

Both relationships were checked using Manage Relationships to verify that they were active and correctly defined.

## 📊 Grouping and Aggregation

Four separate summary tables were created using the Group By operation.

### 1. Count of Order ID
- Grouped by Order ID.
- Used Count Rows to calculate the number of records for each order.

### 2. Average Profit by Category
- Grouped by Category.
- Calculated the average Profit for each category.

### 3. Total Amount by Sub-Category
- Grouped by Sub-Category.
- Calculated the sum of Amount for each sub-category.

### 4. Total Target by Month
- Grouped by Month of Order Date.
- Calculated the sum of Target for each month.

## 💡 Project Outcomes

- Successfully imported three CSV datasets into Power BI.
- Performed data cleaning and transformation using Power Query.
- Created custom and conditional columns.
- Merged order information using a Left Outer Join.
- Checked data quality and duplicate records.
- Created four grouped summary tables.
- Established and verified two data relationships.
- Prepared structured datasets for further analysis.

## 📁 Repository Contents

The GitHub repository contains the following files:

| File Name | Description |
|---|---|
| List of Orders.csv | Original order dataset |
| Order Details.csv | Original order details dataset |
| Sales Target.csv | Original sales target dataset |
| Power BI Assignment 1.pbix | Completed Power BI project file |
| Power_BI_Assignment_1_Screenshots.pdf | Assignment documentation with screenshots |
| README.md | Project description and documentation |

## 🚀 How to Use

1. Install Microsoft Power BI Desktop.
2. Clone or download this GitHub repository.
3. Download the three CSV datasets.
4. Open the Power BI Assignment 1.pbix file in Power BI Desktop.
5. If required, update the data source paths through Data Source Settings.
6. Refresh the data if necessary.
7. Explore the transformed tables, aggregation results, and data model.

## 🛠️ Tools and Technologies

- Microsoft Power BI Desktop
- Power Query Editor
- CSV Datasets
- GitHub
- Microsoft Word / Google Docs

---

**Project Category:** Data Analytics | Data Transformation | Data Modeling

**Project Tool:** Microsoft Power BI Desktop


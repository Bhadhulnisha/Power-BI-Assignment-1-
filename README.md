
# 📊 Project Title: Sales Data Transformation and Data Modeling using Power BI

A Power BI project focused on transforming, cleaning, merging, grouping, and modeling sales datasets to prepare structured data for business analysis.

## 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Data Sources & Architecture](#-data-sources--architecture)
- [Data Transformation ETL](#-data-transformation-etl)
- [Data Model](#-data-model)
- [Grouping and Aggregation](#-grouping-and-aggregation)
- [Project Outcomes](#-project-outcomes)
- [How To Use](#-how-to-use)

---

## 🎯 Project Overview

- **Business Problem:** Raw sales and order datasets need to be organized and transformed before they can be used for meaningful analysis.
- **Objective:** Perform data cleaning, transformation, merging, grouping, aggregation, and data modeling using Microsoft Power BI.
- **Target Audience:** Data Analysts, Sales Teams, and Business Intelligence Professionals.
- **Project Type:** Data Transformation and Data Modeling.

## 🗃️ Data Sources & Architecture

Three CSV datasets were used in this project:

| Dataset | Description |
|---|---|
| List of Orders.csv | Contains customer and order information. |
| Order Details.csv | Contains product, category, amount, and profit information. |
| Sales Target.csv | Contains sales targets and corresponding dates. |

- **Source Format:** CSV files.
- **Tool Used:** Microsoft Power BI Desktop.
- **Data Import Mode:** Import Mode.
- **Data Preparation:** Power Query Editor.

## ⚙️ Data Transformation (ETL)

**Tool Used:** Power Query Editor.

The following data transformation operations were performed:

### 1. Data Import
- Imported List of Orders.csv.
- Imported Order Details.csv.
- Imported Sales Target.csv.

### 2. Row Limiting and Data Types
- Restricted List of Orders to the first 500 rows.
- Changed Order Date to Date data type.
- Changed Amount and Target to Fixed Decimal Number.

### 3. Text Formatting
- Applied Capitalize Each Word formatting to CustomerName.

### 4. Custom Column Creation
- Merged City and State columns to create Location.
- Created Profit Margin using Profit divided by Amount.
- Changed Profit Margin to Percentage data type.

**Custom Column Formula:**

```powerquery
[Profit] / [Amount]
```

### 5. Conditional Column
Created a Profit Status column to classify records into:

- Loss
- Break-Even
- Profit

### 6. Data Merging
- Merged List of Orders and Order Details using Order ID.
- Selected Left Outer Join.
- Expanded the required columns from Order Details.
- Created a new table named Orders Data.

### 7. Handling Missing Values and Duplicates
- Used Column Quality to check data quality.
- Checked Valid, Error, and Empty values.
- Performed duplicate checking across all columns.
- No completely duplicated rows were identified.

### 8. Sorting and Filtering
- Sorted Order Date in descending order.
- Applied a Location filter to analyse Tamil Nadu orders.

## 🧠 Data Model

The project uses relationships between the original tables.

### Relationships Established

**Relationship 1:**
- Table 1: List of Orders
- Table 2: Order Details
- Common Column: Order ID

**Relationship 2:**
- Table 1: Order Details
- Table 2: Sales Target
- Common Column: Category

Both relationships were checked using Manage Relationships to ensure they were active.

## 📊 Grouping and Aggregation

Four summary tables were created using Group By operations.

### 1. Count of Order ID
- Grouped by Order ID.
- Used Count Rows to calculate the number of records for each order.

### 2. Average Profit by Category
- Grouped by Category.
- Calculated the average Profit for each category.

### 3. Total Amount by Sub-Category
- Grouped by Sub-Category.
- Calculated the sum of Amount.

### 4. Total Target by Month
- Grouped by Month of Order Date.
- Calculated the sum of Target.

## 💡 Project Outcomes

- Successfully imported and transformed three CSV datasets.
- Created custom and conditional columns.
- Merged order information into a consolidated Orders Data table.
- Performed data quality and duplicate checks.
- Created four grouped summary tables.
- Established and verified two data relationships.
- Prepared structured datasets for further analysis.

## 🚀 How To Use

1. Install Microsoft Power BI Desktop.
2. Download or clone this GitHub repository.
3. Download the three original CSV datasets.
4. Open the `.pbix` project file in Power BI Desktop.
5. If necessary, update the data source paths through Data Source Settings.
6. Refresh the data if required.
7. Explore the transformed tables, grouped summaries, and data model.

## 📁 Repository Contents

- `List of Orders.csv` – Original order dataset.
- `Order Details.csv` – Original order details dataset.
- `Sales Target.csv` – Original sales target dataset.
- `Power BI Assignment 1.pbix` – Completed Power BI project.
- `Power_BI_Assignment_1_Screenshots.pdf` – Assignment screenshots and documentation.
- `README.md` – Project documentation.

---

## 🛠️ Tools & Technologies

- Microsoft Power BI Desktop
- Power Query Editor
- Microsoft Word / Google Docs
- GitHub
- CSV Datasets

---

**Project Category:** Data Analytics | Data Transformation | Data Modeling

**Project Tool:** Microsoft Power BI Desktop

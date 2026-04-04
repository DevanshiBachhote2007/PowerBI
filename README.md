# Data Leverager – Power Query Transformation Project
🔹 Project Overview
This project simulates a data engineering workflow in Power BI using Power Query. The focus is on data extraction, cleaning, transformation, and integration — no DAX or visualization required.

## 🛠 Step-by-Step Guide
### 01 Load Data Sources
Start Here
Bring in all required datasets into Power Query.

Load an HTML table from the web (e.g., GDP or COVID stats)

Load Sales_Jan.xlsx, Sales_Feb.xlsx, Sales_Mar.xlsx using Append Queries from Folder

Load an Employee dataset with EmployeeID, Name, Department, Region, Join Date

### 02 Apply Basic Transformations

Clean and standardize the raw data for consistency.

Remove blank rows and columns

Promote first row to headers

Rename columns with meaningful names

Change data types (use Change Type with Locale for dates/currency)

Remove duplicates and filter null values

### 03 Use Text Tools

Clean and format text fields like names and addresses.

Apply UPPER(), LOWER(), TRIM(), CLEAN()

Use REPLACE() for corrections

Split columns by delimiter (e.g., First Name / Last Name)

### 04 Apply Numeric Tools

Perform calculations and create new numeric fields.

Round off revenue columns to 2 decimals

Create new column: Profit = Revenue – Cost

### 05 Work with Date & Time

Extract and enrich date-related information.

Extract Day, Month, Year, Quarter from Order Date

Create custom Fiscal Month column

Add Age column from Birthdate

### 06 Conditional Columns & Indexing

Categorize and uniquely identify records.

Create Sales Category (High, Medium, Low)

Add Index columns (0-based and 1-based)

### 07 Pivoting & Unpivoting

Reshape data for analysis flexibility.

Pivot monthly sales into a single column

Unpivot back into normalized form

### 08 Merging & Appending

Combine multiple datasets into one unified model.

Merge Sales Data with Employee Data using Region or EmployeeID

Append Jan–Mar sales data using Append Queries as New

### 09 Grouping & Aggregation

Summarize data for insights.

Group by Region

Compute Total Sales, Average Order Value, Transaction Count

### 10 Data Profiling & Quality Checks

Validate and ensure data integrity.

Use Column Profile, Distribution, and Quality tools

Identify missing values and errors

Check distinct and unique values

### 11 Refresh Simulation

Final Step
Test dynamic updates and prepare submission.

Add Sales_Apr.xlsx to folder and refresh

Verify transformations auto-apply

Export Power BI .pbix file

Write summary document (sources, transformations, challenges)

### ✅ 12 Submission Requirements
Deliver the Power BI .pbix file with all transformations applied.

# 📊Presentation of Project

<img width="1536" height="1024" alt="Copilot_20260404_111047" src="https://github.com/user-attachments/assets/f1f7d9be-9051-48c1-a440-776f6894cf0c" />



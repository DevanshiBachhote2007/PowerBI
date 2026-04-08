# Data Modeler – Normalized Star Schema in Power BI
## 📌 Project Overview
This project demonstrates the construction of a relational data model in Power BI using multiple normalized tables. The goal is to design a Star Schema (with optional Snowflake extension) and showcase understanding of:

Table relationships

Cardinality (1:Many, Many:1, 1:1)

Handling inactive/ambiguous paths

Schema design best practices

📂 Dataset Files
The project uses the following Excel files as source tables:

Customer_Dim.xlsx – CustomerID (PK), Name, Segment

Product_Dim.xlsx – ProductID (PK), Category, Subcategory, ProductName

Sales_Fact.xlsx – SalesID (PK), CustomerID (FK), ProductID (FK), RegionID (FK), DateKey (FK), Revenue

Region_Dim.xlsx – RegionID (PK), Country, State, City

Date_Dim.xlsx – DateKey (PK), Date, Month, Quarter, Year, Fiscal Year

Returns_Fact.xlsx – ReturnID (PK), SalesID (FK), ReturnDateKey (FK), Reason

🛠 Project Tasks
Model Construction & Relationships

Import all files via Power Query, clean data (remove blanks, set data types).

Define Primary Keys and Foreign Keys manually.

Create relationships:

Sales_Fact → Customer_Dim

Sales_Fact → Product_Dim

Sales_Fact → Region_Dim

Sales_Fact → Date_Dim

Returns_Fact → Sales_Fact

Returns_Fact → Date_Dim (inactive relationship for ReturnDateKey)

Schema Design

Build a Star Schema with Sales_Fact as the central fact table.

Model Returns_Fact either as a Snowflake extension or as a second Fact Table.

Demonstrate cardinalities and relationship directions.

Advanced Model Settings

Set appropriate relationship cardinalities and cross-filter directions.

Enable/disable bidirectional filters only when justified.

Simulate inactive relationships using Returns_Fact.

Resolve filter ambiguity issues.

Data Model Enhancements

Apply proper data formats (currency, whole numbers, dates).

Define Data Categories (City, Country, ProductName).

Build hierarchies:

Date_Dim: Year > Quarter > Month > Date

Region_Dim: Country > State > City

Product_Dim: Category > Subcategory > ProductName

Verification

Use a Matrix Table (only allowed visual) to verify:

Sales grouped by Product Category and Region

Return reasons by Fiscal Year

Revenue by Customer Segment

📑 Deliverables
Power BI File (.pbix) containing:

Transformed tables via Power Query

Relationships and schema structure

Hierarchies and cleaned fields

Matrix table for verification

Summary Document (.docx or .txt) explaining:

Schema type (Star/Snowflake)

Relationship rationale and filter flow

Issues encountered and resolutions

🚀 How to Run
Clone this repository.

Open Power BI Desktop.

Import the provided Excel files via Power Query.

Follow the schema design steps to replicate the model.

Verify outputs using the Matrix Table visual.

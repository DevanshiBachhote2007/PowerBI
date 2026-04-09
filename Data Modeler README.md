# 📊 Power BI Data Modeling Project

## 🚀 Project Goal
This project shows how to build a **Star Schema Data Model** in Power BI using Excel files.  
The aim is to connect fact tables and dimension tables correctly, clean the data, and verify results with a matrix visual.

---

## 📂 Files Used
- **Customer_Dim.xlsx** → Customer details  
- **Product_Dim.xlsx** → Product details  
- **Region_Dim.xlsx** → Country, State, City  
- **Date_Dim.xlsx** → Calendar and fiscal dates  
- **Sales_Fact.xlsx** → Sales transactions (main fact table)  
- **Returns_Fact.xlsx** → Returns linked to sales  

---

## 📝 Step-by-Step Process

### 1. Import Data
- Open Power BI Desktop.  
- Use **Power Query** to load all Excel files.  
- Clean the data: remove blank rows, set correct data types (numbers, dates, text).

### 2. Define Keys
- Identify **Primary Keys (PK)** in dimension tables (e.g., CustomerID, ProductID).  
- Identify **Foreign Keys (FK)** in fact tables (e.g., CustomerID in Sales_Fact).

### 3. Create Relationships
- Connect tables as follows:  
  - Sales_Fact → Customer_Dim  
  - Sales_Fact → Product_Dim  
  - Sales_Fact → Region_Dim  
  - Sales_Fact → Date_Dim  
  - Returns_Fact → Sales_Fact  
  - Returns_Fact → Date_Dim (inactive relationship for ReturnDateKey)
 
  - <img width="1113" height="689" alt="image" src="https://github.com/user-attachments/assets/0240be02-0edb-4a5b-aaa8-b9450b412adf" />


### 4. Build Schema
- Use **Sales_Fact** as the central hub.  
- Dimensions (Customer, Product, Region, Date) connect around it → this is the **Star Schema**.
- <img width="699" height="587" alt="image" src="https://github.com/user-attachments/assets/230bad71-9cae-4040-beb1-bb2491c19e7b" />
  
- Returns_Fact can be modeled as a second fact table or a snowflake extension.
- <img width="742" height="713" alt="image" src="https://github.com/user-attachments/assets/7f03bbc8-4816-466b-9f45-795b33717e3d" />


### 5. Advanced Settings
- Set relationship cardinalities (1:Many, Many:1).  
- Use **single filter direction** unless bidirectional is needed.  

### 6. Enhance Model
- Format data fields (currency, whole numbers, dates).
- <img width="702" height="484" alt="image" src="https://github.com/user-attachments/assets/208d1f98-7567-434d-8b94-01e5e1328b8b" />
 
- Define **Data Categories** (City, Country, ProductName).
- <img width="688" height="373" alt="image" src="https://github.com/user-attachments/assets/92284e37-7d87-44fb-9cdb-7e0dd330fc3a" />

- Create hierarchies:  
  - Date: Year → Quarter → Month → Date  
  - Region: Country → State → City  
  - Product: Category → Subcategory → ProductName
  - <img width="337" height="242" alt="image" src="https://github.com/user-attachments/assets/2e7b1ac0-28ba-419e-a40b-9c4096008acf" />
 

### 7. Verify with Matrix Visual
- Create a **Matrix Table** to check:  
  - Sales by Product Category and Region  
  - Return reasons by Fiscal Year  
  - Revenue by Customer Segment
  - <img width="462" height="482" alt="image" src="https://github.com/user-attachments/assets/c15041c4-4f17-4bca-b6e3-ace3ec2af74a" />


---
## 📝 Project Summary

### 📌 Schema Type
The project uses a **Star Schema** with **Sales_Fact** as the central fact table.  
Dimension tables (Customer, Product, Region, Date) connect directly to Sales_Fact.  
The **Returns_Fact** table is modeled separately, either as a second fact table or a snowflake extension, to handle return transactions.

---

### 🔗 Relationship Rationale & Filter Flow
- **Sales_Fact → Customer_Dim** (1:Many)  
- **Sales_Fact → Product_Dim** (1:Many)  
- **Sales_Fact → Region_Dim** (1:Many)  
- **Sales_Fact → Date_Dim** (1:Many)  
- **Returns_Fact → Sales_Fact** (Many:1)  
- **Returns_Fact → Date_Dim** (inactive relationship for ReturnDateKey)  

Filter flow is set to **single direction** wherever possible to avoid ambiguity.  
Inactive relationships are activated using DAX when needed.

---

### ⚙️ Issues & Resolutions
- **Filter Ambiguity** → Resolved by adjusting cross-filter directions.  
- **Inactive Relationships** → Managed using DAX functions for controlled activation.  
- **Data Formatting** → Fixed by applying correct data types (currency, whole numbers, dates).  
- **Hierarchy Sorting** → Built hierarchies (Date, Region, Product) for better drill-down analysis.  

---

### ✅ Verification
A **Matrix Table** was used to confirm:  
- Sales grouped by Product Category and Region  
- Return reasons by Fiscal Year  
- Revenue by Customer Segment  

---



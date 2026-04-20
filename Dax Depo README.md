# 📊 Power BI Project: DAX Depo

## 📌 Project Overview
This project, titled **DAX Depo**, evaluates advanced analytical calculations using **DAX (Data Analysis Expressions)** in Power BI.  
The focus is on backend modeling and analytical computation without relying on external visuals, except for **Matrix tables**.

---

## 📁 Dataset Tables
The following tables are provided and must be used:
- **Sales_Fact**
- **Returns_Fact**
- **Customer_Dim**
- **Product_Dim**
- **Date_Dim**
- **Region_Dim**

---

## 🧠 Project Goals
- Build calculated insights using DAX.  
- Perform advanced analytical calculations on the Sales and Returns model.  
- Display results only in **Matrix visuals**.  
- Demonstrate backend DAX modeling skills rather than visualization design.  

---

## ✅ Tasks to Perform

### 1. Calculated Columns
- Profit = `SalesAmount - Cost`  
- ReturnFlag = Returned / Not Returned  
- Customer Full Name = FirstName + LastName

- Eg.<img width="838" height="746" alt="image" src="https://github.com/user-attachments/assets/76d12103-7496-4f90-a593-ade8efeddfb4" />


### 2. Measures
- Total Sales  
- Total Cost  
- Total Profit  
- Return Rate (% of items returned)  
- Average Sale per Transaction
- <img width="783" height="471" alt="image" src="https://github.com/user-attachments/assets/81d33f1e-a9c3-49b3-afba-d5ecc274a8e4" />


### 3. Quick Measures
- Year‑Over‑Year Sales Growth  
- Difference between Current and Previous Month Sales
- <img width="582" height="252" alt="image" src="https://github.com/user-attachments/assets/50dafb16-4b72-4717-90ec-fb1ec3ee99b4" />
  

### 4. Measure Management
- Create a **Dedicated Measure Table** to organize all DAX measures.
- Eg:-<img width="364" height="664" alt="image" src="https://github.com/user-attachments/assets/30147f1a-07c5-4f34-ad14-c25cb496963d" />


### 5. Filter Context & Behavior
- Use Matrix to compare Sales by Region with and without filters using:  
  - `ALL()`  
  - `FILTER()`  
  - `CALCULATE()`
<img width="923" height="155" alt="image" src="https://github.com/user-attachments/assets/eb5b3290-6736-4e31-9f33-68a3532c7ab1" />



### 6. DAX Operators and Functions
- Math/statistical: `SUM`, `AVERAGE`, `MAX`  
- Iterators: `COUNTX`, `DISTINCTCOUNT`
- <img width="979" height="591" alt="image" src="https://github.com/user-attachments/assets/eddf24a8-6de6-4ca3-8232-0acf05275819" />

- Conditional: `IF`, `AND`, `OR`, `SWITCH`
- 
- IF:-<img width="765" height="121" alt="image" src="https://github.com/user-attachments/assets/9dd28879-8e3c-47bb-8ff5-0a8e6130317f" />

And:-<img width="1318" height="126" alt="image" src="https://github.com/user-attachments/assets/51fcaf84-71d2-4a94-8ca7-2797a4442bb3" />

Or:-<img width="754" height="240" alt="image" src="https://github.com/user-attachments/assets/4b03018c-7528-458e-99b6-68ef48a8018b" />

Switch:-<img width="959" height="198" alt="image" src="https://github.com/user-attachments/assets/9f907ba6-75f1-41ac-8e04-f7dce0d53fed" />


- Text: `CONCATENATE`, `UPPER`, `LEFT`  <img width="797" height="770" alt="image" src="https://github.com/user-attachments/assets/5a7c414e-03ff-4495-9c4c-e07e91ccaa07" />

- Date: `YEAR`, `MONTH`, `EOMONTH`  <img width="935" height="491" alt="image" src="https://github.com/user-attachments/assets/05a6489a-f817-4cc9-a53a-428d4e5677c1" />


### 7. Joining and Relationships
- Use `RELATED()` to pull related data from dimension tables.
- <img width="1055" height="558" alt="image" src="https://github.com/user-attachments/assets/190f1007-4e02-4a67-85a7-7dee000358ad" />


### 8. Time Intelligence (Matrix-based Analysis)
- Use `TOTALYTD()`, `SAMEPERIODLASTYEAR()`, `DATESINPERIOD()`
- <img width="656" height="641" alt="image" src="https://github.com/user-attachments/assets/a5996f95-8087-451a-99f2-dd67aabe21af" />

- Create running totals with `CALCULATE()` + `DATESBETWEEN()`  

### 9. Additional Scenarios
- Categorize sales ranges (Low, Medium, High) using `SWITCH()`
- <img width="1335" height="691" alt="image" src="https://github.com/user-attachments/assets/43130277-ebbe-419b-90b3-3806af9800b5" />

- Use iterators (`SUMX`, `AVERAGEX`) for aggregated metrics
- <img width="230" height="115" alt="image" src="https://github.com/user-attachments/assets/09c75235-4f37-4d47-a3a7-6da41d327f64" />
 

---

## 🔹 Output Requirement
- **Matrix visual only**  
- Grouping dimensions: Region, Month, Product Category, Customer Segment  
- Display all calculated results (columns + measures + time intelligence + categorization)  
- No other visuals allowed
- <img width="1048" height="414" alt="image" src="https://github.com/user-attachments/assets/61a6a97c-6952-4589-9fb4-077b43626c51" />


---

## 📌 Summary
This project tests your ability to:
- Build a robust backend DAX model  
- Apply advanced DAX functions for calculations  
- Organize measures professionally  
- Present all results in a single **Matrix visual** grouped by key dimensions  

---

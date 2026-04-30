# Final Project – Sales & Customer Intelligence Dashboard

## 📌 Overview
This Power BI project delivers insights into **Sales, Returns, Customer Behavior, and Regional Performance** across the last three years.  
It combines **data modeling best practices**, **advanced DAX calculations**, and **interactive dashboards** optimized for both desktop and mobile layouts.

---

## 📂 Dataset Structure
The project uses Excel files with the following tables:

- **Date_Dim**  
- **Customer_Dim**  
- **Product_Dim**  
- **Region_Dim**  
- **Sales_Fact**  
- **Returns_Fact**

Question Link:-
https://docs.google.com/document/d/1_X3f4ejaIH3MIagLGqpYsdKUmJ1kY6jB_yXx-fO1mIY/edit?tab=t.0

Dataset Link:-
https://docs.google.com/spreadsheets/d/1V7-BR_-O7KRYRv2vfNNqeHE617Pn6_SXJorrSeq9wFw/edit?usp=sharing

---

## 🛠️ Step 1: Data Modeling
- Build a **Star Schema** by connecting Fact tables to Dimension tables using **Primary & Foreign Keys**.  
- Hide unnecessary fields from the report view.  
- Apply consistent naming conventions.  

👉 *Screenshot :-*
<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/aaac79a6-8621-4ad9-8637-67574fa8953d" />


---

## 🧮 Step 2: DAX Measures & Calculated Columns
Create measures using:
- `CALCULATE`, `FILTER`, `ALL`, `SUMX`, `COUNTX`, `AVERAGEX`
- `SWITCH` for KPI classification
- `RELATED` for joining values

Calculated columns:
- Profit margin classification  
- Customer full names (`FirstName + LastName`)  
- Year-Month formatting  

👉 *Screenshot :-*
<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/e83d2386-cbed-4a5f-8132-d78700cb00e9" />


---

## 📈 Step 3: Time Intelligence
- Implement **YOY (Year over Year)**, **MOM (Month over Month)**, and **YTD (Year to Date)** calculations.  
- Identify seasonal trends using line charts.  

👉 *Screenshot:-*
<img width="1919" height="1016" alt="image" src="https://github.com/user-attachments/assets/ffd12b33-e680-4451-a3b2-728e30f649fa" />


---

## 🎨 Step 4: Dashboard Layout
- **Pages**: 1 Main, 2 Detail Pages, 1 Drillthrough Page  
- Visuals: Cards, KPI Cards, Line Charts, Bar Charts, Donut Charts  
- Add **Trend lines & Forecasts** for sales 
👉 *Screenshot*
<img width="1918" height="1016" alt="image" src="https://github.com/user-attachments/assets/978f56e6-0315-4847-86a0-67c86ac4602f" />

- Use **Matrix visuals** with conditional formatting  
- Display **Top N Products by Sales** and **Top N Customers by Profit**
👉 *Screenshot :-*
<img width="1466" height="995" alt="image" src="https://github.com/user-attachments/assets/f19f466b-ff04-425f-9afa-7793bc1ba0c6" />




---

## 🔍 Step 5: Filtering & Interaction
- Add slicers for **Product, Customer Segment, Region, and Date**  
- Enable **Drill Up/Down** and **Drillthrough filters**  
- Implement **Numeric Range Parameters** for custom filtering  

👉 *Screenshot:-*
<img width="1316" height="734" alt="image" src="https://github.com/user-attachments/assets/f823cd79-27e0-453f-a8e5-0f1a166b192c" />


---

## 🧭 Step 6: Navigation & UX
- Add **Custom Buttons & Bookmarks** for page navigation  
- Build a **Collapsible Slicer Panel**  
- Enable **Tooltips** with mini visual summaries  
- Use **Advanced Conditional Formatting** in Matrix/Table views  

👉 *Screenshot :-*
<img width="1387" height="741" alt="image" src="https://github.com/user-attachments/assets/10c818d0-d693-4d98-bd96-ce1847a65e41" />


---

## 📱 Step 7: Mobile Layout
- Optimize key pages for mobile viewing  (Optional)
- Prioritize KPI Cards and Top N visuals  

👉 *Screenshot :-*
<img width="1401" height="745" alt="image" src="https://github.com/user-attachments/assets/6fa59567-39b1-414a-9b6d-88daeed3c325" />


---

## 🔒 Step 8: Security
- Add roles for **Region Managers**  
- Simulate **Row-Level Security (RLS)** for viewing regional data  

👉 *Screenshot :-*
<img width="432" height="306" alt="image" src="https://github.com/user-attachments/assets/49229f40-67e7-47d8-9795-6cabc47a1374" />



---

## ✅ Key Learnings
- Building a clean **Star Schema** ensures scalability.  
- Advanced **DAX patterns** drive meaningful KPIs.  
- **Time Intelligence** highlights growth and seasonality.  
- **Navigation & UX** elevate user experience.  
- **Mobile optimization** ensures accessibility.  
- **Row-Level Security** enables controlled access.



---

## 📊Project Preview

### Page 1:-
<img width="1411" height="724" alt="image" src="https://github.com/user-attachments/assets/4da1dd12-58d1-4d7f-b455-da417d9189b3" />

### Page 2:-
<img width="1407" height="740" alt="image" src="https://github.com/user-attachments/assets/50dc4270-7390-45ff-afc4-57ccb2e613f0" />

### Page 3:-
<img width="1408" height="737" alt="image" src="https://github.com/user-attachments/assets/ce1ac1dd-260f-46db-a6d2-1dbe920b32e8" />

### Page 4:-
<img width="1408" height="742" alt="image" src="https://github.com/user-attachments/assets/20fec906-8073-4e52-8451-2bd915405c04" />



---



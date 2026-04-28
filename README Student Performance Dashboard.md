# 🎓 Student Performance Dashboard – Academic & Behavioral Insights

## 📌 Project Overview
This project builds an **interactive Power BI Dashboard** to analyze **academic performance, attendance, and behavioral data**.  
The goal is to provide actionable insights and recommendations for **students, faculty, and administrators** to improve outcomes.

---

## 📁 Dataset Files
The following CSV files are required:

- **Student.csv** → StudentID, Name, Gender, Class Section  
- **Academic.csv** → StudentID, SubjectID, Category, Scores, Maximum, Term  
- **Attendance.csv** → StudentID, Date, Status (Present/Absent), Reason  
- **Behavior.csv** → StudentID, Date, BehaviorType, Reason  

---

## 🧠 Project Objectives
1. **Data Modeling & Cleaning**  
   - Load all datasets into Power BI.  
   - Establish relationships between tables.
   - <img width="691" height="523" alt="image" src="https://github.com/user-attachments/assets/7b8bd493-d432-4286-8756-758409306da5" />
 
   - Clean and transform data (handle blanks, nulls, duplicates).  

2. **DAX Measures**  
   Create calculated fields for:  
   - `Average Score`  
   - `Attendance Rate`  
   - `Behavior Frequency`  
   <img width="330" height="246" alt="image" src="https://github.com/user-attachments/assets/b26f1f99-b414-4967-a9bf-1110d2447c73" />


3. **Performance Analysis**  
   - Scores per Subject  
   - Attendance per Subject  
   - Behavior per Category  
   - Performance comparison using `SWITCH()` for score ranges (e.g., Excellent, Average, Poor).  
   <img width="468" height="101" alt="image" src="https://github.com/user-attachments/assets/5bd1fdc2-e30c-4b9d-909b-084595819780" />


4. **Visualization**  
   - 📊 Bar Chart → Average Scores by Subject & Class  
   - 🍩 Donut Chart → Attendance Rate  
   - 📈 Line Chart → Behavior Frequency Trend  
   <img width="889" height="580" alt="image" src="https://github.com/user-attachments/assets/350cbc59-2934-4609-b956-fb7bc9fb3e28" />

   - 🃏 Card Visuals → KPIs (Average Attendance, Average Score, etc.) 
   <img width="390" height="243" alt="image" src="https://github.com/user-attachments/assets/1e501cc7-304a-4616-ba7f-c3b924a2e02d" />


5. **Interactivity**
- Slicers for Class, Section, Subject, Term
- Drillthrough page for individual student profile
<img width="1378" height="790" alt="image" src="https://github.com/user-attachments/assets/38f4ddf6-d3af-42d3-8d73-52411529aec5" />

- Tooltips with mini charts or metrics
<img width="1125" height="793" alt="image" src="https://github.com/user-attachments/assets/e9566127-cb3a-428a-8a27-fe6b29041db8" />

- Bookmark navigation (e.g., switch between Academic and Behavioral views)
<img width="195" height="233" alt="image" src="https://github.com/user-attachments/assets/086da446-a592-48ef-aa4f-d0284c20c0f2" />

   

6. **Customization**  
   - Add slicers for Class, Gender, Subject, Term.  
   <img width="382" height="460" alt="image" src="https://github.com/user-attachments/assets/c9a6f145-ddb2-41fc-8671-776508f59b68" />

   - Apply a custom dashboard theme.  
   - Create an **Insight Page** with key metrics & recommendations.  
   <img width="434" height="566" alt="image" src="https://github.com/user-attachments/assets/e0377588-4143-4a90-b40f-b8ed008944b8" />


7. **Optional**  
   - Mobile layout for Power BI mobile app.  

---

## 🧮 DAX Formulas


### Calculated Columns
#### DAX

-- Average Score per Student
AverageScore = DIVIDE(SUM(Academic[Scores]), SUM(Academic[Maximum]))

-- Attendance Flag
AttendanceFlag = IF(Attendance[Status] = "Present", 1, 0)

-- Behavior Count
BehaviorCount = COUNTROWS(Behavior)

-- Average Score (Overall)
AvgScore = AVERAGE(Academic[Scores])

-- Attendance Rate
AttendanceRate = DIVIDE(SUM(Attendance[AttendanceFlag]), COUNTROWS(Attendance))

-- Behavior Frequency
BehaviorFrequency = COUNTROWS(Behavior)

-- Performance Category using SWITCH
PerformanceCategory = SWITCH(
    TRUE(),
    [AvgScore] >= 90, "Excellent",
    [AvgScore] >= 75, "Good",
    [AvgScore] >= 60, "Average",
    "Needs Improvement"
)


## Project Overview
### 1.Main Dashborard
<img width="1295" height="714" alt="image" src="https://github.com/user-attachments/assets/bcd59d94-1d65-4b37-807b-74dd70bb8851" />

### 2. Student Profile Dashboard
<img width="1268" height="712" alt="image" src="https://github.com/user-attachments/assets/ddbb780d-993b-42df-8ffe-86dfce143c3a" />

### 3. Tooltip Page
<img width="421" height="325" alt="image" src="https://github.com/user-attachments/assets/d167de11-de51-4ca9-a8df-fe834445794b" />

### 4. StoryTelling
<img width="1314" height="743" alt="image" src="https://github.com/user-attachments/assets/44b85414-6590-4b1e-abb7-b62f81cc8f7a" />

### 5.Mobile Layout
<img width="500" height="730" alt="image" src="https://github.com/user-attachments/assets/29c87560-e8cd-47ce-a60c-65855dd113fb" />
<img width="490" height="622" alt="image" src="https://github.com/user-attachments/assets/cabe14aa-1819-4de8-a1d5-0f820bf9ec39" />
<img width="486" height="733" alt="image" src="https://github.com/user-attachments/assets/72882843-e0eb-4bfc-93cc-d17ce5e1b966" />
<img width="486" height="718" alt="image" src="https://github.com/user-attachments/assets/91c067ff-3fd9-469f-a8d7-fa2672ce4f43" />
<img width="463" height="738" alt="image" src="https://github.com/user-attachments/assets/b57c8161-625f-41b4-be15-8f126e9400be" />
<img width="460" height="737" alt="image" src="https://github.com/user-attachments/assets/e4fbd242-fd41-4733-ac65-ace6006826bd" />










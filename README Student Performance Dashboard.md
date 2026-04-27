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
   - Clean and transform data (handle blanks, nulls, duplicates).  

2. **DAX Measures**  
   Create calculated fields for:  
   - `Average Score`  
   - `Attendance Rate`  
   - `Behavior Frequency`  

3. **Performance Analysis**  
   - Scores per Subject  
   - Attendance per Subject  
   - Behavior per Category  
   - Performance comparison using `SWITCH()` for score ranges (e.g., Excellent, Average, Poor).  

4. **Visualization**  
   - 📊 Bar Chart → Average Scores by Subject & Class  
   - 🍩 Donut Chart → Attendance Rate  
   - 📈 Line Chart → Behavior Frequency Trend  
   - 🃏 Card Visuals → KPIs (Average Attendance, Average Score, etc.)  

5. **Customization**  
   - Add slicers for Class, Gender, Subject, Term.  
   - Apply a custom dashboard theme.  
   - Create an **Insight Page** with key metrics & recommendations.  

6. **Optional**  
   - Mobile layout for Power BI mobile app.  

---

## 🧮 DAX Formulas (Copy‑Ready)

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

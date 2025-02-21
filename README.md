# 📊 Developer Salary & Job Satisfaction Analysis at Stack Overflow- Power BI Report

## 📌 Overview
This Power BI report provides a **comprehensive analysis of global developer salaries, job satisfaction levels, and work mode preferences** using survey data from Stack Overflow. The insights help in understanding **regional salary trends, satisfaction metrics, and the impact of remote vs. on-site work.**

## 📁 Dataset
- **Source:** Stack Overflow Developer Survey Data
- **Key Fields Used:**
  - `ConvertedCompYearly` (Annual Salary)
  - `Country`
  - `WorkMode` (Remote, Hybrid, On-site)
  - `JobSatisfaction`
  - `YearsExperience`

## 📊 Visuals & Key Insights
### 1️⃣ **Geographic Distribution of Developers**
   - **Map Visual:** Displays the top respondent countries (USA, Germany, India) and highlights Europe's overall dominance in developer participation.
   
### 2️⃣ **Work Mode by Age & Remote vs. On-site Work Trends**
   - **Stacked Bar Chart:** Shows work preference distribution across age groups, with hybrid work being the most dominant model.
   
### 3️⃣ **Salary Trends Over Time**
   - **Waterfall Chart:** Analyzes yearly salary increases and decreases, tracking compensation growth across the years.
   
### 4️⃣ **Satisfaction vs. Salary by Country**
   - **Scatter Plot & KPI Cards:** Correlates job satisfaction levels with developer salaries in different countries, revealing that European countries maintain high satisfaction despite moderate salaries.
   
### 5️⃣ **Salary vs. Cost of Living**
   - **Heatmap:** Adjusts salary data based on the cost-of-living index, showing where developers earn the most in real terms.
   
### 6️⃣ **Experience vs. Salary Growth**
   - **Line Chart:** Tracks how salary evolves with years of experience, highlighting key salary jumps at different career stages.

## 📈 DAX Measures & Calculations
Key **DAX formulas** used in this report:

```DAX
SalaryChange =
VAR CurrentYearSalary =
    CALCULATE(
        AVERAGE('Survey'[ConvertedCompYearly]),
        'Survey'[Year] = MAX('Survey'[Year])
    )
VAR PreviousYearSalary =
    CALCULATE(
        AVERAGE('Survey'[ConvertedCompYearly]),
        'Survey'[Year] = MAX('Survey'[Year]) - 1
    )
RETURN
    CurrentYearSalary - PreviousYearSalary
```

## 📦 Features & Functionalities
✅ **Interactive Filters** (Year, Country, Work Mode)  
✅ **Drill-down capabilities** for deeper insights  
✅ **Custom KPI cards** tracking key metrics  
✅ **Color-coded visualizations** for easy interpretation  

## 📌 How to Use the Report
1. **Load the Power BI file (.pbix) into Power BI Desktop.**
2. **Ensure the dataset is correctly linked and refreshed.**
3. **Use the interactive filters to explore different insights.**
4. **Analyze trends, compare regions, and extract key workforce insights.**

## 🚀 Future Enhancements
- **Machine Learning-powered Salary Prediction Model**
- **Industry-Specific Salary Analysis**
- **Deeper insights into developer technologies & skills**

## 👨‍💻 Author & Contribution
Developed by **Sahil Gaur**, incorporating **DAX, Power Query, and interactive Power BI visuals** to create an insightful and data-driven report.

For any queries or suggestions, feel free to reach out! 🚀


# Road_Accidents_Analysis_Dashboard

## Table of Contents
* Introduction
* Aimed to Solve
* Dashboard KPI's
* DAX Formulas Used in Measures
* Challenges
* Learnings
* Summary

## Introduction
In an era where data drives decisions, road safety remains a paramount concern. The ability to analyze and interpret road accident data is critical for policymakers, law enforcement agencies, and the public alike. The "Road Accidents Analysis Dashboard using Power BI" project was born out of the need for a comprehensive, accessible, and informative tool to explore road accident trends and gain actionable insights.<br>

## Aimed to Solve
1. Identify accident hotspots.
2. Analyze accident trends.
3. Enable user-friendly data exploration.
4. Ensure data privacy compliance.
5. Promote informed decisions for road safety.

## Dashboard KPI's
* Primary KPI's - Total Casualties and Total Accident values for Current Year and YoY Growth.
* Primary KPI's - Total Casualties by Accident Severity for Current Year and YoY Growth.
* Secondary KPI's - Total Casualties with respect to Vehicle Type for Current Year.
* Monthly Trend showing comparison of Casualties for Current Year and Previous Year.
* Casualties by Road Type for Current Year.
* Current Year Casualties by Area/Location & Day/Night.
* Total Casualties and Total Accident by Location. <br>
 <div align="center">
   <strong>Dashboard</strong><br>
  <img width="818" alt="image" src="https://github.com/Ajay-V1/Road_Accidents_Analysis_Dashboard/assets/132564171/c306ddbf-749b-4ee1-87ea-e3acf1e725f5">
</div>

## DAX Formulas Used in Measures
1. Total Casualties For Current Year and Year on Year Growth<br>
   (a) Current Year To Date Casualties -- CY Casualties Measure
   * CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])
   (b) Previous Year Casualties -- PY Casualties Measure
   * PY Casualties = CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR('Calendar'[Date]))
   (c) Year on Year Growth of Casualties - YoY Casualties Measure
   * YoY Casualties = ([CY Casualties] - [PY Casualties])/[PY Casualties]<br>
   
2. Total Accidents for Current Year and Year on Year Growth
   (a) Current Year Accidents Count -- CY Accidents Count Measure
   * CY Accidents Count = TOTALYTD(COUNT(Data[Accident_Index]), 'Calendar'[Date])
   (b) Previous Year Accidents Count -- PY Accidents Count Measure
   * PY Accidents Count = CALCULATE(COUNT(Data[Accident_Index]), SAMEPERIODLASTYEAR('Calendar'[Date]))
   (c) Year on Year Growth of Accidents - YoY Accidents Measure
   * YoY Accidents = ([CY Accidents Count]-[PY Accidents Count])/[PY Accidents Count]
  

## Challenges
* Data Quality and Consistency: Dealing with raw accident data often involves data quality issues like missing values, duplicates, and inconsistencies. Cleaning and standardizing the data posed a significant challenge.
* Complex Visualizations: Creating meaningful and informative visualizations that effectively communicated insights from the data without overwhelming the user presented design and data visualization challenges.
* User Education: Helping users, especially those unfamiliar with data analysis, understand how to use the dashboard effectively and interpret the visualizations was an ongoing challenge.

## Learnings
* Power BI Proficiency: Developed a strong skill set in using Power BI, from importing and modeling data to creating interactive dashboards and reports.
* Data Analysis: Acquired the ability to extract valuable insights from accident data, including identifying trends, seasonality, and risk factors contributing to accidents.
* Performance Optimization: Explored techniques to optimize the dashboard's performance, such as aggregating data, optimizing DAX calculations, and using summary tables.

## Summary
Our "Road Accidents Analysis Dashboard using Power BI" project provides data-driven insights into road safety. The user-friendly dashboard empowers users to explore accident data, identify hotspots, and drive safety improvements. We've prioritized data privacy and continuous learning, making this a valuable resource for all concerned with safer roads.<br>







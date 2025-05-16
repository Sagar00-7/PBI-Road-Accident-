# PBI-Road-Accident-

Table of Contents
Introduction<br>
Dashboard Requirements<br>
Installation / Usage<br>
DAX Formulas Used in Measures<br>
Bug / Feature Request<br>
Authors<br>

Introduction<br>
This Power BI report provides a detailed analysis of road accident data in the United Kingdom. It presents key insights related to total casualties, accident types, vehicle involvement, and location-based trends.<br> 
The dataset can be accessed from this link: UK Road Accident Dataset (Google Sheets).<br>
The dashboard supports quick identification of critical risk factors and high-impact areas for road safety improvements.<br>

Dashboard Requirements<br>
Primary KPI's - Total Casualties and Total Accident values for Current Year and YoY Growth
Primary KPI's - Total Casualties by Accident Severity for Current Year and YoY Growth
Secondary KPI's - Total Casualties with respect to Vehicle Type for Current Year
Monthly Trend showing comparison of Casualties for Current Year and Previous Year
Casualties by Road Type for Current Year
Current Year Casualties by Area/Location & Day/Night
Total Casualties and Total Accident by Location

Installation / Usage
Open the .pbix file in Power BI Desktop.
Refresh the data (if connected to an external source).
Use the filters on the top of the dashboard to narrow down insights by:
  Road Surface
  Weather Conditions
Interact with the charts to drill into specific insights.

DAX Formulas Used in Measures
1. Total Casualties For Current Year and Year on Year Growth

(a) Current Year To Date Casualties -- CY Casualties Measure
CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])

(b) Previous Year Casualties -- PY Casualties Measure
PY Casualties = CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR('Calendar'[Date]))

(c) Year on Year Growth of Casualties - YoY Casualties Measure
YoY Casualties = ([CY Casualties] - [PY Casualties])/[PY Casualties]

2. Total Accidents for Current Year and Year on Year Growth

(a) Current Year Accidents Count -- CY Accidents Count Measure
CY Accidents Count = TOTALYTD(COUNT(Data[Accident_Index]), 'Calendar'[Date])

(b) Previous Year Accidents Count -- PY Accidents Count Measure
PY Accidents Count = CALCULATE(COUNT(Data[Accident_Index]), SAMEPERIODLASTYEAR('Calendar'[Date]))

(c) Year on Year Growth of Accidents - YoY Accidents Measure
YoY Accidents = ([CY Accidents Count]-[PY Accidents Count])/[PY Accidents Count]

Bug / Feature Request
If you encounter issues or would like to suggest improvements:
Email: sagar007ak@gmail.com
Or raise an issue on the project repository (if applicable)

Authors
Your Name: Sagar
Role: Data Analyst / Power BI Developer
Email: sagar007ak@gmail.com
LinkedIn: www.linkedin.com/in/sagar1505





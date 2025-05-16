# PBI-Road-Accident-

Table of Contents<br>
Introduction<br>
Dashboard Requirements<br>
Installation / Usage<br>
DAX Formulas Used in Measures<br>
Bug / Feature Request<br>
Authors<br>

<b>Introduction</b><br>
This Power BI report provides a detailed analysis of road accident data in the United Kingdom. It presents key insights related to total casualties, accident types, vehicle involvement, and location-based trends.<br> 
The dataset can be accessed from this link:[https://drive.google.com/drive/folders/1G3BFBOcSn-i-8aJ6c_MgGWJzhYWM_Okb?usp=sharing](https://docs.google.com/spreadsheets/d/1tdsA0IuAA_pTvupbG5sFtOZEm7qk0kpX/edit?gid=324101254#gid=324101254)(Google Sheets).<br>
The dashboard supports quick identification of critical risk factors and high-impact areas for road safety improvements.<br>

<b>Dashboard Requirements</b><br>
•Primary KPI's - Total Casualties and Total Accident values for Current Year and YoY Growth.<br>
•Primary KPI's - Total Casualties by Accident Severity for Current Year and YoY Growth.<br>
•Secondary KPI's - Total Casualties with respect to Vehicle Type for Current Year.<br>
•Monthly Trend showing comparison of Casualties for Current Year and Previous Year.<br>
•Casualties by Road Type for Current Year.<br>
•Current Year Casualties by Area/Location & Day/Night.<br>
•Total Casualties and Total Accident by Location.<br>

<b>Installation / Usage</b><br>
Open the .pbix file in Power BI Desktop.<br>
Refresh the data (if connected to an external source).<br>
Use the filters on the top of the dashboard to narrow down insights by:<br>
    •Road Surface<br>
    •Weather Conditions<br>
Interact with the charts to drill into specific insights.<br>

<b>DAX Formulas Used in Measures</b><br>
1. Total Casualties For Current Year and Year on Year Growth<br>
(a) Current Year To Date Casualties -- CY Casualties Measure<br>
CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])<br>

(b) Previous Year Casualties -- PY Casualties Measure<br>
PY Casualties = CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR('Calendar'[Date]))<br>

(c) Year on Year Growth of Casualties - YoY Casualties Measure<br>
YoY Casualties = ([CY Casualties] - [PY Casualties])/[PY Casualties]<br>

2. Total Accidents for Current Year and Year on Year Growth<br>
(a) Current Year Accidents Count -- CY Accidents Count Measure<br>
CY Accidents Count = TOTALYTD(COUNT(Data[Accident_Index]), 'Calendar'[Date])<br>

(b) Previous Year Accidents Count -- PY Accidents Count Measure<br>
PY Accidents Count = CALCULATE(COUNT(Data[Accident_Index]), SAMEPERIODLASTYEAR('Calendar'[Date]))<br>

(c) Year on Year Growth of Accidents - YoY Accidents Measure<br>
YoY Accidents = ([CY Accidents Count]-[PY Accidents Count])/[PY Accidents Count]<br>

<b>Bug / Feature Request</b><br>
If you encounter issues or would like to suggest improvements:<br>
Email: sagar007ak@gmail.com<br>
Or raise an issue on the project repository (if applicable)<br>

<b>Authors</b><br>
Your Name: Sagar<br>
Role: Data Analyst / Power BI Developer<br>
Email: sagar007ak@gmail.com<br>
LinkedIn: www.linkedin.com/in/sagar1505<br>





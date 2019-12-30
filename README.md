# DataMiningTableau
Tableau for Data Mining

This repository contains 2 datasets - OfficeSupplies.csv and ChurnModelling.xlsx - and uses Tableau to analyze data to determine relationship between various data attributes and the outcomes as well as visualize these relationships. Both datasets are described below along with steps for data mining:

-----------------------------------------------------------------------------------------------------------------------------------------
Dataset 1: Office Supplies

Description:

Each row in the dataset has info for each order of Office Supplies. The dataset contains the following columns:

OrderDate - The date each item was ordered
Region - Region where each item was sold
Rep - The customer service representative that made the sale
Item - The item that was ordered 
Units - The number of units of the ordered item 
Unit Price - The price of each unit of item ordered

Objective: 

Given the dataset 'DatasetOfficeSupplies.csv' on sales of office supplies, find out using Tableau which customer service Rep from each Region should get the bonus based on their Total Sales.

Perform the following steps to get the results as shown in files AnnualEmployeeBonus.pptx and AnnualEmployeeBonus.twb:

Step 1: Connect the dataset to Tableau.

Step 2: Create a calculated field Total Sales = Units * Units Price.

Step 3: Drag Total Sales in Rows; Drag Region in Columns; Drag Rep in Columns after Region. 

Step 4: On the Total Sales axis click the sorted bar chart icon to sort Rep by descending order with respect to Total Sales.

Step 5: Drag Region from Dimensions to Colour in Marks panel to give each region its own unique color.

Step 6: Drag Total Sales from Measures to Labels in Marks panel to show total sales made by each employee on the chart.

Step 7: Right Click on the wokrsheet and click Format. On the left Format pane click the Fields dropdown and select SUM(Total Sales).

a) On the Pane tab, Click the Numbers dropdown and Select Currency (Custom). Change the Display Units to Thousands.

b) Repeat a) for Axis tab. Step 8: Rename your sheet to Annual Employee Bonus or whatever name you think is suitable. Save your final chart.

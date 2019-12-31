# DataMiningTableau
Tableau for Data Mining

This repository contains 2 datasets - OfficeSupplies.csv and ChurnModelling.xlsx - and uses Tableau to analyze data to determine relationship between various data attributes and the outcomes as well as visualize these relationships. Both datasets are described below along with steps for data mining:

----------------------------------------------------------------------------------------------------------------------------------------
WhoGetsTheBonus 

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

  b) Repeat a) for Axis tab.

Step 8: Rename your sheet to Annual Employee Bonus or whatever name you think is suitable. Save your final chart.

Conclusion: 
Central: Award bonus to Matthew
East: Award bonus to Susan
West: Award bonus to James

----------------------------------------------------------------------------------------------------------------------------------------
Churn Modelling 

Description:

The dataset represents information for a sample of 10000 customers of a bank. Each row in the dataset has info for each customer and the last column 'Exited' has a value 0 (customer did not exit the bank) or 1 (customer exited the bank). The dataset contains the following columns:

CusotmerId - The ID of each customer assigned by the bank
Surname - Last name of customer
CreditScore - The customer's credit score
Geography - The location of the the customer 
Age - Age of customer
Tenure - Number of years for which the customer had an account with the bank before the data was gathered
Balance - Balance of each customer by the time data was gathered
NumOfProducts - Number of products the customer has/had with the bank
HasCrCard - 1 means the customer has/had credit card with the bank at the time of gathering data; 0 means they did not have credit card
IsActiveMember - 1 means the customer has (0 means has not) used bank's services/products in the 6 months prior to gathering the data
EstimatedSalary - The salary of the customer estimated by the bank at the time of gathering data
Exited: 0 means the customer did not exit the bank; 1 means the customer did exit the bank

Objective: 

Given the dataset 'ChurnModelling.xslx', find out using Tableau which factor is a good (or bad) predictor of a customer exiting a bank.

Perform the following steps to get the results as shown in files ChurnModelling.pptx and ChurnModelling.twb:

Step 1: Connect the dataset to Tableau.

Step 2: Since Exited has values 0 or 1, it's treated by Tableau as a numerical variable and therefore is placed under Measures; drag Exited to Dimensions for it to be correctly identified as a categorical variable

To visulaize the effect of Gender on Exited outcome:

Step 3: Drag Gender to Columns; Drag Number of Records Rows; Drag Exited to Colour under Marks to identify how many custoemrs of each Gender exited the bank 

Step 4: To label the exact numbers of customers that left the bank, drag Number of Records to Label under Marks.

Step 5: As number of males and females is not equal, getting the percentages instead of absolute values may help compare the effect of gender better; click dropdown for Number of Records under Marks>Add Table Calculation. Choose Percent of Total as Calculation Type, under Compute Using select Table (down). To make the percentages simpler, Click Number of Records dropdown and click Format. On the left panel under Default, click Numbers dropdown and select Perecentage and choose 0 decimal places. 

Step 6: To make the axis consistent with the chart, Press ctrl and drag Number of Records from Marks to Rows. This will replace the format for Number of Records in Rows to the one in Marks.

Step 7 (Optional): You can add a reference line as a baseline to decide which gender (or any attribute for that matter) is above or below it. We can set this to the number of customers that left the bank as a percentage of the entire sample. Remove Gender from Columns by right clicking Gender in Columns field and clicking Remove. The resulting graph shows that 20% of all customers from the sample left the bank. Now you can press Ctrl+Z to get Gender back in the Columns field. To add the reference line at 20%, right click y-axis and click Add a Reference Line. For the Value field 2nd dropdown, change it from Average to Constant, then Change the value to 0.2 (or 20%) and press OK. This adds a reference line at the 20% mark.

Step 8: Rename your wokrsheet to Gender

Conclusion: 

Since 25% of all females (above 20% mark) left the bank whereas only 16% of all males(below 20% mark) left the bank, on average female customers are more likely to churn compared to male customers.

To find out whether which country you live in affects if you're likely to Exit the bank or not:

Step 9: Replicate the Gender worksheet by Right-clicking Gender tab and clicking Duplicate.

Step 10: Replace Gender in Columns with Geography by dragging Geogrpahy from Dimensions to Columns

Step 11: Rename your sheet to Country

Conclusion:

German customers have a higher churn rate compared to France and Spain

To find out whether or not having a credit card affect if a customer will leave the bank:

Step 12: Replicate the Country worksheet by Right-clicking Country tab and clicking Duplicate.

Step 13: Drag HasCrCard from Measures to Dimensions as it is a categorical variable. 

Step 14: Replace Geography in Columns with HasCrCard by dragging HasCrCard from Dimensions to Columns.

Step 15: To make your results visually clear replace 0 and 1 values for HasCrCard with their aliases. Click HasCrCard dropdown in Dimensions and click Aliases. Give 0 a value of No and 1 a value of Yes. Then click OK.

Step 16: Rename your sheet to HasCrCard.

Conclusion:

Having a credit card is not an important factor in determining if a customer will churn.

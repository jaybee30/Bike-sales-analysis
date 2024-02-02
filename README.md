# Bike-sales-analysis
The purpose of this analysis is to understand the bike sales market, clean the messy dataset, generate insights from the dataset which will in turn guide on making useful business decision.


DATA COLLECTION

The dataset was obtained from Github from Alex the analyst. The dataset was downloaded into an excel sheet. The link for the dataset is https://github.com/AlexTheAnalyst/Excel-Tutorial/blob/main/Excel%20Charts%20Tutorial%20File.xlsx

The dataset consists of; 13 columns and 1027 rows. The dataset consists of column a unique ID and other 12 variables. The column names include; ID, Marital Status, Gender, Income, Children Education, Occupation, Home Owner, Cars, Commute Distance, Region, Purchased Bikes.

DATA CLEANING

Data cleaning is an important process in the data analysis. This is an important process as it provides a complete understanding of the dataset which will in turn guide the analyst to gain insights and make accurate business decisions. Data cleaning may involve one or all of the following steps: Removal of duplicates, fixing structural errors, filtering unwanted outliers, handling missing data, and lastly validation.

DATA CLEANING STEPS

1.Removal of Duplicates: This was done by selecting the whole table, clicking on the Data tab> Data tools> Remove duplicates tab> OK. 26 duplicates were found and removed.

2.MARITAL STATUS: Using the Find and replace option (CRTL + H). I used the find and replace tab to change the “M” to “Married” and “S” to “Single”. 

3. GENDER: Using the find and replace tab, the ‘M’ and ‘F’ gender column was replaced with “M” for “Male” and “F” for “Female”.

4. INCOME: The data type column of the income column was changed from ‘General’ to ‘Accounting’

5. . Income range: A new column to group the income into categories using the IF statement.
=IF(E3>100000,"VERY HIGH", IF(E3>=60000,"HIGH", IF(E3<60000,"AVERAGE","")))

6. Commute distance: The commute distance was given in (0-1 miles, 1-2 miles, 2-5 miles, 5-10 miles, 10+ miles). This is obscure for the sake of our data analysis.
So, a new column was created and named as DISTANCE REGION which grouped the commute distance into (Very short, short, medium, far, very far) using the nested IF statement below: 

=IF(L2="0-1 Miles", "Very short", IF(L2="1-2 Miles", "Short", IF(L2="2-5 Miles", "Medium", IF(L2="5-10 Miles", "Far", IF(L2="10+ Miles", "Very far ","")))))

7. AGE COLUMN: I changed the age column naming them “adolescent, middle age, and old age” using the nested IF statement. The nested IF function helped me categorize the ages into age groups, this was important as it helped in the analysis process.

NESTEDIF Statement
=IF(O2>60,"Old Adults", IF(O2>=40, "Middle Age", IF(O2<40, "Young Adults", "")))

PROBLEM STATEMENT

•	What influence does income range has on bike purchase?

•	What effect does commute distance has on bike purchase?

•	What is the rate of bike purchase based on the Age Groups?

•	Bike purchase based on region?

•	What effect does marital status has on bike purchase?



DATA VISUALISATION

With the aid of Pivot Charts in excel, an interactive dashboard reports was created, i also incorporated slicers for an effortless user experience and to help filter the dashboard based on Marital status, Region, Education, and Occupation.

**INSIGHTS**

•	Male bike buyers bought bikes at a higher rate than their female counterparts, this might be due to higher purchasing power because they earn higher than their female counterpart which may be a factor causing a slight difference in the purchase rate.
•	Customers with very short distance (0–1 miles) purchased the highest number of bikes.
•	Customers within the middle Age bracket purchased more bikes (52%) compared to other age groups.
•	Customers within the Average income range made highest bike purchase.
•	Based on region, individuals in North America purchased bikes at a higher rate compared to other regions being the Pacific and Europe.
 

![dashboard](https://github.com/jaybee30/Bike-sales-analysis/assets/106179938/71ef6fc8-bfb7-4ff0-a65d-3cde6fa721a8)



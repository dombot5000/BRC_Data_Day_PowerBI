# BRC_Data_Day_PowerBI #
Instructions for British Red Cross Data Day @ CUSP London


## 1. Introducing PowerBI ##


#### a) Open PowerBI ####
If you have not downloaded go to <https://powerbi.microsoft.com/en-us/downloads/>


#### b) Explore the views ####
Report, Data and Relationships


#### c) Explore data connection options ####


**Home > Get Data > More > Web**


d) Enter URL <https://en.wikipedia.org/wiki/List_of_highest_mountains_on_Earth> and load


e) **Edit Queries** and select **Height m** column


f) **Transform** and change from **Text** to **Whole Number** then **Close and Apply**

g) Make a chart and map 


## 2. Loading data ##


## 3. Tidying up our model ##


## 4. Creating measures ##

In *FactTrees* click *...* and select *New Measure* then enter *No. Trees = COUNTROWS(FactTrees)*


In *FactBoroughPop* click *...* and select *New Measure* then enter *Population = SUM(FactBoroughPop[All usual residents])*


In *FactBoroughPop* click *...* and select *New Measure* then enter *Trees Per Person = [Population]/[No. Trees]*


Let's see what that looks like in a table - uh-oh we have an infinity problem - lets edit our *Trees Per Person* measure

*TreesMeasure 3 = IFERROR([Population]/[No. Trees], BLANK())*

## 5. Exploring geography ##





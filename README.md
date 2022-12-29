# Excel-projects

## 1. Bike Purchases

### Overview of data
This dataset was downloaded from Kaggle website. Click [here](https://www.kaggle.com/datasets/heeraldedhia/bike-buyers) to download this file. This dataset contains **13** columns of **1001** samples of individuals from different backgrounds and demography. The columns are **ID, Marital status, Gender, Income, Children, Education, Occupation, Home owner, Cars, Commute distance, Region, Age and Purchased bike**

### Objective and questions
1. To find out the total number of individuals who have purchased a bike from each category.
2. Is the power of purchasing a bike linearly related to the income of individuals?

### Hypothesis
1. The highest paying individual purchases the most number of bikes

### Data exploration 
A thorough look at the dataset reveals multiple rows with missing and inaccurate values. There were 7 missing values in marital status, 11 in gender, 6 in income, 8 in children, 4 in home owner, 9 in cars and 8 in age columns repectively across the dataset. On the other hand, since this dataset deals with 1000 individuals each with a certain unique ID's, the ID column needed to be checked in excel for a possible duplicate values however none was found in them. 

### Data cleaning
After careful observation, any rows with missing value were not removed from the dataset but replaced with another values that are meaningful. The data contains a lot of missing value of different column, therefore, removing them completely from the dataset would lead to bias and inaccuracy of the data. In order handle these missing values, each column with the missing data was imputed with the highest occurence records found in each respective column. Pandas module was used in python to find the frequncies and replace the missing values accordingly. View [here](https://github.com/aminbasiran/excel-projects/blob/main/cleaned_bike_buyers.ipynb) for the source code in python.

Since the value of age would create multiple distinct values to deal with in the next step, a new column called "Age group" was introduced to group the individual within certain age range. Those invividuals whose age below 60 falls under the middle age group while the rest falls under the senior citizen group. Refer cells below;

| Age |
| --- |
| 42  |
| 43  |
| 60  |
| 41  |
| 36  |
| 50  |
| 33  |
| 43  |

=IF([@Age]<60,"Middle age","Senior citizen")

| Age | Age group      |
| --- | -------------- |
| 42  | Middle age     |
| 43  | Middle age     |
| 60  | Senior citizen |
| 41  | Middle age     |
| 36  | Middle age     |
| 50  | Middle age     |
| 33  | Middle age     |
| 43  | Middle age     |

### Observation and results derived from the dataset

After cleaning the data, we will begin to look at the dataset from multiple perspectives systematically by using Pivot table. Multiple pivot tables were created to better lay out the number of bikes each individual purchases by different perspective. Table 1 below is a pivot table that illustrates the number of bike purchases by marital status. Click [here](https://github.com/aminbasiran/excel-projects/blob/main/Bike%20purchases.xlsx) to jump into the excel file to view cleaned data, pivot tables and dashboard.

| Bike        | Column Labels |     |             |  
| ----------- | ------------- | --- | ----------- |
| Row Labels  | No            | Yes | Grand Total |
| Married     | 308           | 234 | 542         |
| Single      | 211           | 247 | 458         |
| Grand Total | 519           | 481 | 1000        |

Table 1.1 Bike puchases by marital status

<img src="https://user-images.githubusercontent.com/111835474/209469759-5576f3a8-bc4f-40c1-a154-54b04c15b785.png" width="400" height="200" />

Based on the observations(collected from the pivot table) generated in the excel file, a total of 234 married individuals have purchased a bike compared to a slighly higher number of 247 single individuals. A 9.74% difference between those 2 numbers. In addition, the total numbers of purchased bikes from female and male individuals are 308 and 211 repectively.

On the other hand, according to the next pivot table, it is evident that an individual who makes RM40,000 a year contributed the most bike purchases of 89 individuals followed by 87 individuals who makes RM60,000 a year while the lowest recorded of bike purchases came from a single individual making RM170,000 a year. 

Next, an individual who makes commute less than a mile has contributed the highest number of bike purchases with a total of 200 individuals. Breaking down further into the table, it is observed that out of the 200 individuals, only 100 of them didn't own a single car. Conversely, only 33 individuals who needs to commute more than 10 miles have purchased a bike. 

Next, looking into the regional perspective, out of 495 individuals who have purchased a bike, 148 of them located in europe, followed by 220 individuals located in the north america and 113 from the pacific region.

In addition, from the line graph plotted by the number of purchases against the yearly income, is it concluded that they are not linearly related. Despite the graph showed an increase from 30 to 94 individuals from RM10,000 to RM40,000 of yearly income, the pattern shifted and dropped as the income reaches RM60,000. On top of that, hypothesis is denied because it was evident that only a single individual whose income reaches Rm170,000 purchased a bike.




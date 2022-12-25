# Excel-projects

## 1. Bike Purchases

### Overview of data
This dataset was downloaded from Kaggle website. Click [here](https://www.kaggle.com/datasets/heeraldedhia/bike-buyers) to download this file. This dataset contains **13** columns of **1001** samples of individuals from different backgrounds and demography. The columns are **ID, Marital status, Gender, Income, Children, Education, Occupation, Home owner, Cars, Commute distance, Region, Age and Purchased bike**

### Objective and questions
1. To identify which category contributes the most on the purchases of bikes among 1000 samples
2. is the power of purchasing a bike is linearly related to income of individuals?

### Data exploration 
A thorough look at the dataset reveals multiple rows with missing and inaccurate values. There were 7 missing values in marital status, 11 in gender, 6 in income, 8 in children, 4 in home owner, 9 in cars and 8 in age columns repectively across the dataset. On the other hand, since this dataset deals with 1001 individuals each with a certain unique ID's, the ID column needed to be checked in excel for a possible duplicate values however none was found in them. 

### Data cleaning
 After careful observation, any rows with missing value were not removed from the dataset but replaced with another values that are meaningful. The data contains a lot of missing value of different column, therefore, removing them completely from the dataset would lead to bias and inaccuracy of the data. [HANDLING MISSING VALUES]

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

### Results derived from the dataset 

After cleaning the data, we will begin to look at the dataset from multiple perspectives systematically by using Pivot table. Multiple pivot tables were created to better lay out the number of bikes each individual purchases by different perspective. Table below illustrates the number of bike purchases by marital status and income group. Click [here]() to jump into the excel file to view all.

| Bike        | Column Labels |     |             |
| ----------- | ------------- | --- | ----------- |
| Row Labels  | No            | Yes | Grand Total |
| Married     | 313           | 236 | 549         |
| Single      | 218           | 259 | 477         |
| Grand Total | 531           | 495 | 1026        |

Table 1. Bike puchases by marital status

| Count of Purchased Bike | Column Labels |     |             |
| ----------------------- | ------------- | --- | ----------- |
| Row Labels              | No            | Yes | Grand Total |
| RM10,000.00             | 46            | 30  | 76          |
| RM20,000.00             | 45            | 33  | 78          |
| RM30,000.00             | 83            | 57  | 140         |
| RM40,000.00             | 65            | 94  | 159         |
| RM50,000.00             | 20            | 20  | 40          |
| RM60,000.00             | 84            | 82  | 166         |
| RM70,000.00             | 59            | 66  | 125         |
| RM80,000.00             | 58            | 36  | 94          |
| RM90,000.00             | 15            | 25  | 40          |
| RM100,000.00            | 19            | 11  | 30          |
| RM110,000.00            | 8             | 8   | 16          |
| RM120,000.00            | 8             | 11  | 19          |
| RM130,000.00            | 17            | 15  | 32          |
| RM150,000.00            | 1             | 3   | 4           |
| RM160,000.00            |               | 3   | 3           |
| RM170,000.00            | 3             | 1   | 4           |
| Grand Total             | 531           | 495 | 1026        |

Table 2. Bike puchases by income group



# Excel-projects

## 1. Bike Purchases
### Data cleaning

This dataset was provided from Kaggle website. Click [here](https://www.kaggle.com/datasets/heeraldedhia/bike-buyers) to download the file. This dataset contains **13** columns of **1001** samples of individuals from different backgrounds and demography. The columns are **ID, Marital status, Gender, Income, Children, Education, Occupation, Home owner, Cars, Commute distance, Region, Age and Purchased bike**. A thorough look at the dataset reveals multiple rows with missing and inaccurate values. After careful observation, any rows with missing value were not removed from the dataset but replaced with another values that are meaningful. The data contains a lot of missing value of different column, therefore, removing them completely from the dataset would lead to bias and inaccuracy of the data. [HANDLING MISSING VALUES]

Since the value of age would create multiple distinct values to deal with in the next step, a new column called "age group" was introduced to group the individual within certain age range. Those invividuals whose age below 60 falls under the middle age group while the rest falls under the senior citizen group. Refer cells below; 


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


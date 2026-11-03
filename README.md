# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT

```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
df = pd.read_csv("/content/titanic_dataset.csv")
df
```
<img width="699" height="287" alt="image" src="https://github.com/user-attachments/assets/db9e7de0-8070-459f-91f5-876fefb7ca12" />

```
df.info()
```
<img width="302" height="215" alt="image" src="https://github.com/user-attachments/assets/fd7eef88-5208-468a-9fc3-3624ad744dab" />

```
df.describe()
```
<img width="494" height="186" alt="image" src="https://github.com/user-attachments/assets/c5c702f2-6182-4d9b-acbe-655dace14bae" />

```
df.shape
```
<img width="243" height="58" alt="image" src="https://github.com/user-attachments/assets/a22dbe5d-b5b0-4a79-95ea-3e36fb74cf1b" />

```
df.dtypes
```
<img width="320" height="297" alt="image" src="https://github.com/user-attachments/assets/0a18cd90-a862-4f96-be40-61b680b595f5" />

```
print(df.isnull().sum())
```
<img width="376" height="200" alt="image" src="https://github.com/user-attachments/assets/ee14058c-6a0b-4de7-8427-e8ce781a8d8a" />
```
df.duplicated().sum()
```
<img width="266" height="70" alt="image" src="https://github.com/user-attachments/assets/5f496a79-74ae-4e26-b9ee-a76c6df03441" />





# RESULT
        <<INCLUDE YOUR RESULT HERE>>

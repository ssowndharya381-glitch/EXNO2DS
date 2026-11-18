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
dt.nunique()
```
<img width="325" height="326" alt="image" src="https://github.com/user-attachments/assets/07804e7e-9159-4673-a0cd-4c0f1b0f7f31" />

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

```
import seaborn as sns
sns.countplot(data=dt,x="Survived")
```

<img width="509" height="380" alt="image" src="https://github.com/user-attachments/assets/78a08816-96e7-4d3a-a4dd-4d396f24e4ca" />

```
 sns.boxplot(data=dt,x="Survived")
```

<img width="457" height="381" alt="image" src="https://github.com/user-attachments/assets/50eaf5ba-86c4-4cd9-b1e3-4e1c8d6df2ac" />

```
sns.boxplot(data=dt,x="Age")
```

<img width="457" height="385" alt="image" src="https://github.com/user-attachments/assets/8308c081-942b-4e1c-b94d-98e3a4219345" />

```
sns.histplot(data=dt,x="Age")
```

<img width="437" height="329" alt="image" src="https://github.com/user-attachments/assets/2b40bdae-34f2-409a-908f-5bdd16d18087" />

```
dt.rename(columns={'Sex':'Gender'},inplace=True)
dt
```
<img width="610" height="217" alt="image" src="https://github.com/user-attachments/assets/5fb47036-6f2d-4062-8924-7b143e9d2eb2" />

```
sns.catplot(x='Survived',hue="Gender",data=dt,kind='count')
```

<img width="485" height="331" alt="image" src="https://github.com/user-attachments/assets/680c82ec-c0b4-40b1-a215-cd583f79cc73" />

```
dt.boxplot(column="Age",by="Survived")
```

<img width="452" height="311" alt="image" src="https://github.com/user-attachments/assets/72ad7f83-c4e5-4638-9895-c19a53a8f9e8" />

```
sns.scatterplot(x=dt["Age"],y=dt["Fare"])
```

<img width="506" height="294" alt="image" src="https://github.com/user-attachments/assets/b2fee46d-1c7c-4a05-9e9a-f5902dad2a5d" />

```
sns.barplot(x=dt["Age"],y=dt["Fare"])
```
<img width="455" height="292" alt="image" src="https://github.com/user-attachments/assets/351052f9-55df-4050-9559-01525be2a14c" />

```
sns.scatterplot(x=dt["Survived"],y=dt["Fare"])
```

<img width="473" height="299" alt="image" src="https://github.com/user-attachments/assets/f4671f90-7fcd-463f-adff-a655e9c127ad" />

```
sns.boxplot(x="Pclass",y="Age",hue="Gender",data=dt)
```

<img width="407" height="287" alt="image" src="https://github.com/user-attachments/assets/1af20e4c-d403-43f6-830b-ccdbbd34092f" />

```
sns.catplot(data=dt,col="Survived",x="Gender",hue="Pclass",kind="count")
```

<img width="490" height="228" alt="image" src="https://github.com/user-attachments/assets/6c1a907f-337a-40ff-85c5-563f15b83380" />

```
sns.heatmap(dt.corr(numeric_only=True))
```

<img width="449" height="327" alt="image" src="https://github.com/user-attachments/assets/0d4b5130-4655-40da-bbad-4f0c5e7b3415" />

```
sns.pairplot(dt)
```

<img width="545" height="242" alt="image" src="https://github.com/user-attachments/assets/27a21fe6-3816-42ea-afd9-2e615a5e65bf" />


## INTERPRETATION:
            The dataset was analyzed using Exploratory Data Analysis (EDA) techniques. The data was checked for missing values, duplicate records, and outliers. Statistical measures and visualizations were used to understand the data        distribution, identify patterns, and find relationships between variables.


## RESULT
     We have performed Exploratory Data Analysis on the given data set successfully.

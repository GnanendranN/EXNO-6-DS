# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
![image](https://github.com/user-attachments/assets/ac1f29e8-f684-4e57-ac8e-323dc8dc0c17)
## Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/user-attachments/assets/0c539318-85dd-402a-b650-6e97e6dcbc77)

## Multi Line Plot
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![image](https://github.com/user-attachments/assets/577fe09f-2478-4aa0-9cc2-8060c6b1d2fe)

## TO VISUALIZE RELATIONSHIPS
## Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/user-attachments/assets/4c73a359-a36d-48c7-bc46-c2728c0b00ba)

## Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/user-attachments/assets/b82e58d6-2aa1-4cf5-bf20-93acc526962c)

## TO CAPTURE DISTRIBUTIONS
## Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/user-attachments/assets/866bc97b-c075-4416-965f-9b2660068a16)

## Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/user-attachments/assets/da447ff4-49ac-4890-8d38-da25926aca9b)

## Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/user-attachments/assets/3592dada-74a9-4ebd-a984-81641e69bb34)

## DENSITY PLOT
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/user-attachments/assets/9f157d9e-32b6-41b4-8de1-7c916b2123da)

## HEATMAP
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![image](https://github.com/user-attachments/assets/2b351116-d56c-4713-93c6-fe623bf0fcad)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

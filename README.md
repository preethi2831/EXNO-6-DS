```
NAME : Preethika N
REG NO : 212223040130
```

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
![image](https://github.com/user-attachments/assets/d4a8a573-9e38-4d5c-aba6-0ff68bee47ee)
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/user-attachments/assets/5f328c42-6981-44ba-a39b-98950e2068af)
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1,label="line 1")
sns.lineplot(x=x,y=y2,label="line 2")
sns.lineplot(x=x,y=y3,label="line 3")
plt.legend()
plt.title('Multi Line Plot')
```
![image](https://github.com/user-attachments/assets/47de5d67-849f-4f03-954e-62350585558c)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/user-attachments/assets/9dee6e0d-382c-45e8-8989-709634e7a4fd)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow',hue="Pclass")
plt.title("Fare Of Passenger By Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/5b34bb08-864a-45bb-b936-e4b50b7e32d2)
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/user-attachments/assets/ef9ed814-1f0e-44db-bb97-0dad38cab18d)
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/user-attachments/assets/ac299d31-4e31-4b11-b0d3-e0a434fd31a0)
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/user-attachments/assets/0a6e921b-be0e-4918-acbd-e7565fbcae39)
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/user-attachments/assets/524da657-68f8-4baf-b336-b8352b5380c3)
```
sns.violinplot(x="Pclass", y="Fare", data=df, palette='rainbow')
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/user-attachments/assets/8c0cebc2-cd96-41dd-97a9-0ff2ada343f0)
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/user-attachments/assets/d416622e-a354-4ea6-a91c-62f98c1bec0a)
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![image](https://github.com/user-attachments/assets/8455c011-e616-4c31-aac9-2632ecdf51f4)

# Result:
 Data visualization is successfully performed using seaborn library for the given data.

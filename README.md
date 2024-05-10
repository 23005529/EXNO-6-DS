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
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/dec24568-bd44-496b-857f-f2755664664b)
```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/c87cf4ed-cb7c-4275-8f34-328fbcadac34)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/d06946aa-b541-4421-bf8a-6cc1ebd0a365)
```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/fa506e0d-469c-4112-b90e-95bd0aeb02f0)
```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/9f6301d7-2d8b-417c-a432-53151aa17121)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/3e07bb26-8169-49e4-83a1-95e3be999cdd)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/d9b2cea0-97c8-4c3f-9d4c-69fc609b9ad2)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/9601f80c-a0aa-412a-8956-4cbf1ed04809)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/67da44fe-0a61-41c9-bec4-c86a482ea889)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/cf8d5574-c6c3-4816-9409-d3650f6c2d0a)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/d7aca9dd-ca38-4b80-b2d2-b579a394791d)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/9467c871-9a09-4793-b4d3-43677fd61040)
```
num_var = np.random.randn(1)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/d2e101d6-0ff7-4c80-89e6-ac035b5ffb28)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/42513f21-905b-4240-8b49-2220cc0709ff)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/6f61c131-57ed-4395-b938-060b234859a3)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/de3c3609-5fbb-4030-a04a-08011eb65837)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/0a8d04aa-48e1-43bb-b7f0-2c710b21386b)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/0fe33cea-e925-458b-9dd7-c1acc469cf24)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/fe1471fc-a982-43f7-8f3f-ac76589681f9)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/5ec7b795-4960-4f0f-9542-115d4aef402b)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/8a466c68-cea9-44ec-b1a4-733f3a8200ed)

```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/4e3885b6-868e-4f2a-af1e-354f5a31561e)

```
sns.kdeplot(data=mart)
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/850898f0-983d-41bd-90c9-9789b619e425)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/f191fd8f-ed6b-4228-a551-52adb89cdc9a)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/44b44589-6b61-497a-afe1-425bdefb1ff3)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/b047ad42-0df6-4fc5-8f53-033318bde60b)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/23005529/EXNO-6-DS/assets/139842207/17090152-cefa-48eb-b6c6-22133d575275)

# Result:
 Thus, all the data visualization techniques of Seaborn has been implemented.

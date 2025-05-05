# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

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
import matplotlib.pyplot as plt
import numpy as np
x1=[1,2,3]
y1=[2,4,1]
plt.plot(x1,y1,label='line 1',linewidth=6)
x2=[1,2,3]
y2=[4,1,3]
plt.plot(x2,y2,label='line 2',linewidth=6)
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Two lines on same graph!')
plt.legend()
```
![5 1](https://github.com/user-attachments/assets/0ee44330-d054-4a6c-a76c-e9a7e50c52ea)

```
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color='blue',linestyle='dashed',linewidth=4,marker='o',markerfacecolor='red',markersize=14)
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Some cool Customizations')
```
![5 2](https://github.com/user-attachments/assets/4bf09e37-81e4-43dc-b340-59ecf00e4f13)

```
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896,]
plt.plot(years,apples,color='red',linewidth=5)
plt.plot(years,oranges,color='yellow',linewidth=5)
plt.xlabel('YEAR')
plt.ylabel('Yields (Tons per hectare)')
plt.title('Crop Yields in Kanto')
plt.legend(['Apples','Oranges'])
```
![5 3](https://github.com/user-attachments/assets/5b2cbb7d-4786-4020-bb60-bcd9a3e612f1)

```
x_values=[0,1,2,3,4,5]
y_values=[0,1,4,9,16,25]
plt.scatter(x_values,y_values,s=100,c='red')
plt.xlabel('X-AXIS',fontsize=14)
plt.ylabel('Y-AXIS',fontsize=14)
plt.title('Scatter Plot')
```
![5 4](https://github.com/user-attachments/assets/02bf24d5-57f5-4f66-ad26-9c847b292a1c)

```
x=[1,2,3,4,5,6,7,8,9,10]
y=[2,4,5,7,6,8,9,11,12,12]
plt.scatter(x,y,label='stars',marker='*',s=300,c='blue')
plt.xlabel('X-AXIS',fontsize=14)
plt.ylabel('Y-AXIS',fontsize=14)
plt.title('Scatter Plot Star')
plt.legend()
plt.savefig("StarScatter.png")
```
![5 5](https://github.com/user-attachments/assets/51e6fe18-15b4-4e66-a62c-22f77a871dc8)

```
x=[1,2,3,4,5,6,7,8,9]
y=[1,4,9,16,25,36,49,64,81]
plt.xlabel('X-AXIS',fontsize=14)
plt.ylabel('Y-AXIS',fontsize=14)
plt.title('Scatter Plot Star')
plt.subplot(2,2,1)
plt.plot(x,y,'ro--')
plt.subplot(2,2,2)
plt.plot(y,x,'g*--')
plt.subplot(2,2,3)
plt.plot(x,x,'bo')
plt.subplot(2,2,4)
plt.plot(y,y,'go')
```
![5 6](https://github.com/user-attachments/assets/5d64503f-1f89-434f-a0d9-e4f5fc646570)

```
import numpy as np
np.pi
```
![5 7](https://github.com/user-attachments/assets/074fd8be-0840-4cc0-9e55-7a2bc31ca272)

```
x=np.arange(0,4*np.pi,0.1)
y=np.sin(x)
plt.title("Sin Wave Form")
plt.plot(x,y,linewidth=5,c='green',linestyle='dotted')
```
![5 8](https://github.com/user-attachments/assets/3d4af565-c1fa-41f6-a30c-099acd6881eb)

```
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='red')
plt.fill_between(x,y2,color='blue')
plt.plot(x,y1,color='black')
plt.plot(x,y2,color='white')
plt.legend(['y1','y2'])
plt.show()
```
![5 9](https://github.com/user-attachments/assets/75f74576-9882-4d6c-b52d-0db900a6ea13)

```
heigth=[10,24,36,40,5]
names=['One','Two','Three','Four','Five']
c1=['g','b']
plt.bar(names,heigth,width=0.8,color=c1)
plt.xlabel('X-AXIS')
plt.ylabel('Y-AXIS')
plt.title('Bar Graph')
```
![5 10](https://github.com/user-attachments/assets/8600733b-e63f-4d57-a31a-53dbf9d041d2)

```
x=[2,8,10]
y=[11,16,9]
x2=[3,9,11]
y2=[6,15,7]
plt.bar(x,y,color='r')
plt.bar(x2,y2,color='y')
plt.xlabel('X-AXIS')
plt.ylabel('Y-AXIS')
plt.title('Bar Graph')
```
![5 11](https://github.com/user-attachments/assets/77a6617d-37eb-4e03-9f77-91c1ac0e7402)

```
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color='orange',histtype='bar',rwidth=0.8)
plt.xlabel('Age')
plt.ylabel('No. of People')
plt.title('Histogram')
```
![5 12](https://github.com/user-attachments/assets/498dc485-eef4-4ffe-91a9-f95c655d43f1)

```
x=[2,1,6,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x,bins=10,color='cyan',alpha=0.5)
plt.show()
```
![5 13](https://github.com/user-attachments/assets/e14c828f-f1bb-4cbc-a063-723cc1f7fe4a)

```
np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
data
```
![5 14](https://github.com/user-attachments/assets/fbd91c57-781b-47cc-b8f3-b689f12ca22e)

```
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Value')
ax.set_title('Box Plot')
```
![5 15](https://github.com/user-attachments/assets/6dc0d2e5-be06-411c-adb0-c478a60a3e6f)

```
act=['Eat','Sleep','Work','Play']
slices=[3,7,8,6]
colors=['yellow','blue','orange','red']
plt.pie(slices,labels=act,colors=colors,startangle=90,shadow=True,explode=(0,0.1,0,0),autopct='%1.1f%%')
plt.title('Pie Chart')
plt.show()
```
![5 16](https://github.com/user-attachments/assets/4c208e75-8cdc-42ae-bd50-61aff56e401d)

```
labels=['Python','C++','Rubby','Java']
slices=[215,130,245,210]
colors=['yellow','blue','orange','red']
plt.pie(slices,labels=labels,colors=colors,startangle=90,shadow=True,explode=(0.1,0,0.1,0),autopct='%1.1f%%')
plt.title('Equal')
plt.show()
```
![5 17](https://github.com/user-attachments/assets/c793add0-f94f-4fc2-9770-4d456883d64a)


# Result:
Thus the program to Perform Data Visualization using mathplot library for the given datas is been implemented

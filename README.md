# 8-Python-Data_Visualization

## 📘 Introduction

This  showcases three fundamental data visualization techniques using Python libraries such as `matplotlib` and `seaborn`. Visualization is a key component in data analysis, allowing patterns and insights to be quickly understood at a glance.

- **Exercise 1** uses a line plot to track the population growth of four cities over time.
- **Exercise 2** presents a scatter plot to analyze the relationship between hours studied and test scores.
- **Exercise 3** illustrates a bar chart to represent monthly sales distribution throughout the year.

These visualizations help turn raw data into a visual story, supporting better decision-making and deeper insights.



### Exercise 1: Line plot of population over time for 4 cities

#### Create a line plot using matplotlib pyplot that displays the population of four different cities over time. Each city should have its own line, and the x-axis should represent years (e.g. 2010, 2011, 2012, etc.) while the y-axis should represent the population.

##### The data for the four cities is provided below:

##### City A: [500000, 550000, 600000, 650000, 700000, 750000, 800000]

##### City B: [800000, 850000, 900000, 950000, 1000000, 1050000, 1100000]

##### City C: [1000000, 1050000, 1100000, 1150000, 1200000, 1250000, 1300000]

##### City D: [1200000, 1250000, 1300000, 1350000, 1400000, 1450000, 1500000]



#### PROGRAM 1

import matplotlib.pyplot as plt


years=[2010,2011,2012,2013,2014,2015,2016]

City_A=[500000, 550000, 600000, 650000, 700000, 750000, 800000]

City_B=[800000, 850000, 900000, 950000, 1000000, 1050000, 1100000]

City_C=[1000000, 1050000, 1100000, 1150000, 1200000, 1250000, 1300000]

City_D=[1200000, 1250000, 1300000, 1350000, 1400000, 1450000, 1500000]


plt.plot(years,City_A,label='City A',marker='o')

plt.plot(years,City_B,label='City B',marker='s')

plt.plot(years,City_C,label='City C',marker='x')

plt.plot(years,City_D,label='City D',marker='^')


plt.title("POPULATION OVER TIME 2010-2016")

plt.xlabel("Year")

plt.ylabel("Population")

plt.legend()

plt.grid(True)

plt.tight_layout()

plt.show()


#### OUTPUT 1

![image](https://github.com/user-attachments/assets/b6381b4f-c185-4a37-97bf-8e551754b5c0)



### Exercise 2: Scatter plot of hours studied vs test scores using Seaborn

#### Create a scatter plot using seaborn that shows the relationship between the number of hours studied and the test scores obtained by a group of students. Use the following data:

##### Hours Studied: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

##### Test Scores: [93, 57, 61, 54, 51, 53, 87, 81, 83, 85]



#### PROGRAM 2

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd



hours = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

scores = [93, 57, 61, 54, 51, 53, 87, 81, 83, 85]


data = pd.DataFrame({

    'Hours Studied': hours,
    
    'Test Score': scores
    
})



sns.scatterplot(data=data, x='Hours Studied', y='Test Score')

plt.title("Hours Studied vs Test Score")

plt.grid(True)

plt.show()


#### OUTPUT 2

![image](https://github.com/user-attachments/assets/e8f3bce1-12b3-46a7-b549-011592a0af53)




### Exercise 3:Bar chart of monthly sales

#### Create a bar chart using matplotlib pyplot that shows the total sales for each month of the year. Use the following data:

##### Month: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]

##### Sales: [11860, 10480, 4997, 5523, 13965, 6011, 13158, 9533, 5158, 9058, 11346, 6675]


#### PROGRAM 3


import matplotlib.pyplot as plt

Month=["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]

Sales=[11860, 10480, 4997, 5523, 13965, 6011, 13158, 9533, 5158, 9058, 11346, 6675]

plt.bar(Month,Sales)

plt.title("TOTAL MONTHWISE SALES")

plt.xlabel("Month")

plt.ylabel("Sales")

plt.show()


#### OUTPUT 3

![image](https://github.com/user-attachments/assets/4c8d935c-4c9e-4d34-b2eb-f350a61d78f7)



## ✅ Conclusion

Through these exercises, we explored the versatility and effectiveness of data visualization tools in Python. The line plot clearly demonstrated growth trends across cities, the scatter plot highlighted potential correlations between study habits and performance, and the bar chart revealed monthly variations in sales.

Such visual representations not only enhance understanding of the data but also help in identifying key patterns, trends, and outliers. Whether for business analytics, academic insights, or research, visual tools are essential for presenting data in a meaningful way.

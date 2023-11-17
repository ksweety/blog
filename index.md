# Creating Graphs About Titanic  
The Titanic was a British passenger liner that famously sank on its maiden voyage in April 1912 after hitting an iceberg, resulting in the loss of over 1,500 lives. It remains one of the most well-known maritime disasters in history. 


---

# Create Question: What is the survival rate?
```python 
import pandas as pd 
df = pd.read_csv('titanic.csv') 
``` 
This line of code reads data from a CSV file named 'titanic.csv' using the Pandas library in Python and stores it in a DataFrame called 'df'. 

Next step 
```python 
import matplotlib.pyplot as plt
import pandas as pd
data = {'Survived': ['Died', 'Survived'],
        'YourVariable': [30, 70]}  
df = pd.DataFrame(data)

x = df['Survived']
y = df['YourVariable']

plt.bar(x, y)
plt.xlabel('Individuals', fontsize=12)
plt.ylabel('Average of them', fontsize=12)
plt.title('The Average of those that Died/Survived', fontsize=20)
plt.xticks(rotation=0)  
plt.grid(axis='y', linestyle='--', alpha=0.5)  
plt.legend(['Survival']) 
plt.show() 
``` 
This code snippet uses Matplotlib and Pandas in Python to create a bar chart illustrating the average of a variable ('YourVariable') for individuals categorized as 'Died' and 'Survived' in the 'Survived' column of a DataFrame, providing a visual representation of the average for each survival category.

<img src="blog/assets/Died&Survived.png">

Results
 
# What was the gender-based disparity in survival rates among titanic passengers? 

First Step 
```python 
import pandas as pd
import matplotlib.pyplot as plt


df = pd.read_csv('titanic.csv')


male_df = df[df['Sex'] == 'male']
female_df = df[df['Sex'] == 'female'] 
``` 
This code loads information about the Titanic passengers, and then it separates them into two groups: one for males and another for females. This makes it easy to study or visualize data specific to each gender. 

Next Step 
``` python 
survivalcount_male = male_df['Survived'].value_counts()
survivalcount_female = female_df['Survived'].value_counts() 

combined_counts = [survivalcount_male[0], survivalcount_male[1], survivalcount_female[0], survivalcount_female[1]]

labels = ['Male Died', 'Male Lived', 'Female Died', 'Female Lived']

explode = (0, 0.1, 0, 0.1)
plt.pie(combined_counts, labels=labels, explode=explode, autopct='%1.1f%%', startangle=140)
plt.axis('equal')
plt.title('Survival Percentage Among Genders')
plt.show() 
``` 
In this code snippet, we're delving into the Titanic dataset to unravel the survival dynamics between male and female passengers. First, we calculate the survival counts for both genders, breaking it down into categories of 'Died' and 'Lived.' These counts are then combined for a clear visualization using a pie chart, where each slice represents the percentage of survivors and non-survivors within each gender. The chart is designed to offer an accessible and insightful overview of survival patterns among male and female passengers aboard the Titanic. 

<img src="blog/assets/download.png"> 
 






# What was the survival rate of those who survived under 18 

First step to answering to this question 
```python
import pandas as pd
import matplotlib.pyplot as plt


df = pd.read_csv('titanic.csv')


under18 = df[df['Age'] < 18] 
``` 
In this code snippet, we leverage Pandas and Matplotlib to explore the Titanic dataset. Specifically, we read the data from a CSV file and then filter the DataFrame to include only passengers under the age of 18, laying the groundwork for an analysis focused on the younger demographic aboard the Titanic. 

Next Steps 
```python 
survival_rate = (under18['Survived'] == 1).mean()


plt.bar(['Under 18'], [survival_rate], color=['blue'])
plt.ylabel('Survival Rate')
plt.title('Survival Rate for Passengers Under 18')
plt.ylim(0, 1)  

plt.text('Under 18', survival_rate, f'{survival_rate:.2%}', ha='center', va='bottom')


plt.show() 
```  
In these lines of code, we compute the survival rate for passengers under the age of 18 in the Titanic dataset and visually represent it through a simple bar chart. The blue bar shows the survival rate, and a precise percentage label enhances the clarity of the visualization, showing the proportion of young passengers who survived the titanic. 

<img src="blog/assets/under18(1).png">  

# Obstacles 
Creating a blog post from this code might be tricky because it assumes readers have the Titanic dataset, and the code could be a bit tough for those not familiar with programming. To make it more reader-friendly, it would help to explain the purpose of the code, break down key concepts, and provide extra information on potential issues with the data. Making sure the post is clear about interpreting the visual results and giving tips for using the code in different situations would also be beneficial.
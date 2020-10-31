# Retage's Portfolio
This is my mid-term professional coding portfolio

Hi and welcome to my portfolio! I'm Retage - a 4th year Medical Sciences student at Dalhousie University. The following displays some of my coding skills so far, and I'm excited to build my knowledge in coding!

 <img src = "https://user-images.githubusercontent.com/73716282/97746793-b73e6380-1ac9-11eb-8b3b-7c5609ee974b.png" width=100>

Questions? Email me at:
[al962601@dal.ca](mailto:al962601@dal.ca)

## Skill #1 - Reading in data Files: 
A loop to read data files
Read in data:

files = glob('spid*/*_data.txt')

dataframes = [pd.read_csv(x, sep='\t') for x in files]

## Skill #2 - Data Visualization - Boxplot 
[](https://github.com/alretagealbader/RetagePortfolio/issues/3#issue-733791402)

Here is an example of code I wrote to [represent reaction time data for a Flanker Test](boxplots code.md)

### The following details some code for data visualization techniques with neural data. 


```python
# reaction times in flanker conditions
flanker_conditions_rt = df.groupby(['flankers'])[['rt']]

# creating a boxplot for analysis 
logrt_flanker.plot(kind='box')

# modifying the boxplot 
plt.title('Reaction Times in Flanker-Congruent and Flanker-Incongruent Conditions ')
plt.xlabel('Flanker Conditions')
plt.ylabel('Log RT')
plt.show() 
```


<img src = "https://user-images.githubusercontent.com/73716282/97788149-79a70c80-1b95-11eb-93e7-eda51fdff741.png" width = 700>

## Skill #3 - Data Visualization - Barplot 
In this example, I used data from the [World Happiness Report from Kaggle](https://www.kaggle.com/unsdsn/world-happiness)

I joined and presented happiness scores from the happiest and saddest countries into the following barpolot:

[](Barplot.md)
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```


```python
# Reading in the data
df = pd.read_csv('happy2019.csv')
# Subselecting the happiest and saddest countries
happy = df.head(5)
sad = df.tail(5)
all = happy.append(sad, ignore_index = True)
```


```python
# Barplot
barplot = sns.catplot(kind='bar', data= all, y='Score', x = 'Country or region')
# Modifying X-Labels to avoid overlapping country names
plt.xticks(
    rotation=45, 
    horizontalalignment='right',
    fontweight='light',
    fontsize='small'  
)
plt.show()
```




    
![png](Barplot_files/Barplot_2_0.png)
    




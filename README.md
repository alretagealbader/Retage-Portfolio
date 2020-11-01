# Retage's Portfolio

Hello and welcome to my portfolio!
I'm Retage - a 4th year Medical Sciences student at Dalhousie University. The following displays some of my coding skills so far in NESC3505, and I'm excited to keep building my knowledge in coding in the future!

 <img src = "https://user-images.githubusercontent.com/73716282/97746793-b73e6380-1ac9-11eb-8b3b-7c5609ee974b.png" width=100>

Questions? Email me at:
[al962601@dal.ca](mailto:al962601@dal.ca)

# Skills:
1. [Reading in Data Files](ReadingData.md)
2. [Data Visualization - Boxplot (neural data)](boxplots code.md)
3. [Data Visualization - Strip Plot (neural data)](stripplot.md)
4. [Data Visualization - Barplot](Barplot.md)
5. [Statistical Analysis (Correlations)](scatter.md)


## Skill #4 - Data Visualization - Barplot 
In this example, I used data from the [World Happiness Report from Kaggle](https://www.kaggle.com/unsdsn/world-happiness)

I joined and presented happiness scores from the 5 happiest and saddest countries into the following barpolot.

Here, I join the happy and sad countries together:

```python
# Reading in the data
df = pd.read_csv('happy2019.csv')
# Subselecting the happiest and saddest countries
data = df.head(5).append(df.tail(5), ignore_index = True)
```

Here, I made a few modifications to the barplot so countries' names are clearly legible. 

```python
# Barplot
barplot = sns.catplot(kind='bar', data= data, y='Score', x = 'Country or region')
# Modifying X-Labels to avoid overlapping country names
plt.xticks(
    rotation=45, 
    horizontalalignment='right',
    fontweight='light',
    fontsize='small'  
)
plt.title('Happiness Score')
plt.show()
```
<img width="400" lenght="400" alt="AllBarplots" src="https://user-images.githubusercontent.com/73716282/97790227-977c6d80-1ba5-11eb-96c5-90f26af2f618.png">

## Skill #5 - Statistical Analysis (Correlations):


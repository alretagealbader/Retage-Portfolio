# Retage's Portfolio

Hello and welcome to my portfolio!
I'm Retage - a 4th year Medical Sciences student at Dalhousie University. The following displays some of my coding skills so far in NESC3505, and I'm excited to keep building my knowledge in coding in the future!

 <img src = "https://user-images.githubusercontent.com/73716282/97746793-b73e6380-1ac9-11eb-8b3b-7c5609ee974b.png" width=100>

Questions? Email me at:
[al962601@dal.ca](mailto:al962601@dal.ca)

# Skills:
1. Reading in Data Files:
2. Data Visualization - Boxplot (neural data)
3. Data Visualization - Strip Plot (neural data)
4. Data Visualization - Barplot 
5. Statistical Analysis (Correlations)

## Skill #1 - Reading in Data Files: 
A loop to read data files:

```python
files = glob('subject*/*_data.txt')
dataframes = [pd.read_csv(x, sep='\t') for x in files]
```

## Skill #2 - Data Visualization - Boxplot 
[](https://github.com/alretagealbader/RetagePortfolio/issues/3#issue-733791402)

Here is an example of code I wrote to [represent reaction time data for a Flanker Test](boxplots code.md)

```python
# reaction times in flanker conditions
flanker_conditions_rt = df.groupby(['flankers'])[['rt']]

# creating a boxplot for analysis 
logrt_flanker.plot(kind='box')

# modifying the boxplot 
plt.title('Reaction Times in Flanker-Congruent and 
Flanker-Incongruent Conditions ')
plt.xlabel('Flanker Conditions')
plt.ylabel('Log RT')
plt.show() 
```
<img width="550" alt="barplot" src="https://user-images.githubusercontent.com/73716282/97790149-f68db280-1ba4-11eb-9eec-cb336c5f4497.png">

## Skill 3 - Data Visualization - Strip Plot
The following codes for a strip plot that visually compares the clustering of reaction times (ms) in different flanker conditions:

```python
sns.stripplot(x=df['flankers'], y=df['rt'], data= df, size=3, jitter=True)
plt.title('Reaction Times in Flankers Conditions')
plt.ylabel('Reaction Times')
plt.xlabel('Flanker Conditions')
plt.show()
```
<img width="500" alt="Striplots" src="https://user-images.githubusercontent.com/73716282/97791468-833e6d80-1bb1-11eb-9736-d691bb290d85.png">

## Skill #4 - Data Visualization - Barplot 
In this example, I used data from the [World Happiness Report from Kaggle](https://www.kaggle.com/unsdsn/world-happiness)

I joined and presented happiness scores from the 5 happiest and saddest countries into the following barpolot.

Here, I join the happy and sad countries together:

```python
# Reading in the data
df = pd.read_csv('happy2019.csv')
# Subselecting the happiest and saddest countries
data = (df.head(5)).append((df.tail(5)), ignore_index = True)
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
The following code yields the Pearson's r, Spearman's rho, and Kendall's tau correlations between Healthy Life Expectancy and Happiness scores:
```python
x = all['Healthy life expectancy']
y = all['Score']

Pearson = scipy.stats.pearsonr(x, y)    # Pearson's r
Spearman = scipy.stats.spearmanr(x, y)   # Spearman's rho
Kendall = scipy.stats.kendalltau(x, y)  # Kendall's tau

# For example:
print('The Spearmans rho correlation between countries happiness scores and 
healthy life expectancy is: ' + str(Spearman[0].round(2)) + ' at ' + str(Spearman[1].round(4)) +' significance')
>>> The Spearmans rho correlation between countries happiness scores 
and healthy life expectancy is: 0.79 at 0.0061 significance

```
The following code helps visually represent the relationship between healthy life expectancy and happiness score in all 156 countries in the dataset with a scatter plot:

```python
scatter = matplotlib.pyplot.scatter(df['Healthy life expectancy'], df['Score'])
plt.title('Healthy Life Expectancy and Happiness Score')
plt.ylabel('Happiness Score')
plt.xlabel('Healthy Life Expectancy')
plt.show()
```
<img width="500" alt="scatter" src="https://user-images.githubusercontent.com/73716282/97791505-e16b5080-1bb1-11eb-8d31-6c706ac67085.png">

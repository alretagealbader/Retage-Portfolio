
```python
# Reading in the data
df = pd.read_csv('happy2019.csv')
# Subselecting the happiest and saddest countries
happy = df.head(5)
sad = df.tail(5)
all = happy.append(sad, ignore_index = True)
```


```python
#  Making a Bar Plot using Seaborn
barplot = sns.catplot(kind='bar', data= all, y='Score', x = 'Country or region')

# Modifying the X-Labels to avoid overlapping country names
plt.xticks(
    rotation=45, 
    horizontalalignment='right',
    fontweight='light',
    fontsize='small'  
)
plt.show()
```




    
<img width="400" lenght="400" alt="AllBarplots" src="https://user-images.githubusercontent.com/73716282/97790227-977c6d80-1ba5-11eb-96c5-90f26af2f618.png">
    



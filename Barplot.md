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
    



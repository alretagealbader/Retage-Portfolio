```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import scipy.stats
```


```python
# Reading in the data
df = pd.read_csv('oacs.csv')
df.head(2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ID</th>
      <th>M/F</th>
      <th>Hand</th>
      <th>Age</th>
      <th>Educ</th>
      <th>SES</th>
      <th>MMSE</th>
      <th>CDR</th>
      <th>eTIV</th>
      <th>nWBV</th>
      <th>ASF</th>
      <th>Delay</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>OAS1_0001_MR1</td>
      <td>F</td>
      <td>R</td>
      <td>74</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>29.0</td>
      <td>0.0</td>
      <td>1344</td>
      <td>0.743</td>
      <td>1.306</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>OAS1_0002_MR1</td>
      <td>F</td>
      <td>R</td>
      <td>55</td>
      <td>4.0</td>
      <td>1.0</td>
      <td>29.0</td>
      <td>0.0</td>
      <td>1147</td>
      <td>0.810</td>
      <td>1.531</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
x = df['eTIV'] # Estimated Total Intracranial Volume
y = df['nWBV'] # Normalized Whole Brain Volume 

Pearson = scipy.stats.pearsonr(x, y)    # Pearson's r
Spearman = scipy.stats.spearmanr(x, y)   # Spearman's rho
Kendall = scipy.stats.kendalltau(x, y)  # Kendall's tau

# For example:
print('The Spearmans rho correlation between Estimated Total Intracranial Volume and Normalized Whole Brain Volume is: ' + str(Spearman[0].round(2)) + ' at ' + str(Spearman[1].round(2)) +' significance')

```

    The Spearmans rho correlation between Estimated Total Intracranial Volume and Normalized Whole Brain Volume is: 0.03 at 0.49 significance


Here, I use Seaborn to create a scatter plot to visually represent the relationship between Estimated Total Intracranial Volume and Normalized Whole Brain Volume


```python
# Creating a Scatter Plot
scatter = matplotlib.pyplot.scatter(x, y)
plt.title('Brain Volume in Alzheimers Patients')
plt.ylabel('Normalized Whole Brain Volume')
plt.xlabel('Estimated Total Intracranial Volume')
plt.show()
```




    
![png](azl_files/azl_4_0.png)
    




```python

```

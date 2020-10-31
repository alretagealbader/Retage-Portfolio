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


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-1-78e21bbaf664> in <module>
          1 # reaction times in flanker conditions
    ----> 2 flanker_conditions_rt = df.groupby(['flankers'])[['rt']]
          3 
          4 # creating a boxplot for analysis
          5 logrt_flanker.plot(kind='box')


    NameError: name 'df' is not defined



```python

```

## Skill #2 - Data Visualization - Boxplot (neural data)

The following is some code that generates a boxplot to visualize neural data from a Flanker Task.

```python
# reaction times in flanker conditions
flanker_conditions_rt = df.groupby(['flankers'])[['rt']]

# creating a boxplot for analysis 
logrt_flanker.plot(kind='box')

# modifying the boxplot 
plt.title('Reaction Times in Flanker-Congruent and Flanker-Incongruent Conditions')
plt.xlabel('Flanker Conditions')
plt.ylabel('Log RT')
plt.show() 
```

<img width="550" alt="barplot" src="https://user-images.githubusercontent.com/73716282/97790149-f68db280-1ba4-11eb-9eec-cb336c5f4497.png">

## Skill #2 - Data Visualization - Boxplot (neural data)

The following is some code that generates a boxplot to visualize neural data from a Flanker Task.

Specifically, this allows me to visually see the difference in logarithmic reaction times ('rt') in congruent and incongruent flanker conditions. A Flanker Test is a common test used in cognitive psychology. In congruent conditions, flankers/arrows are all pointing in the same direction; in the flanker incongruent condition, the target arrow is surrounded by incongruent flanker arrows, pointing in the opposite direction. 

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

The plot allows me to observe that the reaction times' median in flanker incongruent conditions is larger/slower than congruent conditions.

[Go to Skill #1](https://alretagealbader.github.io/RetagePortfolio/ReadingData.html)

[Go to Skill #3](https://alretagealbader.github.io/RetagePortfolio/stripplot.html)
 
[Go to Main Page](https://alretagealbader.github.io/RetagePortfolio/)

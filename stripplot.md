## Skill #3 - Data Visualization - Strip Plot (neural data)

The following codes for a strip plot that visually compares the clustering of reaction times (ms) in different flanker conditions:

```python
# Making a Strip Plot for Conditions in a Flanker Task using Seaborn
sns.stripplot(x=df['flankers'], y=df['rt'], data= df, size=3, jitter=True)

# Modifying the Strip Plot
plt.title('Reaction Times in Flankers Conditions')
plt.ylabel('Reaction Times')
plt.xlabel('Flanker Conditions')
plt.show()
```

<img width="500" alt="Striplots" src="https://user-images.githubusercontent.com/73716282/97791468-833e6d80-1bb1-11eb-9736-d691bb290d85.png">

[Go to Skill #2](https://alretagealbader.github.io/RetagePortfolio/boxplots%20code.html)

[Go to Skill #4](https://alretagealbader.github.io/RetagePortfolio/Barplot.html)
 

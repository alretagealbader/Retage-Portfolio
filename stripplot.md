```python
# Making a Strip Plot for Conditions in a Flanker Task using Seaborn
sns.stripplot(x=df['flankers'], y=df['rt'], data= df, size=3, jitter=True)

# Modifying the Strip Plot
plt.title('Reaction Times in Flankers Conditions')
plt.ylabel('Reaction Times')
plt.xlabel('Flanker Conditions')
plt.show()
```

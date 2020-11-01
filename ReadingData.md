## Skill #1 - Reading in Data Files 


Here is some code I used to help read in multiple data files all starting with 'subject' and ending with 'data.txt'.
```python
#Read in Data
files = glob('subject*/*_data.txt')
dataframes = [pd.read_csv(x, sep='\t') for x in files]
```

(Developed with Jillian Fennell)

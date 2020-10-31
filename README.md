# Retage's Portfolio
This is my mid-term professional coding portfolio

Hi and welcome to my portfolio! I'm Retage - a 4th year Medical Sciences student at Dalhousie University. The following displays some of my coding skills so far, and I'm excited to build my knowledge in coding!

 <img src = "https://user-images.githubusercontent.com/73716282/97746793-b73e6380-1ac9-11eb-8b3b-7c5609ee974b.png" width=100>

Questions? Email me at:
[al962601@dal.ca](mailto:al962601@dal.ca)

## A loop to read data files
Read in data:

files = glob('spid*/*_data.txt')

dataframes = [pd.read_csv(x, sep='\t') for x in files]

## Creating a boxplot from neural data: Flanker test

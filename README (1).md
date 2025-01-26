# Project Overview

This project is based on a Jupyter Notebook, detailing the following:

### Section 1: Markdown
#NAME       JAHANZAIB ZAFAR#ROLL NO:       125...

### Section 2: Code
```python
import pandas as pd
```

### Section 3: Markdown
#DATA LOADING  we load data by using pd.read_csv()...

### Section 4: Code
```python
zz=pd.read_csv("C:\\Users\\hp\\Documents\\internet project\\internet_users .csv")
```

### Section 5: Markdown
#now we check           is our data load or not ?...

### Section 6: Code
```python
zz.shape
```

### Section 7: Markdown
#we use head method that give first five rows and then tail method which give ending five rows...

### Section 8: Code
```python
zz.head()
```

### Section 9: Code
```python
zz.tail()
```

### Section 10: Markdown
#DATA CLEANING#IN which we clean the data by using isnull().sum() method and then fill by using fillna()...

### Section 11: Code
```python
zz.isnull().sum()
```

### Section 12: Markdown
#since many rows are uncomplete ,we complete by using fillna method ...

### Section 13: Code
```python
zz.fillna(100,inplace=True)
```

### Section 14: Markdown
#now we see no rows are null.we use inplace=true for frequently written....

### Section 15: Code
```python
zz.isnull().sum()
```

### Section 16: Markdown
#duplicate values remove ...

### Section 17: Code
```python
print(zz.duplicated())
```

### Section 18: Code
```python
zz.drop_duplicates()
```

### Section 19: Markdown
#DATA PREPROCESSING IN which we rename the columns , ...

### Section 20: Code
```python
zz.columns
```

### Section 21: Code
```python
zz.rename(columns={"Rate (WB)":"Rate","Notes":"Note"},inplace=True)
```

### Section 22: Code
```python
zz.columns
```

### Section 23: Markdown
#Data aggregation in which we see the mean ,mode ,meddian and plot graph ...

### Section 24: Code
```python
zz.info()
```

### Section 25: Code
```python
zz["Rate"].mean()
```

### Section 26: Code
```python
zz["Rate"].mode()
```

### Section 27: Code
```python
zz["Rate"].median()
```

### Section 28: Code
```python
zz["Year"].value_counts()
```

### Section 29: Markdown
#DATA VISUALIZATIONMEAN creating a graphical or visual representation of something to understand or explain it better...

### Section 30: Code
```python
zz["Year"].value_counts().plot(kind="bar")
```

### Section 31: Code
```python
zz["Year"].value_counts().plot(kind="barh")
```

### Section 32: Code
```python
zz["Year"].value_counts().plot(kind="box")
```

### Section 33: Code
```python
zz["Year"].value_counts().plot(kind="kde")
```

### Section 34: Code
```python
zz["Year"].value_counts().plot(kind="hist")
```

### Section 35: Code
```python
zz["Year"].value_counts().plot(kind="line")
```

### Section 36: Code
```python
zz["Year"].value_counts().plot(kind="pie")
```

### Section 37: Markdown
...

### Section 38: Code
```python

```

### Section 39: Markdown
#DATAFRAME...

### Section 40: Code
```python
zz.columns
```

### Section 41: Code
```python
a=pd.DataFrame({    "Rate":4,    "Year":5,
```

### Section 42: Code
```python
zz=pd.concat([a,zz])
```

### Section 43: Code
```python
zz
```

### Section 44: Markdown
row deletion in dataframe ...

### Section 45: Code
```python
zz.drop(0,inplace=True)zz
```

### Section 46: Markdown
#slicing...

### Section 47: Code
```python
zz[2:8]
```

### Section 48: Code
```python
zz[2:8:2]
```

### Section 49: Markdown
#Data save ...

### Section 50: Code
```python
pip install openpyxl
```

### Section 51: Code
```python
zz=pd.read_csv("internet_users .csv")zzzz.to_excel("internet_users.xlsx",
```

## Instructions

To use this notebook, you need to have the following installed:

- Python (3.x)
- Jupyter Notebook or JupyterLab
- Required libraries listed in the notebook

## Usage

1. Open the notebook in Jupyter.
2. Execute the cells in order to reproduce the analysis or results.

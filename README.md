## Complete Code

```python
# Importing necessary library
import pandas as pd

# Loading data
zz = pd.read_csv("C:\\Users\\hp\\Documents\\internet project\\internet_users.csv")

# Checking if data is loaded correctly
zz.shape
zz.head()
zz.tail()

# Data Cleaning
zz.isnull().sum()  # Checking for null values
zz.fillna(100, inplace=True)  # Filling null values
zz.isnull().sum()  # Verifying no null values remain

# Removing duplicate values
print(zz.duplicated())
zz.drop_duplicates(inplace=True)

# Data Preprocessing
zz.columns  # Displaying column names
zz.rename(columns={"Rate (WB)": "Rate", "Notes": "Note"}, inplace=True)
zz.columns  # Verifying updated column names

# Data Aggregation
zz.info()  # General information about the dataset
zz["Rate"].mean()  # Calculating mean
zz["Rate"].mode()  # Calculating mode
zz["Rate"].median()  # Calculating median
zz["Year"].value_counts()  # Counting values in 'Year'

# Data Visualization
zz["Year"].value_counts().plot(kind="bar")  # Bar chart
zz["Year"].value_counts().plot(kind="barh")  # Horizontal bar chart
zz["Year"].value_counts().plot(kind="box")  # Box plot
zz["Year"].value_counts().plot(kind="kde")  # KDE plot
zz["Year"].value_counts().plot(kind="hist")  # Histogram
zz["Year"].value_counts().plot(kind="line")  # Line plot
zz["Year"].value_counts().plot(kind="pie")  # Pie chart

# DataFrame manipulations
zz.columns  # Checking columns
a = pd.DataFrame({"Rate": [4], "Year": [5]})
zz = pd.concat([a, zz])  # Adding rows
zz.drop(0, inplace=True)  # Deleting a row

# Slicing
zz[2:8]  # Slicing rows
zz[2:8:2]  # Slicing with step

# Saving Data
pip install openpyxl  # Installing dependency
zz.to_excel("internet_users.xlsx")  # Saving data to an Excel file

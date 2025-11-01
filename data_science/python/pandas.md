https://pandas.pydata.org/

Known for DataFrame type that represents tabular data (such as a spreadsheet).

https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html


### Loading a CSV

``` python
import pandas as pd

df = pd.read_csv("<file_path>")
```

https://pandas.pydata.org/docs/reference/api/pandas.read_csv.html#pandas.read_csv

### Inspecting a DataFrame
#### View DataFrame Information

``` python
import pandas as pd

df = pd.read_csv("data.txt")
df.info()
print(df.info())
```

This displays data like:

``` bash
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 104 entries, 0 to 103
Data columns (total 5 columns):
 #   Column    Non-Null Count  Dtype  
---  ------    --------------  -----  
 0   suspect   104 non-null    object 
 1   location  104 non-null    object 
 2   date      104 non-null    object 
 3   item      104 non-null    object 
 4   price     104 non-null    float64
dtypes: float64(1), object(4)
memory usage: 4.2+ KB
```

#### View Top n Rows
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.head.html

``` python
import pandas as pd

n = 5

df = pd.read_csv("data.txt")
df.head(n)
print(df.head(n))
```

5 is the default if no value is provided.

### Column Selection
#### Bracket Notation
``` python
import pandas as pd

df = pd.read_csv("data.txt")    # assumes there is a file called "data.txt"
items = df["items"]             # assumes there is a column named "items"
```

#### Dot Notation
- requires attributes that are valid python variable names

``` python
import pandas as pd

df = pd.read_csv("data.txt")
items = df.items
```

### Row Selection
Logical statements can be used to select rows. Here are some examples:

``` python
import pandas as pd

df = pd.read_csv("data.txt")
high_price_rows = df[df.price > 1000]               # selects all rows where df.price > 1000
target_name_rows = df[df.name == "John Smith"]      # selects all rows where df.name  is "John Smith"
```
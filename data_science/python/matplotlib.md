https://matplotlib.org/



### Line Plots
Great for viewing ordered data (hours/day, etc.)

Basic line plot:

``` python
from matplotlib import pyplot as plt

plt.plot(data1.x_values, data1.y_values, label="Data 1")
plt.plot(data2.x_values, data2.y_values, label="Data 2")        # not required, just showing that its possible
plt.legend()                                                    # not required, shows labels if provided

plt.show()
```

### Scatter Plots
Good for viewing unordered (or maybe less ordered) data, such as height vs. age.

Basic scatter plot:

``` python
from matplotlib import pylot as plt

plt.scatter()
```

### Bar Chart
Comparison of categorical data.

Basic
``` python

plt.bar()

```

Horizontal


Stacked


### Histogram
Data placed into bins and counts the number of values in a given bin (category).

``` python

plt.hist()

```

Normalization is an important topic. Return to this. But a matplotlib helper:

``` python

plt.hist(df.column_1, density=True)
plt.hist(df.column_2, density=True)

```
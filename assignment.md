# Assignment

## Brief

Write the Python codes for the following questions.

## Instructions

Paste the answer as Python in the answer code section below each question.

### Question 1

Question: How do you create a 2x2 subplot grid in matplotlib and select the first subplot?

Answer:

```python
import matplotlib.pyplot as plt

fig, axes = plt.subplots(nrows=2, ncols=2)
ax1 = axes[0, 0]
ax1.set_title('First Subplot (0, 0)')
plt.tight_layout()
plt.show()
```

### Question 2

Question: How to plot a line and set the color to red and style to dash in a matplotlib plot?

```python
x = [1, 2, 3, 4]
y = [1, 4, 9, 16]
```

Answer:

```python
plt.plot(
    x,
    y,
    color='red',      # Sets the color to red
    linestyle='--'    # Sets the line style to dashed
)
```

### Question 3

Question: How to plot a histogram with 30 bins for `data` in matplotlib?

```python
data = np.random.randn(1000)
```

Answer:

```python
plt.hist(
    data,
    bins=30,      # <-- This sets the number of bins to 30
    edgecolor='black',
    alpha=0.7,
    color='skyblue'
)
```

### Question 4

Question: How can you set the x-axis and y-axis labels in a matplotlib plot?

Answer:

```python
import matplotlib.pyplot as plt
import numpy as np

data = np.random.randn(1000)

plt.hist(
    data,
    bins=30,      # <-- This sets the number of bins to 30
    edgecolor='black',
    alpha=0.7,
    color='skyblue'
)
plt.title('Histogram of Standard Normal Data ($\mu=0, \sigma=1$) with 30 Bins', fontsize=14)
plt.xlabel('Value', fontsize=12)
plt.ylabel('Frequency', fontsize=12)
plt.grid(axis='y', linestyle='--', alpha=0.6)

# Display the plot
plt.show()
```

### Question 5

Question: How do you create a bar plot in seaborn using the `tips` dataset to show the average tip amount per day?

```python
import seaborn as sns
tips = sns.load_dataset('tips')
```

Answer:

```python
plt.figure(figsize=(8, 6))
sns.barplot(
    data=tips,
    x='day',           
    y='tip',           
    estimator='mean',   
    errorbar='sd',      
    palette='viridis'   
)
```

### Question 6

Question: How to create a box plot for total_bill categorized by day in the `tips` dataset using seaborn?

Answer:

```python
plt.figure(figsize=(10, 6))
sns.boxplot(
    x='day',            
    y='total_bill',     
    data=tips,          
    palette='Set2'      
)
```

## Submission

- Submit the URL of the GitHub Repository that contains your work to NTU black board.
- Should you reference the work of your classmate(s) or online resources, give them credit by adding either the name of your classmate or URL.

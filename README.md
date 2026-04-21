# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

```
from matplotlib import pyplot as plt
import pandas as pd

# Load dataset
df = pd.read_csv("/content/County_Health_Rankings.csv")

# Display first few rows
display(df.head())

# Group data by 'Year span' and sum 'Raw value' for time series analysis
df_yearly_sales = df.groupby('Year span')['Raw value'].sum().reset_index()

# Plot the data
plt.figure(figsize=(12, 6))
plt.plot(df_yearly_sales['Year span'], df_yearly_sales['Raw value'], label='Total Raw Value', color='blue', marker='o')

plt.title('Time Series Plot of Total Raw Value by Year Span')
plt.xlabel('Year span')
plt.ylabel('Raw value')
plt.legend()
plt.grid(True)
plt.xticks(df_yearly_sales['Year span'].unique(), rotation=45)

# Show plot
plt.tight_layout()
plt.show()
```


# OUTPUT:
<img width="1484" height="661" alt="image" src="https://github.com/user-attachments/assets/f9c94a38-ed4e-4818-9af7-8244e4c8990d" />



# RESULT:
Thus we have created the python code for plotting the time series of given data.

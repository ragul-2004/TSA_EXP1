###  Developed by : Ragul A C
###  Register no: 212221240042
###  Date:

## Ex.No: 01A PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data that measures Total revenue of mobile sales.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to monthly sales.
5. Display the graph.
# PROGRAM:
~~~
import pandas as pd
import matplotlib.pyplot as plt

# Load the CSV file
file_path = '/content/mobile_sales.csv'
data = pd.read_csv(file_path)

# Convert the 'Date' column to datetime format
data['Date'] = pd.to_datetime(data['Date'])

# Group by date and sum the total revenue
revenue_per_day = data.groupby('Date')['TotalRevenue'].sum()

# Plot the time series
plt.figure(figsize=(12, 6))
plt.plot(revenue_per_day, marker='o')
plt.title('Total Revenue Over Time')
plt.xlabel('Date')
plt.ylabel('Total Revenue')
plt.grid(True)
plt.show()
~~~
# OUTPUT:
![output](https://github.com/user-attachments/assets/2c7d6754-1027-4839-b6cc-d93bb2435c78)

# RESULT:
Thus we have created the python code for plotting the time series of mobile sales.

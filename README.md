# codetech_powerbi_task_2.4

Name:Parth Deorukhkar

Company:CODETECH IT SOLLUTION

ID:CT08EIB

Domain:POWER BI

Duration:Dec17 to Jan 17

Mentor:Neela Santosh Kumar
Project Title: Advanced Data Analysis and Visualization in Power BI using Python and R


---

Overview

This project demonstrates the integration of Python and R scripts within Power BI to perform advanced data analysis and create dynamic visualizations. The dataset used contains sales data across cities and states, enabling detailed insights into sales performance.


---

Files Included

1. Power BI Report (.pbix): The main report file showcasing:

Python visualizations (Sales by City).

R visualizations (Sales Trend Over Time).

Standard Power BI visuals (Total Sales, Sales by State, etc.).



2. Sample Dataset (CSV): Fake sales data used in the report.


3. README (This File): Instructions to reproduce the project.




---

Prerequisites

1. Power BI Desktop (Latest Version).


2. Python Installed:

Recommended: Python 3.x.

Required Libraries:

pandas

matplotlib

seaborn




3. R Installed:

Recommended: R 4.x.

Required Packages:

ggplot2






---

Dataset Structure

The dataset includes the following columns:

Product Name: Name of the product.

City: City where the product was sold.

State: State where the product was sold.

Sale Amount: Total sales amount for the product.

Date: Date of the transaction.


Sample Data:


---

Steps to Reproduce

1. Set Up Python in Power BI

Go to File > Options and Settings > Options.

Navigate to Python Scripting under Global settings.

Set the Python environment path (e.g., C:\Python3\python.exe).


2. Set Up R in Power BI

Go to File > Options and Settings > Options.

Navigate to R Scripting under Global settings.

Set the R environment path (e.g., C:\Program Files\R\R-4.x.x\bin\R.exe).


3. Load the Dataset

Import the provided CSV file into Power BI.

Rename the table to Sales Data for consistency.


4. Create Python Visuals

Add a Python Visual to the report.

Drag fields into the Values pane (e.g., City, Sale Amount).

Use the following Python script:

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load data from Power BI
dataset = dataset

# Group data by city and calculate total sales
city_sales = dataset.groupby('City', as_index=False)['Sale Amount'].sum()

# Create a bar plot for sales by city
plt.figure(figsize=(10, 6))
sns.barplot(data=city_sales, x='City', y='Sale Amount', palette='viridis')
plt.title('Total Sales by City')
plt.xticks(rotation=45)
plt.xlabel('City')
plt.ylabel('Total Sales')
plt.tight_layout()
plt.show()


5. Create R Visuals

Add an R Visual to the report.

Drag fields into the Values pane (e.g., Date, Sale Amount).

Use the following R script:

library(ggplot2)

# Load dataset from Power BI
dataset <- dataset

# Create a time-series plot for sales
ggplot(data=dataset, aes(x=Date, y=`Sale Amount`)) +
  geom_line(color='blue', size=1) +
  labs(title="Sales Trend Over Time", x="Date", y="Sales Amount") +
  theme_minimal()



---

Key Features in the Report

1. Python Visualizations:

Sales by City: Bar plot using Python and Seaborn.



2. R Visualizations:

Sales Trend: Line chart using R and ggplot2.



3. Standard Power BI Visuals:

Total Sales.

Sales by State (Bar Chart).

Sales over Time (Line Chart).





---

How to Use the Report

1. Open the Power BI file in Power BI Desktop.


2. Ensure Python and R are installed and configured in Power BI settings.


3. Refresh the dataset to update visuals.


4. Use slicers to filter data by Product, City, or State.




---

Conclusion

This report showcases the seamless integration of Python and R in Power BI to enhance analytical capabilities. By leveraging Python and R scripts, users can create advanced, customized visualizations that go beyond native Power BI features.

Feel free to extend the scripts or visuals for more complex analyses!

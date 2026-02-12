#  Sales Data Analysis Dashboard (Python)

##  Project Overview
This project analyzes company sales data using Python and popular data analysis libraries. It helps in understanding sales performance, identifying top products, and visualizing trends through graphs.

---

## Technologies Used
- Python  
- Pandas  
- Matplotlib  
- Seaborn  

---

##  Dataset Details
The dataset includes sales records with the following fields:
- **Date** – Date of sale  
- **Product** – Product name  
- **Region** – Sales region  
- **Sales** – Sales amount  

---

##  Key Features
✔ Calculate **Total Sales Revenue**  
✔ Identify **Best Selling Product**  
✔ Analyze **Monthly Sales Trends**  
✔ Compare **Sales by Region** using charts  

---

##  Visualizations
 Line chart showing monthly sales trend  
 Bar chart showing region-wise sales performance  

---

##  How to Run

1. Install required libraries:
   ```bash
   pip install pandas matplotlib seaborn
   import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load data
data = pd.read_csv("sales_data.csv")

# Convert Date column to datetime
data["Date"] = pd.to_datetime(data["Date"])

# Total Sales
total_sales = data["Sales"].sum()
print("Total Sales:", total_sales)

# Best Selling Product
best_product = data.groupby("Product")["Sales"].sum().idxmax()
print("Best Selling Product:", best_product)

# Monthly Sales Trend
data["Month"] = data["Date"].dt.month
monthly_sales = data.groupby("Month")["Sales"].sum()

print("\nMonthly Sales:\n", monthly_sales)

# Plot Monthly Sales Trend
plt.figure()
monthly_sales.plot(kind="line", marker="o")
plt.title("Monthly Sales Trend")
plt.xlabel("Month")
plt.ylabel("Sales")
plt.show()

# Sales by Region (Bar Chart)
plt.figure()
sns.barplot(x="Region", y="Sales", data=data)
plt.title("Sales by Region")
plt.show()

2.Run the Python notebook or script to see analysis and graphs.
Project Outcome

This project demonstrates practical skills in:

Data analysis

Business insight generation

Data visualization using Python

👩‍💻 Created by: Vaibhavi Kokadwar
🎓 MCA Student | Aspiring Python Developer

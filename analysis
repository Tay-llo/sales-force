import csv
from csv import DictReader
from typing import List, Dict
# Read the data from the spreadsheet

data: List[Dict[str, str]] = []
with open('sales.csv', 'r')as sales_csv:
    reader: DictReader = csv.DictReader(sales_csv)
    for row in reader:
        data.append(row)


# Collect all the sales from each month into a single list

    sales_data = [int(row['sales']) for row in data]
    print('sales_data', sales_data)

# Calculate monthly changes as percentages

    monthly_changes = [0]
    for i in range(1, len(sales_data)):
        change = ((sales_data[i]-sales_data[i-1])/sales_data[i-1])*100
        monthly_changes.append(change)

# Output the total sales across all months

    total_sales = sum(sales_data)
    print("Total Sales across all months:", total_sales)

# Calculate and output the average sales

    average_sales = sum(sales_data)
    print("Average sales per month:", average_sales)

# Find the month with the highest sales

    max_sales_month = max(data, key=lambda x: int(x['sales']))['month']
    print("Month with the highest sales:", max_sales_month)

# Find the month with the lowest sales

    min_sales_month = min(data, key=lambda x: int(x['sales']))['month']
    print("Month with the lowest sales:", min_sales_month)


# Output the monthly changes as percentages

    for i, month in enumerate(data):
        print(f"percentage change for {month['month']}: {monthly_changes[i]:.2f}%")

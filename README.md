Exp-No---4--Yearly-Revenue-Growth-Visualization-Using-Matplotlib





Aim:



To visualize the yearly trend of company revenue and expenses using Matplotlib by plotting multiple line charts with labels, legends, grids, and annotations.




Algorithm:





1. Import Libraries – Import matplotlib.pyplot and numpy for visualization and numeric support.
2. Create Dataset – Define lists for Years, Revenue, and Expenses.
3. Plot Graphs:
   - Plot Revenue as a solid line.
   - Plot Expenses as a dashed line.
4. Add Titles and Labels – Use plt.title(), plt.xlabel(), and plt.ylabel().
5. Add Legends and Grid – Use plt.legend() and plt.grid(True) to make the chart clear.
6. Annotate Key Points – Highlight the highest revenue and expense years using annotations.
7. Display Plot – Use plt.show() to render the visualization.

Program:

  # Company Revenue and Expense Visualization using Matplotlib

import matplotlib.pyplot as plt

import numpy as np

# Step 1: Create dataset

years = np.arange(2017, 2024)

revenue = [20, 25, 28, 35, 40, 45, 52]  # in lakhs

expenses = [15, 18, 22, 27, 30, 33, 38]  # in lakhs

# Step 2: Plot Revenue and Expenses

plt.figure(figsize=(8,5))

plt.plot(years, revenue, marker='o', color='green',
         linewidth=2, label='Revenue')

plt.plot(years, expenses, marker='s', color='red',
         linestyle='--', linewidth=2, label='Expenses')

# Step 3: Add titles, labels, and grid

plt.title("Company Revenue and Expense Trends (2017 - 2023)",
          fontsize=13, fontweight="bold")

plt.xlabel("Year", fontsize=11)

plt.ylabel("Amount (in Lakhs)", fontsize=11)

plt.grid(True, linestyle='--', alpha=0.6)

# Step 4: Add legend

plt.legend(loc='upper left')

# Step 5: Annotate highest revenue and expense

max_rev_index = np.argmax(revenue)

max_exp_index = np.argmax(expenses)

plt.annotate(f"Highest Revenue: {revenue[max_rev_index]}L",
             xy=(years[max_rev_index], revenue[max_rev_index]),
             xytext=(years[max_rev_index]-0.5,
                     revenue[max_rev_index]+2),
             arrowprops=dict(facecolor='black', arrowstyle='->'))

plt.annotate(f"Highest Expense: {expenses[max_exp_index]}L",
             xy=(years[max_exp_index], expenses[max_exp_index]),
             xytext=(years[max_exp_index]-0.5,
                     expenses[max_exp_index]+2),
             arrowprops=dict(facecolor='black', arrowstyle='->'))

# Step 6: Show plot

plt.tight_layout()

plt.show()







#Output:



 <img width="821" height="496" alt="Screenshot 2026-11-20 111322" src="https://github.com/user-attachments/assets/314bf6d4-bd83-4089-98f8-940a0208faaa" />








Result:



The program successfully created datasets for yearly company Revenue and Expenses, and plotted them using Matplotlib line charts.

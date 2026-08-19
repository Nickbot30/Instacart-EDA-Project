# Instacart-EDA-Project
Instacart Market Basket Analysis — Exploratory Data Analysis (EDA)

⭐ Project Overview
This project explores customer purchasing behavior using the Instacart Market Basket dataset, a large collection of grocery orders.
The goal is to understand:
When customers shop
How often they reorder
What products are most popular
How many items customers typically buy
Patterns across days, hours, and user behavior
This EDA demonstrates your ability to work with large datasets, perform data cleaning, and extract meaningful insights using Python and Pandas.

📘 Dataset Description
The project uses five datasets:
orders — order metadata (time, user, order number)
order_products — products included in each order
products — product names and IDs
departments — department categories
aisles — aisle categories
These datasets contain millions of rows, making this a strong demonstration of your ability to handle large-scale data.

🧹 Data Cleaning
Several issues were identified and resolved:
1. Missing Values
product_name had 1,258 missing values
All missing names occurred in aisle 100 and department 21
Missing names were replaced with "unknown"
2. Missing add_to_cart_order Values
836 rows had missing values
All missing values occurred for items placed 65th or later in the cart
Replaced missing values with 999 (code for “unknown order position”)
Converted column to integer type
3. Duplicate Rows
orders contained 15 duplicate rows
All duplicates were removed
Other datasets had no full-row duplicates
4. Duplicate Product Names
1,257 duplicate product names (case-insensitive)
Cleaned using .drop_duplicates()
This cleaning ensures accurate analysis and prevents misleading results.

🔍 Exploratory Data Analysis
1. When do people shop?
Customers shop most frequently between 9 AM and 5 PM, with peaks at:
10 AM
3 PM
This aligns with typical grocery shopping behavior.
2. What days are most popular?
Assuming Sunday = 0:
Sunday and Monday have the highest order volume
Midweek (Wed–Fri) sees lower activity
3. How long do people wait between orders?
Most customers reorder within 2–10 days, with:
A major spike at 7 days (weekly shopping)
Smaller spikes at 14, 21, and 28 days (biweekly or monthly patterns)
A large spike at 30 days, possibly due to subscription or monthly auto-orders
4. Wednesday vs Saturday Shopping Patterns
Comparing hourly order distribution:
Saturday has consistently higher order volume
Wednesday shows a dip between 11 AM–1 PM, possibly due to lunch breaks
5. How many orders do customers place?
Most customers place 1–10 orders total.
Only a small number of customers place more than 20 orders, indicating:
Many one-time or infrequent users
A smaller group of loyal repeat customers
6. What are the top 20 most popular products?
All top products are produce, except for milk:
Bananas
Organic Bananas
Organic Strawberries
Organic Baby Spinach
Organic Hass Avocado
… and more
This suggests Instacart users prioritize fresh produce.
7. How many items do people buy per order?
Most orders contain 5–6 items, with the majority falling between 1–20 items.
A few orders contain 100+ items, but these are rare outliers.
8. What items are reordered most often?
Reordered items indicate customer loyalty and repeat purchasing behavior.
Top reordered items include:
Bananas
Organic Strawberries
Organic Whole Milk
Organic Raspberries
Produce dominates again, showing strong repeat demand.

🛠️ Tools & Technologies
Python
Pandas
Matplotlib
Jupyter Notebook

📂 Project Structure
Code
instacart-eda/
    ├── instacart_analysis.ipynb
    ├── README.md
    ├── data/ (optional)
    
⭐ Key Skills Demonstrated
Large-scale data cleaning
Handling missing values
Duplicate detection and removal
Grouping and aggregation
Data visualization
Customer behavior analysis
Product-level insights
Working with multi-table relational datasets

▶️ How to Run
Clone the repository
Open the notebook in Jupyter or VS Code
Ensure datasets are placed in the correct directory
Run all cells sequentially

⭐ Future Improvements
Add heatmaps for hour/day combinations
Build a dashboard (Tableau or Power BI)
Perform association rule mining (Apriori)
Predict reorder probability using ML

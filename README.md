## **Sales Analysis (Python & Pandas)**  
- **Business Problem:** A company needs their sales data analysed to to uncover trends, patterns, and key insights.
- **How I plan to solve the problem**: I plan to use python to analyse their sales data by identifying the best-selling products, seasonal trends, and more.
- I will need to:
  - Import sales data
  - Ensure data is clean before analysis
  - Clear Documentation: The python notebook will have comments describing functionality and purpose for readability
  - Analyse the data and answer questions.
 
## Explanation of python code used to solve the problem
**Setup**
1) Import the data: The dataset consists of multiple csv files that contain data for different months of the year.
  - For analysis these files needed to be consolidated into one file.
  - To do this I wrote code to list all the files in the folder containing csv files
  - Appended the contents of each csv file one by one into a empty list (Lists can store dataframes).
  - Combine the data so all rows from each CSV file are merged into one DataFrame, instead of being stored separately in a list.

2) Clean the data:
  - Inspected the data and then carried out the following:
  - Removed Null values,
  - Corrected Incorrect data types
  - Derived a new column by using string parsing to extract the city from each address.
    - I did this by getting making a function the second element after splitting the address with "split".
    - Afterwards used that function with "apply" to use on a column and create a new column.

**Analysis**

After everything is setup, I started my analysis, asking key questions about the sales data.

1) What month was best for sales? How much was earned
  - I created two columns, month and total sales
  - Used groupby and aggregate functions to get total sales for each month
  - Used seaborn to turn it into a visualisation for readability against total sales

2) Which city had the highest number of sales
  - Grouped data by city's
  - Used seaborn to turn it into a visualisation for readability against total sales

3) At what time of day are customers most likely to make a purchase, indicating the optimal window for ad placement?
- Grouped data by hour
- Used seaborn to turn it into a visualisation for readability against total sales

4) What products are sold together the most? (Pairs)
This question was challenging to answer it I...
- Filtered orders to retain only those with duplicate Order IDs, indicating that multiple items were purchased together in a single transaction.

- Created a new column (Grouped) that aggregated all products associated with the same Order ID, effectively capturing the list of items per order.

- Removed duplicate combinations of Order ID and grouped products to avoid redundancy.

- Applied the combinations function to generate all possible product pairs within each grouped order.

- Used Python’s Counter from the collections module, to count the frequency of each pair and identify the most commonly purchased product combinations.

5) Which product produced the most revenue?
- Grouped the data by product and used aggregate functions to calculate total revenue for each item.
- Visualized the results to make patterns more interpretable and highlight top-performing products.
- Identified a correlation between high-revenue products and their higher unit prices, suggesting that cost per item was a key factor driving total revenue.

## 🛠️ Tech Stack
- **Tools Used:** Python (Pandas, Matplotlib, Seaborn)  
- **Details:** Check out the full analysis in the PDF: *Sales Analysis.pdf*. 💼

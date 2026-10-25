Customer Shopping Behavior Analysis
Project Overview
This project explores customer shopping behavior using Python. The analysis uses 3,900 retail purchase records to examine which product categories generate the most revenue, how purchases vary by customer demographics and season, and whether discounts or subscriptions are associated with different spending patterns.

Tools used: Python, Pandas, NumPy, Matplotlib, Google Colab
Dataset size: 3,900 rows
Business Problem
A retail store wants to understand its customers and sales patterns: what customers buy, which groups contribute the most recorded revenue, and where the business could focus its marketing and customer-retention efforts.
Business Questions
- Which product categories and individual items generate the most revenue?
- How does revenue vary by gender and age group?
- Which seasons and states contribute the most revenue?
- Are average purchase amounts different when discounts are applied?
- Do subscribed customers spend differently from non-subscribers?
- Which payment methods and shipping types are most commonly used?
- How do previous purchases vary by purchase frequency?
Analysis Workflow
1. Load the CSV data using Pandas.
2. Inspect sample rows, dataset dimensions, data types, summary statistics, missing values, and duplicates.
3. Standardize column names to lowercase snake_case.
4. Create an age-group field and a flag for review ratings of 4 or higher.
5. Compare revenue using grouping, aggregation, sorting, and value counts.
6. Create Matplotlib charts for revenue by category, season, age group, gender, state, and item, plus payment and shipping counts.
7. Summarize the findings and possible business actions.
Key Findings
- Clothing is the largest category: $104,264, about 45% of the total recorded purchase amount of $233,081.
- Accessories is second: $74,200. Clothing and Accessories together account for about 77% of recorded purchase revenue.
- Revenue is fairly similar across seasons: Fall is highest at $60,018 and Summer lowest at $55,777.
- Recorded revenue by gender: Male customers account for $157,890, compared with $75,191 for female customers. This is a total-revenue difference; it does not by itself show that an individual male customer spends more.
- Top states are close together: Montana is highest among the listed states at $5,784, followed by Illinois at $5,617 and California at $5,605.
- Top individual items are close together: Blouse generated $10,410, Shirt $10,332, and Dress $10,320.
- Average purchase amount is slightly lower for discounted records: about $59.28 with a discount versus $60.13 without one. This comparison alone does not establish that discounts reduce spending.
- Subscription status: 1,053 records are marked subscribed (about 27%) and 2,847 are not. Average purchase amounts are similar: about $59.49 for subscribers and $59.87 for non-subscribers.
- Payment and shipping choices are used in fairly similar numbers, with no single option overwhelmingly dominating.
- Across all records, the average purchase amount is about $59.76 and the average review rating is about 3.75.
Business Recommendations
1. Review merchandising for Clothing and Accessories, which together account for about 77% of recorded revenue.
2. Investigate customer segments further before targeting campaigns by gender or age. Total revenue can be affected by the number of records in each group.
3. Test discount strategies carefully. Compare similar groups or run controlled tests before deciding whether discounts improve sales.
4. Review subscription benefits. Subscribers represent about 27% of records, but their average purchase amount is close to that of non-subscribers.
5. Continue monitoring payment and shipping options, as their usage is relatively balanced in this sample.
6. Collect transaction dates and richer customer history in future datasets to enable time-based and repeat-customer analysis.
Data Quality Checks and Limitations
- The inspected df1 dataset has 3,900 rows and 19 columns.
- The notebook reports no missing values and no duplicate rows in df1.
- The data has no transaction dates, so monthly or year-over-year trends cannot be analyzed.
- Several values and group totals are very similar. The dataset may be synthetic, so findings should be treated as observations about this sample rather than guaranteed real-world behavior.
- The notebook loads both shopping_trends.csv and shopping_trends_updated.csv. The first has 19 columns, including Preferred Payment Method; the second has 18 columns and a different arrangement of payment-related fields. The analysis shown is primarily performed on df1. Confirm which dataset version is intended before extending the analysis.
Tools and Technologies
- Python — analysis
- Pandas — data loading, cleaning, grouping, and aggregation
- NumPy — numerical support
- Matplotlib — charts
- Google Colab / Jupyter Notebook — notebook environment
How to Run
1. Download or clone the repository.
2. Open the notebook in Google Colab or Jupyter Notebook.
3. Make sure the CSV file(s) are available and update file paths if needed.
4. Install dependencies if they are not already installed:pip install pandas numpy matplotlib
5. Run the notebook cells from top to bottom.
The notebook currently uses these Colab paths:
pd.read_csv("/content/shopping_trends.csv")
pd.read_csv("/content/shopping_trends_updated.csv")
For local use, replace /content/ with the actual dataset path.
Project Structure
Update this example to match the actual filenames in your repository:
Customer-Shopping-Behavior-Analysis/
├── shopping_trends.csv
├── shopping_trends_updated.csv
├── Customer_Shopping_Behavior_Analysis.ipynb
└── README.md
Skills Demonstrated
- Reading CSV files with Pandas
- Checking data types, missing values, duplicates, and summary statistics
- Standardizing column names and category labels
- Creating derived columns for age groups and review-rating flags
- Grouping, aggregating, sorting, and comparing data
- Creating Matplotlib visualizations
- Turning descriptive findings into cautious business recommendations
Acknowledgment
This project is based on the Customer Shopping Behavior Analysis project by Amlan Mohanty. This README describes the Python notebook content reviewed for this project. Retain attribution to the original project and verify repository file names and dataset versions before publishing.

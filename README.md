# Superstore Sales Analysis (Python)

Exploratory data analysis of retail sales data to find which categories, regions and customer segments drive sales and profit, and how discounts affect profitability.

## Objective
- Clean and prepare the Superstore sales data
- Identify top-performing and weak areas (category, region, segment)
- Understand the relationship between discounts and profit
- Summarize the business with key performance indicators (KPIs)

## Dataset
- **File:** `Sample - Superstore 2019.xls` (Orders sheet), a public sample retail dataset
- **Size:** 9,994 order lines, 21 columns
- **Period:** Jan 2016 – Dec 2019 (United States only)
- **Scale:** 5,009 orders from 793 customers

## Tools
Python · pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## What I Did
1. **Data inspection:** shape, data types and missing values.
2. **Data cleaning**
   - 11 missing Postal Codes (all Burlington, Vermont) filled after looking up the correct code.
   - Checked duplicates (none) and inconsistent text values (none).
   - Detected outliers in Sales, Profit, Discount and Quantity using the IQR method. They were commercially valid, so I kept them.
3. **Feature engineering:** Shipping Duration, Profit Margin, and Sales Performance (Low / Medium / High).
4. **Analysis and visualization:** 10 charts, each with a question and a written finding.
5. **Extras:** KPI summary, an object-oriented preprocessing class, memory optimization (-41.6%), and an automated text report.

## Key Insights
| Metric | Result |
|---|---|
| Total sales | $2,297,201 |
| Total profit | $286,397 |
| Average profit margin | 12.03% |
| Average shipping time | 3.96 days (most orders ship in 4–5 days) |

- **Technology** is the top category in both sales ($836K) and profit ($145K).
- **Furniture** sells a lot ($742K) but makes only about $18K profit, a margin of roughly 2.5%.
- **West** is the best region (sales $725K, profit $108K). **Central** has the lowest profit ($40K).
- **Consumer** is the biggest customer segment ($1.16M in sales).
- **Discount and profit margin have a strong negative correlation (-0.86)**. Heavy discounts (70–80%) are linked to negative profit, though this shows a relationship, not proof of causation.

## Selected Charts
![Correlation Heatmap](images/Correlation%20Heatmap.png)
![Monthly Sales Trend](images/Trend%20plot.png)
![Profit by Category](images/Profit%20by%20Category%20Barplot.png)
![Discount vs Profit](images/Discount%20vs%20Profit.png)

## Project Structure
```
├── superstore_sales_analysis.ipynb   # full analysis
├── data/                             # original and cleaned data
├── images/                           # saved charts
└── outputs/                          # KPI summary and text report
```

## How to Run
```bash
pip install pandas numpy matplotlib seaborn xlrd jupyter
jupyter notebook superstore_sales_analysis.ipynb
```

## Author
Taysser Mahmoud · [LinkedIn](https://www.linkedin.com/in/taysser-mahmoud)

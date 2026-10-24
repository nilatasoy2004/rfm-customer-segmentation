# Customer Segmentation with RFM Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nilatasoy2004/rfm-customer-segmentation/blob/main/RFM_Customer_Segmentation.ipynb)

**Question:** Which customers drive an online retailer's revenue, and how should marketing treat each group differently?

## Data
[UCI Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii): transactions from a UK-based online gift retailer, December 2009 to December 2011. After removing rows without a customer ID, cancellations, invalid quantities or prices, and duplicates, the analysis uses **779,425 transactions from 5,878 customers**.

## Method
1. **RFM table:** for each customer, Recency (days since last purchase), Frequency (number of orders) and Monetary value (total spend).
2. **Scoring:** each metric scored 1 to 5 by quintile.
3. **Segmentation:** rule-based segments (Champions, Loyal, Potential Loyalists, New Customers, At Risk, Needs Attention, Hibernating, Lost).
4. **Check:** k-means clustering on log-scaled, standardised RFM values, compared with the rule-based segments.

Tools: Python, pandas, matplotlib, scikit-learn (Google Colab).

## Key findings
- **Revenue is highly concentrated:** the top 20% of customers generate **77.2%** of revenue.
- **Champions** are 22.4% of customers but **68.7%** of revenue, with an average spend of £9,070, about four times that of Loyal customers (£2,289).
- **At Risk** customers (11.6% of the base) used to buy often and spent £2,434 on average, but have stopped buying recently. They account for **£1.66M** of past revenue.

## Recommendations
- Focus retention budget on Champions (account management, early access, loyalty rewards).
- Move Loyal customers towards Champion behaviour with upselling and bundles.
- Test a targeted win-back campaign for At Risk customers.
- Keep spending on Lost and Hibernating customers low.

## Limitations
The data is from 2009 to 2011 and covers a single UK retailer with many wholesale buyers. It has no margin or marketing cost data, and the segments describe past behaviour rather than predict it.

## How to run
Click the **Open in Colab** button above and run the cells from top to bottom. The notebook downloads the data itself.

*Author: Nil Atasoy*

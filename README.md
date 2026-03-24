# Customer Behavior Analysis

**Tools:** Python · SQL (PostgreSQL) · Power BI  
**Dataset:** 10,000+ customer transaction records including purchase history, demographics, discounts, and subscription status  
**GitHub:** [View Repository](https://github.com/bhavika-chouhan/customer-behavior-analysis)

---

## Business Problem

A retail business needed to understand who its most valuable customers were, whether discounts were helping or hurting, and why subscription numbers weren't reflecting the loyalty already present in its customer base.

---

## What I Found

### The Customer Base Is Retention-Driven — Not Acquisition-Driven
After segmenting 3,900 customers by purchase history:

| Segment | Customers | Definition |
|---|---|---|
| Loyal | 3,116 | More than 10 previous purchases |
| Returning | 701 | 2–10 previous purchases |
| New | 83 | First purchase only |

**80% of the customer base is Loyal** — meaning the business grows by keeping customers, not constantly finding new ones. Marketing spend should reflect this.

### 2,518 Loyal Customers Haven't Been Converted to Subscribers
This was the most significant finding in the entire analysis.

Of all customers with more than 5 previous purchases:

| Subscription Status | Count |
|---|---|
| Not Subscribed | 2,518 |
| Subscribed | 958 |

**72% of repeat buyers are outside the subscription program.** These are customers who have already proven their loyalty through behavior — they just haven't been given a reason to subscribe. This is the single largest untapped revenue opportunity in the dataset.

### Discount Behavior
- Identified top 5 products with the highest discount rates using SQL
- Analyzed whether discounted purchases still exceeded average spend — they did, for a specific customer segment
- Subscribers and non-subscribers showed different average spend patterns

### Gender & Age Revenue Split
- Revenue contribution analyzed by gender and age group
- Identified which age segments drive disproportionate revenue

---

## Approach

### 1. Data Cleaning (Python)
- Resolved duplicates and missing values across 10,000+ records
- Standardized categorical fields (discount, subscription, shipping type)
- Prepared clean dataset for SQL and Power BI

### 2. SQL Analysis (PostgreSQL)
10 queries written covering:
- Revenue by gender
- Above-average spenders who used discounts (subquery)
- Top 5 products by review rating
- Shipping type vs average purchase amount
- Subscriber vs non-subscriber spend comparison
- Top discounted products (CASE + aggregation)
- Customer segmentation: New / Returning / Loyal (CTE + CASE)
- Top 3 products per category (ROW_NUMBER with PARTITION BY)
- Repeat buyer subscription correlation
- Revenue by age group

### 3. Power BI Dashboard
3-page interactive report covering:
- Customer segmentation breakdown
- Revenue by age group and gender
- Product performance and discount analysis
- Subscription vs non-subscription spend trends

---

## Key Takeaway

The data tells a clear story: this business has a loyalty problem disguised as a growth problem. With 3,116 loyal customers and 2,518 unconverted repeat buyers, the biggest revenue opportunity isn't acquiring new customers — it's converting the loyal ones who are already there.

---

## Files in This Repository

| File | Description |
|---|---|
| `customer_behavior_analysis.ipynb` | Python data cleaning notebook |
| `customer_behavior_analysis.sql` | 10 SQL queries with comments |
| `customer_behavior_analysis.pbix` | Power BI dashboard file |
| `Screenshots/` | Dashboard screenshots |

---

*Part of my data analytics portfolio. Also see: [Superstore Sales Analysis](https://github.com/bhavika-chouhan/superstore-sales-analysis)*

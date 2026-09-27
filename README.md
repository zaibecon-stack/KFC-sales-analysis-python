# KFC Sales Data Analysis (Python)

A Python/pandas analysis of a simulated transactional dataset covering ~96,700 KFC-style sales across 6 countries (Pakistan, USA, India, UK, UAE, Australia) from January to June 2025. The project explores revenue patterns by country, menu item, channel, and time of day, and uses basic statistics to test whether observed differences between markets are meaningful.

**Note:** This is a synthetic/practice dataset used for skill-building, not real KFC corporate data.

## Data

The dataset contains one row per transaction, with 96,738 rows and no missing values, covering:
- Date, day of week, hour of transaction
- Store, country, city, sales channel (Dine-In, Delivery, Drive-Thru, Takeaway)
- Menu item, item count, payment method
- Subtotal, discount, delivery fee, and final revenue (USD)

## Analysis

- Revenue breakdown by country, menu item, and sales channel using `pandas.groupby()`
- A pivot table comparing channel performance across countries
- Peak sales hours identified via hourly revenue aggregation
- Distribution of transaction revenue, and correlation between order size and revenue
- An independent t-test comparing average revenue per transaction between Pakistan and USA

## Key Findings

- Revenue differences between countries are driven mainly by transaction **volume**, not spending behavior — average revenue per transaction is nearly identical across all six countries (22.17–22.44 USD), and a t-test confirmed the Pakistan-USA gap is not statistically significant (p = 0.645).
- **Bucket Meal (8pc)** is the top individual seller, followed by Family Festival Box and Zinger Burger.
- **Dine-In** is the strongest sales channel, with a consistent channel mix across every country.
- Sales follow a clear two-peak daily pattern: **lunch (12:00)** and **dinner (18:00–19:00)**, with a lull between 14:00–17:00.
- Order size and revenue are moderately correlated (0.66) — larger orders tend to generate more revenue, though the relationship isn't perfect.

## Tools Used

- **Python** — pandas (data cleaning, groupby, pivot tables), matplotlib (visualization), scipy.stats (t-test)
- **Jupyter Notebook**

## Files

- `kfc_analysis.ipynb` — full analysis notebook with code, charts, and written conclusions
- `kfc_sales_data.xlsx` — source dataset

## About

Built by [Aurang Zaib] as a portfolio project. [Aurang Zaib] is an economics graduate learning data analytics.

# Sales Performance Analysis & Hypothesis Testing

End-to-end sales analytics project: data cleaning, exploratory analysis, customer
segmentation, trend analysis, statistical hypothesis testing, and a business
presentation — built on a two-year sales dataset (2024-2025).

## Project Structure

```
├── data/
│   ├── raw/sales_data_RAW.csv          # Raw dataset with intentional data quality issues
│   └── cleaned/sales_data_CLEANED.csv  # Cleaned, validated dataset
├── scripts/
│   ├── 01_generate_data.py             # Synthetic dataset generation
│   ├── 02_make_raw_data.py             # Injects realistic data quality issues
│   ├── 03_clean_data.py                # Full data cleaning pipeline
│   ├── 04_eda_charts.py                # Part 1: Exploratory data analysis
│   ├── 05_customer_analysis.py         # Part 2: Customer & segment analysis
│   ├── 06_trends_correlation.py        # Part 3: Trends & correlation analysis
│   └── 07_hypothesis_test.py           # Part 4: Statistical hypothesis testing
├── charts/                             # All generated chart images (11 total)
├── reports/
│   ├── Sales_Data_Cleaning.xlsx        # Raw vs Cleaned data + cleaning summary
│   └── Hypothesis_Testing_Summary.md   # Full statistical write-up
└── presentation/
    └── Sales_Performance_Deck.pptx     # Final stakeholder presentation
```

## Key Findings

- **Discounting hurts profit**: correlation of -0.52 between discount and profit;
  orders lose money past a 30% discount threshold.
- **Technology is the top category**, generating ~3x the profit of Furniture.
- **Low customer concentration risk**: top 10 customers account for only 3.5%
  of total sales; 94.9% of customers are repeat buyers.
- **Marketing campaign validated**: a new email campaign produced a statistically
  significant lift in conversion rate (26.1% vs 21.8%, p = 0.0015, 95% CI
  [1.70%, 6.99%]), though it did not significantly change average order value.

## Methodology

1. **Data Cleaning**: standardized text formatting, fixed currency/percent-as-text
   fields, resolved duplicate and conflicting records, handled missing values,
   validated all numeric fields.
2. **EDA**: sales/profit breakdown by region, category, and discount level.
3. **Customer Analysis**: segment performance, customer concentration, repeat
   purchase behavior.
4. **Trend Analysis**: monthly revenue trend, discount-profit correlation.
5. **Hypothesis Testing**: Chi-squared test (conversion rate) and independent
   t-test (order value) comparing a Treatment vs Control marketing group.

## Tools
Python (pandas, numpy, scipy, matplotlib), Excel (openpyxl), PowerPoint (pptxgenjs)

## Author
[Your name here]

# Venture Investment Market Analysis

## Project Overview

This project explores historical startup funding data to support a venture capital firm's choice of industries and funding types.

The analysis covers market segmentation, funding amounts, investment trends, and recorded returns. Recommendations are framed as of **2015**, based on historical data.

## Dataset

The analysis uses two datasets:

- `cb_investments` — company profiles, industries, locations, funding dates, round counts, and investment amounts by funding type.
- `cb_returns` — annual return amounts by funding type over 15 years.

The original company dataset contains **54,294 records**. After preprocessing, outlier removal, and filtering, the final sample includes **35,587 companies** for **2000–2014**.

## Analysis Steps

1. Clean missing values, standardize text fields, and convert data types.
2. Group companies by funding duration.
3. Classify market segments as mainstream, mid-sized, or niche.
4. Identify and remove funding outliers using segment-specific IQR thresholds.
5. Compare funding types by total volume and company count.
6. Explore annual funding trends and growing market segments.
7. Compare recorded returns with funding volumes and formulate historical recommendations.

## Key Findings

- The market is highly fragmented: **289 of 395 segments** are classified as niche.
- Companies with longer funding periods account for most of the capital raised.
- **Venture financing** leads in total funding volume, company count, and recorded returns.
- Funding round counts increased from 2000 to 2013, while median round size declined after 2005.
- The analysis highlights **Apps, Medical, and SaaS** as segments to consider in the historical investment recommendations.

## Tools and Libraries

- **Python**
- **pandas** — data cleaning, feature engineering, and aggregation
- **Matplotlib** and **seaborn** — data visualization
- **PhiK** — correlation analysis
- **Jupyter Notebook** — analysis and documentation
# Yandex Afisha: User Behavior and Seasonal Demand Analysis

## Project Overview

This project analyzes ticket purchases on Yandex Afisha to explore changes in demand between summer and autumn 2024 and compare the behavior of mobile and desktop users.

The goal is to identify seasonal patterns, examine key business segments, and provide recommendations for product and marketing teams.

## Dataset

The analysis uses three datasets covering **June–October 2024**:

- `final_tickets_orders_df.csv` — orders, users, devices, revenue, ticket counts, and intervals between purchases.
- `final_tickets_events_df.csv` — events, categories, age restrictions, venues, regions, and organizers.
- `final_tickets_tenge_df.csv` — daily exchange rates used to convert revenue from Kazakhstani tenge to Russian rubles.

## Analysis Steps

1. Merge datasets and handle missing values, duplicates, and invalid records.
2. Filter extreme revenue values and convert revenue to a common currency.
3. Create per-ticket revenue and temporal features.
4. Compare seasonal demand by event type, device, and age category.
5. Examine daily activity and weekly patterns during autumn.
6. Analyze regional demand and ticketing partner performance.
7. Use one-sided Welch’s t-tests to compare orders per user and mean time between orders for mobile and desktop users.

Seasonal comparisons use both order shares and average monthly order counts, since the data covers three summer months and two autumn months.

## Key Findings

- Average monthly orders increased across all event categories in autumn, with particularly strong growth in sports and theater.
- Mobile devices accounted for approximately **80% of orders** in both seasons.
- User activity was higher on weekdays than on weekends.
- The five largest ticketing partners accounted for **71.2% of orders** and **65.8% of revenue**.
- Among users who ordered on only one device type, mean autumn orders after outlier filtering were **2.60 for mobile** and **1.74 for desktop**. The difference was statistically significant.
- The second test did not support the hypothesis that mobile users had a higher mean interval between orders.

## Tools and Libraries

- **Python**
- **pandas** — data preparation and aggregation
- **NumPy** — numerical calculations
- **Matplotlib and seaborn** — data visualization
- **SciPy** — statistical hypothesis testing
- **Jupyter Notebook** — analysis and documentation

## Recommendations

Focus on the mobile purchase experience, account for seasonal demand and weekly activity patterns, and investigate differences in ticket revenue and performance across regions and ticketing partners.

Dashboard link: https://datalens.yandex/3ykq1muz2hysm?_share_link=public
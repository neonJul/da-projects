# Recommendation Algorithm A/B Test

## Project Overview

An entertainment app with an infinite content feed introduced a new recommendation algorithm intended to improve user engagement.

The goal of this project is to plan an A/B test, validate user allocation, and analyze whether the new algorithm increases the share of users viewing **four or more pages during their first session**.

## Dataset

The analysis uses three CSV datasets:

- **Historical session data:** August 15–September 23, 2025.
- **Launch-day experiment data:** October 14, 2025.
- **Full experiment data:** October 14–November 2, 2025.

The datasets contain user and session identifiers, session and installation dates, session sequence numbers, registration indicators, page views, regions, and device types. The experiment datasets also include group assignments.

## Analysis Steps

1. Explore historical user activity, registrations, and first-session page views.
2. Define the engagement metric and calculate the required sample size and estimated experiment duration.
3. Check launch-day group sizes, user overlap, and distributions by device and region.
4. Compare successful first-session rates between the control and treatment groups.
5. Apply a one-sided two-proportion Z-test and formulate a rollout recommendation.

## Key Result

The successful first-session rate was approximately **31.6% in the control group** and **31.5% in the treatment group**.

The test did not provide statistically significant evidence of an improvement (**p-value = 0.578**, α = 0.05). Based on this result, the recommendation is to retain the existing algorithm.

## Tools and Libraries

- **Python**
- **pandas** — data manipulation and aggregation
- **Matplotlib** — data visualization
- **statsmodels** — sample size calculation and statistical testing
- **Jupyter Notebook** — analysis and documentation
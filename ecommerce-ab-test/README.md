# E-commerce Conversion A/B Test

## Project Overview

BitMotion Kit, an online store selling gamified fitness products, tested a new website interface designed to improve purchase conversion.

The goal of this project is to evaluate the experiment and determine whether the new interface achieves the target conversion increase of **3 percentage points**.

## Dataset

The analysis uses two datasets:

- `ab_test_participants.csv` — user identifiers, experiment names, group assignments, and devices.
- `ab_test_events.zip` — user events, timestamps, and additional event details.

The primary metric is the share of registered users who make at least one purchase within **seven days of registration**.

## Analysis Steps

1. Select participants in the `interface_eu_test` experiment.
2. Compare group sizes and identify overlap with another experiment.
3. Exclude overlapping participants and prepare user events.
4. Filter events to the first seven days after registration.
5. Estimate the required sample size.
6. Calculate purchase conversion for the control and treatment groups.
7. Test the conversion difference against the target threshold.

## Key Results

After excluding participants in the other experiment, the groups contained:

- **Control A:** 4,952 users; purchase conversion of **27.81%**.
- **Treatment B:** 5,011 users; purchase conversion of **29.54%**.

The observed increase was **1.73 percentage points**, below the target of 3 percentage points. The statistical analysis did not establish that the target threshold was exceeded.

## Tools and Libraries

- **Python**
- **pandas** — data preparation and aggregation
- **statsmodels** — sample size estimation and statistical testing
- **Jupyter Notebook** — analysis and documentation
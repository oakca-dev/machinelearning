# In-Vehicle Coupon Recommendation Analysis

## Overview

This project analyzes the **In-Vehicle Coupon Recommendation** dataset to identify factors that influence whether drivers accept or reject coupons while driving.

The analysis includes:

- Data exploration and cleaning
- Investigation of coupon acceptance rates
- Visualization of key dataset characteristics
- Analysis of bar coupon acceptance
- Independent investigation of high-end restaurant coupon acceptance
- Business insights and recommendations

---

## Dataset

The dataset contains information about drivers receiving coupons while traveling, including:

- Coupon type
- Destination
- Weather
- Temperature
- Time of day
- Passenger type
- Driver demographics
- Driving context
- Whether the coupon was accepted (`Y = 1`) or rejected (`Y = 0`)

---

## Project Structure

```
├── prompt.ipynb      # Main Jupyter notebook containing analysis
├── coupons.csv       # Dataset
└── README.md         # Project documentation
```

---

## Tools and Libraries

The analysis was performed using:

- **Python**
- **Pandas** — data manipulation and cleaning
- **NumPy** — numerical operations
- **Matplotlib** — visualizations
- **Seaborn** — statistical data visualization

---

## Data Cleaning

The following preprocessing steps were performed:

1. Inspected missing values across all columns
2. Removed columns with excessive missing data
3. Removed rows containing remaining null values
4. Verified data types and dataset integrity

The cleaned dataset was used for all subsequent analyses.

---

## Exploratory Data Analysis

[View Notebook on GitHub](https://github.com/oakca-dev/machinelearning/blob/main/prompt.ipynb)

Several visualizations were created to better understand the dataset.

### Coupon Distribution

A count plot was used to examine the frequency of each coupon type.

**Findings:**
- Coffee House coupons were among the most common coupon types
- Restaurant ($20–$50) coupons were less frequent
- Coupon categories were not evenly distributed across the dataset

### Temperature Distribution

A histogram was created to analyze temperature values.

**Findings:**
- Most observations occurred at **80°F**
- **55°F** was the second most common temperature
- **30°F** was the least common temperature

---

## Bar Coupon Analysis

The acceptance behavior of drivers receiving Bar coupons was analyzed.

### Key Findings

- Drivers who visit bars frequently were significantly more likely to accept bar coupons
- Prior behavior was a strong predictor of future coupon acceptance
- Frequent bar visitors exhibited substantially higher acceptance rates compared to infrequent visitors

### Business Insight

> Targeting customers who already visit bars regularly may improve coupon campaign effectiveness.

---

## Independent Investigation: High-End Restaurant Coupons

An additional analysis was conducted on **Restaurant ($20–$50)** coupons.

### Overall Acceptance Rate

| Segment | Acceptance Rate |
|---|---|
| All High-End Restaurant Coupons | 44.15% |

### Dining Frequency Analysis

| Segment | Acceptance Rate |
|---|---|
| Visit High-End Restaurants ≤ 3 times/month | 42.52% |
| Visit High-End Restaurants > 3 times/month | 64.23% |

### Passenger Analysis

| Segment | Acceptance Rate |
|---|---|
| Not Driving Alone & Frequent Visitor | 58.97% |
| Traveling with Partner/Friends & Frequent Visitor | 65.22% |

### Key Findings

- Frequent high-end restaurant visitors were much more likely to accept restaurant coupons
- Drivers visiting high-end restaurants more than three times per month accepted coupons at **64.23%**, compared to **42.52%** for less frequent visitors
- Drivers traveling with partners or friends had the highest acceptance rate at **65.22%**

### Business Insight

> Previous dining behavior appears to be one of the strongest predictors of coupon acceptance. Marketing campaigns targeting frequent high-end restaurant customers — especially those traveling with companions — may achieve higher conversion rates.

---

## Summary of Key Takeaways

| Factor | Impact on Acceptance |
|---|---|
| Frequent bar visits | Strong positive predictor for bar coupons |
| Frequent high-end dining (> 3x/month) | Acceptance rate jumps from 42.52% → 64.23% |
| Traveling with partner or friends | Highest acceptance rate at 65.22% |

---

## Getting Started

To run the analysis locally:

```bash
# Clone the repository
git clone <your-repo-url>
cd <your-repo-folder>

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Launch the notebook
jupyter notebook prompt.ipynb
```

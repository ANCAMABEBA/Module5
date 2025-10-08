# Coupon Acceptance Analysis

## Project Overview
This project analyzes customer behavior to understand which features drive acceptance of different coupon types (Bar, Coffee Shop, Takeaways, Cheap Restaurant, More Expensive Restaurants).

## Dataset
- Number of entries: 12,684
- Number of features: 26
- Key columns include:
> Demographics: income, age, gender, marital status, education), customer habbits (number of visits to bars, coffee shops, takeaways and restaurants.
> Trip context: type of company in the vehicle, time to drive to redemption
> Coupon features: Type of coupon, expiration
- Dataset is here: data/coupons.csv

## Objective
The goal is to identify characteristics of drivers who accept coupons versus those who do not, and to visualize insights that can guide marketing strategies.

## Methodology
1. **Exploratory Data Analysis (EDA)**: Histograms, heatmaps, boxplots to identify patterns and outliers.
2. **Feature Engineering**: Created combined features like `To Coupon` to represent distance thresholds.
3. **Visual Analysis**: Compared acceptance rates across different customer segments.
4. **Insights**: Highlighted key features influencing coupon acceptance.

## Key Findings
- Drivers closer to coupon locations are more likely to accept coupons.
- Certain demographics (age, income, passenger type) show distinct acceptance patterns.
- Coupon type affects acceptance rates differently (e.g., Bar vs. Takeaways).

## Files in this Repository
- `analysis.ipynb` — Jupyter notebook with the full analysis.
- `data/` — Folder containing the datasets.
- `README.md` — Project overview and summary.

## How to Run
1. Clone the repository: `git clone <repo-url>`
2. Open `analysis.ipynb` in Jupyter Notebook or Colab.
3. Install required libraries: `pandas`, `seaborn`, `matplotlib`, etc.

## Author
Antonio Campomanes Manueco

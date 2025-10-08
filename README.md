# Coupon Acceptance Analysis

## Project Overview
This project analyzes customer behavior to understand which features drive acceptance of different coupon types (Bar, Coffee Shop, Takeaways, Cheap Restaurant, More Expensive Restaurants).

## Dataset
- Number of entries: 12,684
- Number of features: 26
- Key columns include:
  - Demographics: income, age, gender, marital status, education), customer habbits (number of visits to bars, coffee shops, takeaways and restaurants.
  - Trip context: type of company in the vehicle, time to drive to redemption
  - Coupon features: Type of coupon, expiration
- Dataset is [here](data/coupons.csv)
- Visuals created for Exploratory Data Analysis are [here](visuals)

## Objective
The goal is to identify characteristics of drivers who accept coupons versus those who do not, and to visualize insights that can guide marketing strategies.
These insights can help marketing departments to prioritize and direct investments more wisely.

## Methodology
0. **Data Preparation**: Eliminated "car" column due to its high volume of missing values. I labeled as "missing" missing values in other columns we could not discard.
1. **Exploratory Data Analysis (EDA)**: Histograms, heatmaps to identify patterns. 
2. **Feature Engineering**: Created a combined feature `To Coupon` to represent distance thresholds combining 3 of the existing columns in just one.
3. **Visual Analysis**: Compared acceptance rates across different customer cohorts.
4. **Insights**: Highlighted key features influencing coupon acceptance.

## Key Findings
- The two coupon types with the highest acceptance ratios are "Carry out & Takeaway" and "Restaurant(<20)"
- Certain demographics (age, income, passenger type) show distinct acceptance patterns:
  - Education: Customers with "Some High School" present significantly higher acceptance rates than others
  - Occupation: Customers in "Construction & Extraction". "Healthcare Support" and "Healthcare practicioners and Technical" accept copons more frequently
- Frequent users of Coffee Shops, inexpensive restaurants and Carryaways are more likely to accept coupons.
- Coupons that can be redeems in a less than 15 minutes radio have significantly higher acceptance rates.
- Coupon type affects acceptance rates differently across the different factors, for example:
  - Lower income customers drive significantly higher acceptance rates for Carryovers than for bars.
  - Customers with higher education have significantly higher acceptance rates for Carryaways than for bars
- Based on this, it is clear that further analysis must be conducted by coupon type:
  - Bar Cupons:
    - This type of coupon is more likely to be accepted by:
      - Drivers that go to bars more than once a month AND
      - Had passemgers that were not a kid AND
      - Had occupations other than farming, fishing and forestry
 - Carry and Takeway Cupons:
    - This type of coupon is more likely to be accepted by:
      - Drivers with incomes less than $37,500 AND
      - Passangers are kids AND
      - Drivers go to Carryovers more than once a month.     
  
## Files in this Repository
- `CouponsAnalysisMaster.ipynb` — Jupyter notebook with the full analysis.
- `data/` — Folder containing the dataset.
- `visuals/` — Folder containing the data visualizations created for the analysis.
- `README.md` — Project overview and summary.

## How to Run
1. Clone the repository: `git clone <repo-url>`
2. Open `CouponsAnalysisMaster.ipynb` in Jupyter Notebook or Colab.
3. Install required libraries: `pandas`, `seaborn`, `matplotlib`, etc.

## Author
Antonio Campomanes Manueco

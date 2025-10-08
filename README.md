# PROJECT OVERVIEW
#  - This project analyzes customer data related to coupon offers to understand which factors influence whether a customer accepts or rejects a coupon.
#  - The analysis uses a dataset that includes demographics (income, age, gender, marital status, education), customer habbits (number of visits to bars, coffee shops, etc.) and
#    trip context (other people in the vehicle, whether, destination, time to redemption), and coupon features (type of cuopon, expiration)
#  - You can view the full analysis in the Jupiter notebook here:(https://github.com/ANCAMABEBA/Module5/blob/main/CouponsAnalysisMaster.ipynb)
# CouponsAnalysisMaster.ipynb
# OBJECTIVE
#  - The goal is to identify patterns and differences between customers who accepted the coupon and those who did not.
#  - These insights can help marketing department to prioritize and direct investments more wisely
#
# DATASET - DESCRIPTIVE ANALYTICS
#  - 12,684 records corresponding each one to one coupon
#  - 26 columns: 25 input variables and 1 target variable with the info whether the coupon was accepted or not.
#  - Most columns are objects with categorical data and 8 are integers (including the target column)
#  - The column "car" has 12,576 missing values, which means it is not going to offer much explanatory value. This column is eliminated for the analysis.
#  - There are other 5 columns with missing values (between 107 and 217). They are completed with the word "Missing" to avoid discarding these rows.
# KEY INSIGHTS FROM THE ANALYSIS
#  - Overall, the two coupons types with the highest probablity to be accepted are "Carry out & Take Awa" and "Restaurant(<20)". "Bar" coupons are the least accepted.
#  - Looking at the explanatory value of features independently:
#      - The following features present the biggest gaps of acceptance rates across its values:
#            - Education: Customers with "Some High School" present significantly higher acceptance rates than customers with "Graduate Degree"
#            - Occupation: Customers in "Construction & Extraction", "Healthcare Support" and "Healthcare Practicioners and Technical" present significantly higher acceptance rates
#              compared to "Legal" and "Retired"
#            - Frequent users of Coffee Shops, inpexpensive restaurants and Carryaway are more likely to accept coupons.
#      - A little bit counter-intuitive; the fact that the place to redeem the coupon is or not in the same direction the customer was going, does not seem to have such a great
#        explanatory value.
#  - Driving factors for acceptance rate, vary depending on the coupon type which we know by looking at the data and also because of domain knowledge (customer decisions do not work the same
#    in the case of a bar or a restaurant, for example.
#  - Based on this, and given the time constraints the analysis was focused on two types; "Bar" Coupons and "Carry and Take Aways" Coupons
#  BAR COUPONS
#  - This type of coupons are more likely to be accepted among: (The probability is more than double for this cohort)
#     - Drivers to go to bars more than once a month AND
#     - Had passengers that were not a kid
#     - Had occupations other than farming, fishing and forestry
#  CARRY AND TAKE AWAYS
#  - This type of coupons are more likely to be accepted among: (Acceptance rates over 80% for this cohort).
#     - Driver has income less than $37,500  AND
#     - Passengers are kids AND
#     - Driver goes to Carryovers more than once a month
#  NEXT STEPS / RECOMMENDATIONS
#  - Validate further these hypothesis around these cohorts before spending marketing dollars: This can be achieved leveraging additional data 
#  - Complete the analysis for the rest of coupons types to gain insights 
#  - Start testing these hypothesis for example through A/B experiments to find out how to fine tune these cohorts to maximize conversion rates
#  - Once these hypothesis are confirmed/fine tunes, operationalize this model integrating it in the mobile app to manage coupons
#

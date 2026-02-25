# Unlocking-Retail-Purchase-Patterns-Market-Basket-Analysis-with-Apriori
***
## 📌 Executive Summary

This project applies Market Basket Analysis to an online retail dataset to uncover product purchasing patterns among customers in Germany. Using the Apriori algorithm and association rule mining, the analysis identifies frequently purchased item combinations and strong product associations based on lift and confidence metrics.

The insights generated can support cross-selling strategies, product bundling, promotion design, and recommendation systems to increase average order value and customer engagement.
 ***
### 🎯 Problem Statement

- Retail businesses often struggle to understand:

* Which products are commonly purchased together

- How to design effective product bundles

* How to improve cross-selling and upselling strategies

* How to optimize promotions based on customer purchasing behavior

 
**The objective of this analysis is to:**

Identify frequent itemsets and strong association rules that reveal meaningful purchasing relationships among products.
***
### Methodology

1️⃣ Data Source

* Online Retail Dataset (UCI Machine Learning Repository)

* Filtered to transactions from Germany

2️⃣ Data Cleaning & Preparation

* Removed leading/trailing whitespace in product descriptions

* Removed missing Invoice numbers

* Converted InvoiceNo to string

* Removed cancelled transactions (Invoice numbers containing "C")

* Removed non-product item: "POSTAGE"

* Grouped data by InvoiceNo and Description

* Transformed quantity into binary format (1 = purchased, 0 = not purchased)

#### *This created a transactional basket matrix suitable for association rule mining.*

3️⃣ Model Implementation

* Applied Apriori Algorithm

* Minimum Support = 0.07

* Generated Association Rules

* Metric: Lift

* Minimum Lift Threshold = 1

* Filtered strong rules:

   *Lift ≥ 3*

   *Confidence ≥ 0.30*
***
### Skills & Tools Demonstrated

* Python (Pandas, NumPy)

* Data Cleaning & Transformation

* Feature Engineering (Binary Encoding)

* Apriori Algorithm

* Association Rule Mining

* Business Interpretation of Lift, Confidence & Support

* Retail Analytics

* Exploratory Data Analysis (EDA)
***
## Libraries used:

* mlxtend

* pandas

* numpy
***
## Results & Key Insights

*Identified high-frequency item combinations within German transactions.*

*Discovered strong product associations with:*

1. High Lift (≥ 3)

2. Strong Confidence (≥ 30%)
***
#### *Example Insight:*
Certain themed product sets (e.g., matching lunch boxes and snack boxes) show strong co-purchase behavior, indicating potential for:

1. Bundle pricing

2. Joint promotions

#### *Recommendation engine rules*

High lift values indicate that these product combinations occur significantly more often than expected by chance.
***
## Business Requirements Addressed

This analysis supports:

✅ Cross-selling strategy
✅ Product bundling decisions
✅ Inventory planning
✅ Promotion optimization
✅ Recommendation system logic
✅ Customer purchasing pattern insights

Retail managers can use these insights to:

Increase average basket size

Improve conversion rates

Personalize product recommendations

Optimize store layout (online & physical)
***
### Next Steps

To further enhance the project:

* Test different support thresholds to compare rule stability.

* Segment analysis by:

* Country

* Time (seasonality)

* Customer segment

* Deploy insights into a recommendation engine prototype.

* Visualize rules using network graphs.

* Compare Apriori with FP-Growth for performance improvement.

* Calculate potential revenue impact of suggested bundles.

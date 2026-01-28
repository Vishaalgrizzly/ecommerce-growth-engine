# PulseCart Growth Engine: Propensity Modeling & Segmentation

### About the Author
**MSc Digital Marketing & AI Student | SKEMA Business School**
Bridging the gap between Data Science and Marketing Strategy. This project demonstrates how Machine Learning can solve the "Spray and Pray" marketing problem by identifying high-intent users and segmenting behavior.

--- xxx ---

### The Business Challenge
**PulseCart**, an e-commerce retailer, was struggling with a high CPA (Cost Per Acquisition). The marketing team was treating every website visitor the same, resulting in wasted ad spend on "window shoppers" and missed opportunities with "high-intent" researchers.

**The Goal:** Build a data-driven framework to:
1.  **Predict** who is likely to buy (Supervised Learning).
2.  **Segment** users into actionable personas (Unsupervised Learning).
3.  **Optimize** budget allocation to maximize ROAS.

--- xxx ---

### Methodology & Technical Approach
* **Tech Stack:** Python, Scikit-Learn, Pandas, Seaborn.
* **Data Cleaning:** Solved data quality issues (e.g., merging "New" vs. "New_Visitor" labels) to ensure accurate reporting.
* **Feature Engineering:** Created aggregated metrics like `Total_Engagement` (Duration) and `Total_Activity` (Pages) to feed the clustering algorithms.

### 📊 Key Strategic Insights

#### 1. The "Lost Opportunity" in Clustering
Using K-Means Clustering ($K=4$), we identified distinct behavioral personas. The most critical finding was **"The Researchers"**:
* **Behavior:** High time-on-site, high page views, but *zero* conversions.
* **Business Impact:** These users are stuck in "Analysis Paralysis."
* **Actionable Strategy:** Instead of generic retargeting, trigger an automated email sequence containing **Comparison Guides** or **Social Proof** (Reviews) to push them over the edge.

#### 2. The "VIP" Segment
* **Behavior:** High `PageValues` and administrative interaction.
* **Actionable Strategy:** Stop offering discounts to this group (margin erosion). Shift focus to **Loyalty Programs** and **Bundles** to increase CLV (Customer Lifetime Value).

#### 3. Propensity Scoring (Logistic Regression)
* **Model Performance:** Achieved a **Recall of ~X%** (capturing the vast majority of actual buyers).
* **Threshold Strategy:** Recommended lowering the classification threshold to **0.3** for Email Marketing.
    * *Why?* In a growth phase, missing a potential buyer (False Negative) is more costly than sending a cheap email to a non-buyer.

--- xxx ---

### Final Recommendations
Based on this analysis, I proposed a 3-point plan to the PulseCart management team:
1.  **Budget Reallocation:** Cut ad spend on the "Bouncers" segment (High Bounce Rate, Low Duration) and reinvest it into "Researcher" retargeting.
2.  **UX Optimization:** High exit rates on Administrative pages suggest friction in the checkout/login flow—prioritize for A/B testing.
3.  **Data Quality:** Implement a "Session Timeout" tag to fix the "Zombie Session" data anomalies (sessions > 5 hours).

--- xxx ---

### How to Run This Project
1.  Clone the repo:
    ```bash
    git clone [https://github.com/]https://github.com/vishaalgrizzly/ecommerce-growth-engine.git
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Run the Notebook: `PulseCart_Growth_Strategy.ipynb`

---
*Open for collaboration! Connect with me on LinkedIn.*

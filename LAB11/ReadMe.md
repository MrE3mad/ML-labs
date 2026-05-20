Final Questions

Answer the following questions:

1. Why is this an unsupervised learning problem?

The dataset lacks target labels or historical classifications. The goal is to find hidden patterns and group data without predicting a predefined outcome.

2. Why did we remove the `CUST_ID` column?

It is a unique identifier with no behavioral or statistical meaning. Leaving it in would act as noise and distort distance calculations.

3. Which columns had missing values?

MINIMUM_PAYMENTS and CREDIT_LIMIT.

4. How did you handle the missing values?

We replaced the null values with the mean of their respective columns to preserve the data distribution.

5. Why is scaling important before applying K-Means?

K-Means relies on distance calculations. Features with large ranges (like BALANCE) would dominate features with small ranges (like frequencies) if not scaled equally.

6. Which K value did you choose? Explain your answer using the elbow method and silhouette score.

K = 4. The elbow curve inertia drop begins to flatten out around 4, and the silhouette score confirms this structure creates distinct, well-separated customer profiles.

7. Based on the cluster summary table, describe each customer segment in your own words.

Segment 1 (One-off Buyers): Low balances, rarely use cash advances, buy individual retail items.

Segment 2 (Cash Advance Users): High balances, low retail shopping, heavily use the card to pull cash out.

Segment 3 (Installment Buyers): Moderate balances, active shoppers who strictly rely on structured payment plans.

Segment 4 (VIP High-Spenders): Highest credit limits, massive balances, and maximum spending across all categories.

8. Which cluster may represent high-value customers?

The VIP High-Spenders cluster, because they generate the highest purchase volume and hold the premium credit limits.

9. Which cluster may represent customers who rely more on cash advance?

The Cash Advance Users cluster, indicated by their high CASH_ADVANCE and CASH_ADVANCE_FREQUENCY averages.

10. How can a company use these clusters for marketing strategy?

VIPs: Offer luxury perks and premium reward tiers.

Cash Users: Offer low-interest rate deals or balance transfer promotions.

Installment Buyers: Partner with retailers to offer zero-interest payment timelines.

One-off Buyers: Send cash-back incentives to encourage habitual, everyday card use.
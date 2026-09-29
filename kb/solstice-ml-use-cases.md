# Solstice Commerce Group — Machine Learning Use Cases

Planned machine learning projects at Solstice Commerce Group, written with the company's internal
terms (see the Solstice glossary). The data needs are described in business language.

## Use case 1 — Velocity Tier drop prediction (churn early warning)

Goal: spot customers likely to move from the Steady tier to the Fading tier before it happens.
Data needed: for every customer, the full history of when they placed orders, detailed enough to
compute order frequency and the time between orders.
Approach: binary classification (drops a tier within N weeks or not) or survival analysis.

## Use case 2 — Glimmer Score prediction for new products

Goal: before launching a product, estimate how attractive it will be within its category to set
the launch price.
Data needed: each product's category and price relative to other products in that category, plus
how often products in that category were ordered historically.
Approach: regression on category and relative price features.

## Use case 3 — Drift Margin anomaly detection

Goal: flag orders whose value is far from the customer's usual order value, for fraud checks and
upsell tracking.
Data needed: the value of every order per customer over time, to build each customer's baseline.
Approach: per-customer z-score or isolation forest.

## Use case 4 — Nova Segment re-clustering

Goal: find more meaningful customer groups than signup cohort plus country alone.
Data needed: when each customer signed up, where they are located, and a summary of their orders
(count, frequency, average value).
Approach: k-means or hierarchical clustering.

## Use case 5 — Orbit Cycle forecasting

Goal: predict when a customer's Orbit Cycle starts to stretch, to time re-engagement campaigns.
Data needed: the ordered sequence of order dates per customer.
Approach: per-customer time-series forecasting of the gap to the next order.

## Use case 6 — Halo Effect cross-sell recommendations

Goal: raise basket size by recommending related categories with a strong Halo Effect.
Data needed: which product categories each customer ordered, and in what order over time.
Approach: association rules or sequence mining across categories.

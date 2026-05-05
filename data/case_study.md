## About Dataset

The provided `capstone_dataset.csv` contains **500 records** of e-commerce transactions with the following columns:

| Column | Type | Description |
|--------|------|-------------|
| `transaction_id` | string | Unique transaction identifier |
| `date` | date | Transaction date |
| `customer_id` | string | Customer identifier |
| `customer_segment` | category | Customer type (New, Returning, VIP) |
| `product_category` | category | Product category |
| `product_price` | float | Price in USD |
| `quantity` | int | Units purchased |
| `discount_applied` | float | Discount percentage (0-1) |
| `marketing_channel` | category | Acquisition channel |
| `region` | category | Geographic region |
| `total_revenue` | float | Transaction revenue in USD |
| `customer_satisfaction` | int | Satisfaction score (1-5) |
| `returned` | bool | Whether item was returned |


## Suggested Case Study Paths

Use these as a starting foundation, but you should definitely dig deeper! If you go with this dataset, try to do at least 2 of these paths.

---

## 1. 💰 Revenue Optimization

**Scenario**:
You are a data analyst for an e-commerce company trying to increase revenue.

**Primary Question**:

What factors have the biggest impact on total revenue?

**Suggested Angles**:

* Revenue by product_category
* Revenue by customer_segment
* Impact of discount_applied
* Revenue by marketing_channel

**Deeper Thinking**:

* Are discounts actually increasing total revenue?
* Are certain segments more profitable than others?

*Optional Modeling*:
* Predict `total_revenue`

---

## 2. 🔁 Returns Analysis

**Scenario**:
The company is losing money due to product returns.

**Primary Question**:

What patterns are associated with returned items?

**Suggested Angles**:

* Return rate by product_category
* Return rate by customer_segment
* Relationship between discount_applied and returns
* Regional return patterns

**Deeper Thinking**:

* Are discounts leading to more returns?
* Are certain customer types more likely to return items?

*Optional Modeling*:
* Predict returned (classification)

---

## 3. 📣 Marketing Effectiveness

**Scenario**:
The marketing team wants to know which channels are worth investing in.

**Primary Question**:

Which marketing channels bring in the highest-value customers?

**Suggested Angles**:

* Revenue by marketing_channel
* Average order value by channel
* Return rates by channel
* Customer satisfaction by channel

**Deeper Thinking**:

* Do some channels bring in high revenue but low satisfaction?
* Which channels attract repeat vs low-quality customers?

---

## 4. 👥 Customer Segmentation

**Scenario**:
The company wants to better understand its customers.

**Primary Question:**

* How do different customer segments behave?

**Suggested Angles:**

* Revenue by customer_segment
* Purchase quantity patterns
* Satisfaction scores by segment
* Return behavior by segment

**Deeper Thinking**:

* Are VIP customers actually more valuable?
* Do “New” customers behave differently from “Returning”?

---

## 5. 🌎 Regional Performance

**Scenario:**
Leadership is evaluating regional expansion.

**Primary Question:**

How does performance vary by region?

**Suggested Angles:**

* Revenue by region
* Return rates by region
* Product category preferences by region
* Satisfaction by region

**Deeper Thinking:**

* Are certain regions underperforming?
* Do different regions prefer different products?

---

## 6. 🎯 Discounts & Pricing Strategy

**Scenario:**
The company frequently uses discounts but is unsure if they help.

**Primary Question:**

* Are discounts improving or hurting business performance?

**Suggested Angles:**

* Revenue vs discount_applied
* Return rates vs discount levels
* Satisfaction vs discount
* Quantity purchased vs discount

**Deeper Thinking:**

* Do higher discounts increase sales but reduce profitability?
* Is there a “sweet spot” for discounts?
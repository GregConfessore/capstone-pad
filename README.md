# Capstone Project — Applied Python for Data Analysis

## Overview

The **Capstone Project** is the final project for the Python for AI & Data course. This project is designed to simulate a real-world data analysis workflow using Python.

You will:
- Select a dataset
- Define a clear analytical problem
- Clean and explore the data
- Generate insights and visualizations
- (Optionally) build a simple predictive model
- Present your findings in a professional format

> 🎯 **Goal:** Demonstrate your ability to use Python to analyze data, generate insights, and communicate results clearly.

---

## Project Tracks (Choose One)

To balance flexibility and structure, you will complete the project using one of the following tracks:

### 🔹 Track A: Curated Dataset (Recommended)

Choose **one** of the provided datasets:

- [Ames Housing](./data/airbnb.md) (Regression-focused)
- [Gapminder / World Development](./data/gapminder.md) (EDA & storytelling)
- [Airbnb Listings](./data/airbnb.md) (Real-world, messy data)
- [Instructor-provided case study](./data/case_study.md)

### 🔹 Track B: Bring Your Own Dataset (Approval Required)

[You may use your own dataset](./data/dataset_proposal.md) **only with instructor approval**.

#### Requirements:
- At least **500 rows**
- Includes **numeric and categorical features**
- Tabular format (CSV preferred)
- No heavy API or web scraping required (but encouraged if you feel confident)
- Supports a clear analytical question

---

## 🚨 Dataset Proposal (Required for ALL Students)

Before starting your analysis, you must submit a short proposal including:

1. Dataset name + link
2. Problem statement:
   - What question are you trying to answer?
   - Who is the audience?
3. 2–3 analysis questions you want to explore
4. (Optional) Target variable (if modeling)

> ⚠️ You must receive approval before proceeding.

---

## Project Structure

Capstone_Project/
```text
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── analysis.ipynb
│
├── outputs/
│   ├── figures/
│   └── results.csv (optional)
│
├── docs/
│   └── project_summary.md
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Project Requirements

### 1. Data Processing (Required)
- Load and inspect dataset
- Handle missing values
- Fix data types
- Address duplicates or inconsistencies
- Save cleaned dataset

### 2. Exploratory Data Analysis (Required)
- Summary statistics
- At least **2 meaningful visualizations**
- Identify patterns, trends, or relationships

### 3. Insights & Recommendations (Required)

You must clearly answer:

- What did you discover?
- What insights matter most?
- What should be done based on your analysis?

### 4. Analysis Depth (Choose At Least One)

You must include **at least one** of the following:

- Group-based analysis (e.g., `.groupby()`)
- Statistical comparison
- Segmentation analysis
- Time-based trends
- Simple predictive model (optional)

### 5. Optional: Modeling (Bonus)

You may include a simple model:

- Linear Regression (for numeric prediction)
- Logistic Regression (for classification)

### 6. Documentation (Required)

Your notebook must include:

- Clear problem statement (look at Tips and Resources section)
- Step-by-step explanation of your workflow
- Markdown explanations throughout

### 7. Final Summary (Required)

Include a short summary (`docs/project_summary.md`) with:

- Problem statement
- Key insights
- Recommendations
- Limitations of your analysis

---

## Evaluation Criteria

| Category | Weight |
|----------|--------|
| Data Cleaning & Preparation | 20% |
| EDA & Visualizations | 20% |
| Insights & Recommendations | 25% |
| Code Quality & Organization | 15% |
| Documentation & Clarity | 20% |

---

## Tips for Success

### Do:
- Start with a clear question
- Keep your analysis focused
- Document as you go
- Test your notebook from top to bottom

### Don’t:
- Don’t pick a dataset that is too complex
- Don’t rely only on visuals without explanation
- Don’t overcomplicate your analysis

---

## Using AI Tools

AI tools (ChatGPT, Copilot, etc.) may be used to:
- Debug code
- Explain concepts
- Suggest approaches

You should NOT:
- Copy full solutions without understanding
- Generate your entire project using AI

---

## Submission Instructions

1. Push your completed project to GitHub
2. Ensure all required files are included
3. Submit your repository link via the LMS

---

## Tips & Resources

### 🎯 Start With ONE Clear Question

Your project must answer **one primary business question**.

Bad example:
> “I explored the dataset to find insights.”

Good example:
> “What factors drive revenue, and how can the business increase it?”

---

### 📊 From Observations → Insights → Recommendations

A common mistake is stopping at charts.

You must go further.

#### ❌ Weak Analysis
> “VIP customers have higher average revenue.”

#### ⚠️ Better (but still incomplete)
> “VIP customers have higher average revenue than other segments.”

#### ✅ Strong Insight
> “VIP customers generate significantly higher revenue than other segments, suggesting the company should prioritize retention strategies for this group.”

#### 🚀 Best (Insight + Recommendation)
> “VIP customers generate the highest revenue and have lower return rates. The company should invest in loyalty programs and targeted promotions to retain and expand this segment.”

---

### 🧠 What Makes a Strong Insight?

A strong insight:
- Explains **why something matters**
- Connects to a **business decision**
- Goes beyond just describing data

Ask yourself:
- “So what?”
- “Why does this matter?”
- “What should be done?”

---

### 📉 Avoid These Common Mistakes

- ❌ Creating charts without explanation  
- ❌ Running too many unrelated analyses  
- ❌ Choosing a dataset that is too complex  
- ❌ Jumping into modeling without understanding the data  
- ❌ Failing to connect findings to a real-world decision  

---

### 📌 Keep Your Analysis Focused

- Pick **one main question**
- Support it with **2–3 key analyses**
- Avoid trying to analyze everything

> A focused project is stronger than a scattered one.

---

### 🔗 Working with Multiple Datasets (`pd.merge()`)

If your project uses multiple datasets, you will likely need to **join them together**.

#### Basic Syntax

```python
import pandas as pd

customers = pd.DataFrame({
    "customer_id": [1, 2, 3],
    "segment": ["New", "Returning", "VIP"]
})

orders = pd.DataFrame({
    "customer_id": [1, 2, 2, 3],
    "revenue": [100, 200, 150, 300]
})

merged = pd.merge(customers, orders, on="customer_id", how="inner")
print(merged)
```

| Type    | Description                             |
| ------- | --------------------------------------- |
| `inner` | Only matching rows (default)            |
| `left`  | All rows from left, matches from right  |
| `right` | All rows from right, matches from left  |
| `outer` | All rows from both, fill missing values |


---

### 🎯 Crafting a Strong Problem Statement (SMART Framework)

A weak problem statement leads to a weak project.

Use the **SMART Framework** to define a clear, focused question for your analysis.

---

#### 🔤 SMART Criteria

- **S — Specific**  
  What exactly are you trying to answer?

- **M — Measurable**  
  What data will you use to measure this?

- **A — Achievable**  
  Can you realistically answer this using your dataset?

- **R — Relevant**  
  Why does this matter? What decision could this inform?

- **T — Time-bound (Optional)**  
  Is there a time component (e.g., trends over time)?

---

#### ❌ Weak Problem Statement

> “I want to analyze sales data.”

---

#### ⚠️ Better

> “I want to understand factors affecting revenue.”

---

#### ✅ Strong (SMART) Problem Statement

> “I want to identify which customer segments and marketing channels drive the highest revenue so the company can prioritize high-performing acquisition strategies.”

---

#### 💡 Tips for Writing Your Problem Statement

- Focus on **one main question**
- Tie your analysis to a **decision or action**
- Make sure your dataset can actually support your question

---

#### 🤔 Self-Check Questions

Before moving forward, ask yourself:

- What decision will this analysis inform?
- Who benefits from this analysis?
- What would I do with the result?


---

### 🧪 Optional: Modeling Is Not the Goal

If you include a model:
- Keep it simple
- Focus on what you learned

A good explanation of a simple model > a complex model you don’t understand

---

### 🛠️ Helpful Resources

- Pandas Documentation: https://pandas.pydata.org/docs/
- Matplotlib Gallery: https://matplotlib.org/stable/gallery/
- Scikit-learn Documentation: https://scikit-learn.org/stable/

---

### 💬 Final Advice

> Clarity beats complexity.

A simple, well-explained analysis with strong insights is far more valuable than a complex project with no clear takeaway.

---

## Final Thoughts

This project is about demonstrating what you can do with Python and data.

Focus on:
- Clarity over complexity
- Insight over volume
- Understanding over perfection

**Good luck 🚀**

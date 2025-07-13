## 1. Dataset Description

The **Customer Personality Analysis** dataset contains demographic, behavioral, and spending data for 2,240 customers of a company. It includes 29 attributes such as age, education, income, family size, and spending on different product categories.

**Source**: [https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)

## 2. Justification for Selection

This dataset is ideal for data mining because:
- It contains a rich variety of numeric and categorical variables.
- It includes over 2,000 records, satisfying the required minimum.
- It allows exploration of multiple data mining tasks including **clustering (segmentation)**, **classification (predictive modeling)**, and **association rule mining** based on spending behavior.

## 3. Key Insights from EDA

- **Age Distribution**: Derived from `Year_Birth`, most customers are between 30–60 years old.
- **Spending Trends**: Customers spend the most on **Wines**, followed by **Meat** and **Gold**.
- **Correlations**:
  - **Age** has a **negative correlation** with spending — younger customers spend more.
  - **Income** is positively correlated with all product categories.
- **Marital Status and Spending**: Married and together customers have slightly higher average income and spending.

## 4. Implications for Modeling

- Spending behavior can be predicted based on income, education, and age.
- Segmentation models (e.g., K-Means) could group customers based on purchase habits.
- Classification tasks could focus on predicting high-value customers.

These insights will guide feature selection and modeling in the next phases.
# Customer Segmentation and Campaign Response Analysis

## 1. Modeling Objective

The goal of this project was to go beyond simple regression and apply advanced data mining techniques to better understand customer behavior and marketing campaign responses. Specifically, we:
- Built and evaluated **classification models** to predict campaign responses.
- Applied **K-Means clustering** to segment customers by product spending behavior.
- Conducted **association rule mining** to uncover purchasing patterns across products.
- Performed **hyperparameter tuning** to improve classification performance.

Together, these methods provide a multi-angle understanding of customer behavior: prediction, segmentation, and discovery of cross-product relationships.

---

## 2. Classification Results

Two classification models were implemented: **Decision Trees** and **k-Nearest Neighbors (k-NN)**.

- **Preprocessing:** Categorical variables (e.g., education, marital status) were one-hot encoded, while numerical features were scaled to avoid bias.
- **Results:**
  - Decision Trees provided strong interpretability, showing **income, education, and family composition** as key predictors of campaign response.
  - k-NN was more sensitive to scaling and class imbalance, leading to slightly lower performance compared to Decision Trees.
- **Hyperparameter Tuning:** Adjusting tree depth and k-values improved stability and reduced overfitting.

**Insight:** Higher-income, long-tenure customers were more likely to respond positively to marketing campaigns.

---

## 3. Clustering Results

We applied **K-Means clustering** to segment customers based on product spending (`MntWines`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`).

- **Preprocessing:** StandardScaler was used to normalize spending features.
- **Optimal Clusters:** Using the elbow method, we selected **k=4 clusters**.
- **Cluster Profiles:**
  - **Cluster 0:** High spenders across most categories (premium customers).
  - **Cluster 1:** Moderate and balanced spending.
  - **Cluster 2:** Niche buyers (specialized in wines or gold).
  - **Cluster 3:** Low spenders across all categories.

**Insight:** Clustering revealed actionable customer groups, enabling targeted promotions — such as premium bundles for Cluster 0 and incentives for Cluster 3.

---

## 4. Association Rule Mining Results

Using **Apriori-based association rule mining**, we identified frequent co-purchasing behaviors.

- **Key Findings:**
  - Customers who purchased **wines** often also purchased **meat and gold products**.
  - Rules with high support and confidence indicated that premium buyers tend to be consistent across multiple product categories.
- **Applications:** These insights support **cross-selling strategies**, such as recommending meat or gold to wine buyers.

**Insight:** Association rules highlight opportunities for personalized marketing and product bundling.

---

## 5. Key Insights

- **Classification** identified which customers are more likely to respond to campaigns.
- **Clustering** uncovered natural customer groups based on product spending.
- **Association Rule Mining** revealed strong co-purchasing relationships.
- Combined, these methods provide a comprehensive understanding of customer behavior for **targeted marketing, segmentation, and cross-selling**.

---

## 6. Challenges and Resolutions

- **Categorical Variables:** Education and marital status required one-hot encoding to avoid model errors.
- **Cluster Selection:** Choosing the optimal number of clusters was addressed using the **elbow method** and **silhouette scores**.
- **Association Rule Overload:** Initial runs produced too many low-value rules; we improved results by adjusting support, confidence, and lift thresholds.

---

## 7. Ethical Considerations

- **Data Privacy:** Customer records were anonymized to prevent re-identification.
- **Fairness & Bias:** Features such as income and education can introduce socioeconomic bias. Care was taken to evaluate model fairness and avoid decisions that disproportionately affect specific groups.
- **Transparency:** Decision Trees were prioritized for interpretability, ensuring stakeholders can understand why certain predictions were made.

---

## 8. Visualizations

- **EDA:** Histograms and distributions of customer demographics and spending patterns.
- **Clustering:** Scatter plot of Wine vs. Meat spending (scaled) colored by cluster, and bar charts showing average spending per cluster.
- **Classification:** Decision Tree plots highlighting feature importance.
- **Association Rules:** Network graph of co-purchased products.

---

## 9. Conclusion

This project demonstrates how combining **classification, clustering, and association rule mining** enables businesses to:
- Predict campaign responses.
- Segment customers for personalized strategies.
- Uncover product co-purchasing behavior for effective cross-selling.

These insights can directly inform **marketing strategies, product bundling, and customer engagement** initiatives.
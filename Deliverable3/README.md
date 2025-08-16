## 1. Modeling Objective

The goal of this phase was to expand beyond regression analysis and apply advanced data mining techniques to understand customer behaviors and campaign responses more deeply. Specifically, we built and evaluated classification models to predict customer responses, applied clustering algorithms to uncover natural customer segments, and conducted association rule mining to identify purchasing patterns. Additionally, hyperparameter tuning was applied to improve the performance of at least one classification model. These methods provide a multi-angle approach to modeling customer behavior — prediction, segmentation, and pattern discovery.

## 2. Classification Results

Two classification models — Decision Trees and k-Nearest Neighbors (k-NN) — were implemented. After preprocessing categorical variables with one-hot encoding and scaling numeric features, the Decision Tree model achieved strong interpretability, clearly identifying attributes such as income, education, and family composition as key predictors of campaign response. The k-NN model, while simpler, was sensitive to data scaling and class imbalance, leading to slightly lower accuracy compared to Decision Trees. Hyperparameter tuning (e.g., adjusting tree depth and k values) improved model stability. Overall, classification revealed that higher-income, long-tenure customers were more likely to respond positively to marketing campaigns.

## 3. Clustering Results

A K-Means clustering model was applied to group customers into distinct segments. After experimenting with different values of k, the elbow method suggested an optimal cluster size of around 3–5 groups. The clusters revealed clear differences in spending habits and demographics: one group represented high-income, high-spending customers, another group was mid-income with balanced purchases, and a third cluster contained low-income, low-response customers. Visualizations confirmed well-separated clusters, demonstrating that clustering provides actionable segments for targeted marketing strategies.

## 4. Association Rule Mining Results

Using Apriori-based association rule mining, we identified frequent purchasing patterns across product categories. For example, customers who purchased higher amounts of wine often also purchased gourmet products like gold and meat. Rules with high support and confidence indicated that premium product buyers are consistent across multiple categories. These insights can guide cross-selling strategies, such as recommending meat or gold products to wine enthusiasts. In practice, applying these rules enables more effective personalized marketing and product bundling.

## 5. Key Insights

The integration of classification, clustering, and association rule mining produced complementary insights. Classification models identified which types of customers are most likely to respond to campaigns, while clustering uncovered natural customer groupings that can guide tailored strategies. Association rule mining revealed strong co-purchasing behaviors that can enhance cross-selling opportunities. Together, these results highlight the importance of combining predictive modeling, segmentation, and pattern discovery to fully leverage customer data.

## 6. Challenges and Resolutions

A major challenge was handling categorical variables such as education and marital status during classification, as raw string data caused model training to fail. This was resolved by applying OneHotEncoder with proper scaling for numeric features. Another difficulty was determining the optimal number of clusters for K-Means, which was addressed through the elbow method and silhouette score validation. Finally, association rule mining initially produced too many low-value rules; this was improved by carefully tuning the support, confidence, and lift thresholds to focus on meaningful patterns.
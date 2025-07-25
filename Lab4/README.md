# Regression Analysis on Diabetes Dataset
## Purpose
The purpose of this lab was to explore and compare multiple regression techniques using the Diabetes dataset from sklearn.datasets. The lab demonstrates how different regression models — including Simple Linear Regression, Multiple Linear Regression, Polynomial Regression, Ridge, and Lasso — can be used to predict the progression of diabetes based on physiological features. Through hands-on modeling and evaluation, the goal was to understand how each method fits the data, handles complexity, and mitigates overfitting.

## Key Insights
- **Simple Linear Regression:** Provided a baseline model using a single feature. While easy to interpret, it had limited predictive power, reflecting the importance of using multiple correlated inputs in medical datasets.

- **Multiple Regression:** Improved prediction accuracy by incorporating all features. However, the model risked overfitting in the presence of multicollinearity.
- **Polynomial Regression:** Showed how higher-degree terms can improve model fit but also highlighted the danger of overfitting with increasing complexity. Best suited when non-linear relationships are evident.
- **Ridge and Lasso Regression:** Both regularization techniques helped control overfitting.
- **Ridge:** Penalized large coefficients but kept all features.
- **Lasso:** Performed feature selection by shrinking some coefficients to zero, enhancing interpretability.
- **Evaluation Metrics:** MAE, MSE, RMSE, and R² were used throughout to evaluate model performance and compare predictive effectiveness.

## Challenges and Decisions
- **Feature Scaling:** Ensured consistent model performance, especially for regularized regression. Data was standardized using StandardScaler.

- **Model Selection:** Chose regression techniques progressively — starting from simple linear to advanced regularization — to observe how model complexity impacts performance.

- **Polynomial Degree Tuning:** Demonstrated that increasing the polynomial degree may lead to better training accuracy but worse generalization, highlighting the importance of bias-variance tradeoff.

- **Alpha Selection in Ridge/Lasso:** Explored how different alpha values impact model shrinkage and generalization.
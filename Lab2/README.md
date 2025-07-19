# KNN vs RNN Classification on Wine Dataset
## Purpose
The purpose of this lab was to analyze and compare the performance of two classification algorithms — K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) — using the Wine dataset from scikit-learn. The lab focused on how changing key hyperparameters (k for KNN and radius for RNN) influences model accuracy. This hands-on experiment aimed to build intuition around neighbor-based classifiers and their sensitivity to parameter tuning.

## Key Insights
- **KNN Accuracy Trends:** The model showed strong performance with k values between 5 and 11. Lower values like k=1 risked overfitting, while higher values like k=21 slightly reduced accuracy due to averaging over too many neighbors.
- **RNN Behavior and Limitations:** RNN struggled with certain radius values. If the radius was too small, the model could not classify some test points due to lack of nearby training neighbors. Accuracy improved with slightly larger radius values but plateaued after a point.
- **Model Comparison:** KNN consistently classified all test samples and yielded stable, high accuracy across most k values. RNN, while adaptive, required careful tuning of radius and additional logic to handle unclassified samples.


## Challenges and Decisions
- **Unclassified Instances in RNN:** When using small radius values, the model returned -1 for some test points, indicating no neighbors were found. We addressed this by filtering out unclassified points when computing accuracy — a trade-off between precision and coverage.
- **Hyperparameter Trial & Error:** Unlike KNN, where k values are straightforward, determining appropriate radius values for RNN required iterative experimentation since the data scale was not intuitive.
- **Interpretability & Fair Comparison:** Because RNN may not classify all samples, comparing its raw accuracy with KNN can be misleading. We made sure to note how many samples were actually classified during evaluation.
- **Data Normalization Consideration:** While the Wine dataset did not require extensive preprocessing, future improvements could include feature scaling to ensure distance-based models behave more consistently.

## Tools Used
- Python (Scikit-learn, Pandas, NumPy, Matplotlib)
- Jupyter Notebook
- Wine dataset from sklearn.datasets.load_wine()
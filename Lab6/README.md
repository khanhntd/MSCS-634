# Association Rule Mining on Retail Dataset

## Purpose
The purpose of this lab was to explore and compare association rule mining techniques, specifically the Apriori and FP-Growth algorithms, on a publicly available retail transactional dataset. The lab aimed to develop practical skills in frequent itemset mining and rule generation, along with using visualization techniques to interpret discovered patterns. By applying these algorithms, we gained insights into customer purchasing behavior and the strengths and limitations of each mining approach.

## Key Insights
- **Data Preparation:**
  - Cleaning and filtering the dataset were critical to ensure accurate and efficient mining.
  - Filtering to the most frequent items reduced dimensionality and memory usage significantly.

- **Apriori Algorithm:**
  - Successfully identified frequent itemsets with support thresholds tailored to dataset size.
  - Apriori was straightforward but computationally expensive on larger itemsets due to candidate generation.

- **FP-Growth Algorithm:**
  - Produced frequent itemsets similar to Apriori but with much faster execution times.
  - More scalable for datasets with many transactions and items due to its compact FP-tree structure.

- **Association Rules:**
  - Generated rules with metrics like support, confidence, and lift, revealing meaningful item associations.
  - Visualization of confidence vs. lift helped identify strong and actionable rules for retail strategies.

- **Comparative Analysis:**
  - FP-Growth was consistently faster and more memory efficient than Apriori.
  - Both algorithms produced comparable frequent itemsets when using the same support thresholds.

## Challenges and Decisions
- **Memory Limitations:**
  - One-hot encoding the full dataset caused memory issues; resolved by filtering to top frequent items and using sparse data structures.

- **Support Threshold Selection:**
  - Needed iterative tuning of minimum support to balance between too many trivial patterns and too few meaningful ones.

- **Rule Thresholds:**
  - Setting confidence thresholds impacted the number and quality of generated rules; higher thresholds produced fewer but stronger rules.

- **Visualization Choices:**
  - Seaborn barplots and scatterplots were selected for their clarity in presenting frequent itemsets and rule metrics, facilitating pattern interpretation.

- **Trade-offs:**
  - Filtering items simplified computation but risked missing rare but potentially valuable patterns.
  - Apriori’s simplicity vs. FP-Growth’s efficiency highlighted the importance of algorithm choice based on dataset size and complexity.
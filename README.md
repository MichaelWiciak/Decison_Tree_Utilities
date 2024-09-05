# Decison_Tree_Utilities
The `decisionTree.py` script focuses on implementing a decision tree machine learning algorithm. The goal of this code is to enable classification by building a decision tree from a dataset, learning patterns from the data, and using that tree to predict outcomes for new examples.

### Key Functionalities:

1. **Dataset Management**:
   - The `DataSet` class manages loading and preprocessing of data, extracting features (attributes) and the target variable (what you want to predict). It handles the input of data either from a CSV file or directly via examples.
   - It allows sanitization of data to focus on relevant features and supports splitting the dataset for training and testing.

2. **Decision Tree Construction**:
   - The `DecisionTreeLearner` function is responsible for constructing the decision tree. It uses techniques like **information gain** to determine the best attributes for splitting the dataset into smaller, more homogenous groups, improving classification accuracy.
   - The tree is built recursively by creating decision forks (nodes) and decision leaves (terminal nodes), ensuring the model can classify new data based on learned patterns.

3. **Prediction and Evaluation**:
   - Once the tree is built, it can predict outcomes using the `__call__` methods in `DecisionFork` and `DecisionLeaf` classes. These methods classify new examples by traversing the decision tree based on feature values.
   - The script provides functions like `err_ratio` and `evaluate` to assess the performance of the decision tree by calculating the proportion of incorrect predictions (error rate).

4. **Splitting Data**:
   - The `train_test_split` function allows for the division of the dataset into training and testing subsets. This is essential for evaluating the generalization performance of the decision tree on unseen data.

5. **Plurality Learning and Baseline Comparison**:
   - The `PluralityLearner` serves as a baseline algorithm, always predicting the most common outcome from the training data, enabling comparison with more sophisticated models like the decision tree.

6. **Synthetic Data Generation**:
   - The script includes functions like `SyntheticRestaurant` and `SyntheticRestaurantTest` to generate synthetic datasets for testing and evaluating the decision tree algorithm in controlled scenarios.

7. **Tree Pruning**:
   - The script also incorporates functionality for **tree pruning** (via methods like `evaluate` and `replaceFork`). Pruning is used to remove branches that do not significantly improve predictions, reducing overfitting and improving the model's generalization.

This file enables the creation of a decision tree model that can be trained on a dataset, predict outcomes for unseen data, and optimize itself through pruning to maintain accuracy while minimizing complexity.

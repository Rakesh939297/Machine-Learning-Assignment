# Machine-Learning-Assignment
# Decision Trees and Overfitting Tutorial: Breast Cancer Classification

## Table of Contents
- Introduction
- Dataset
- Workflow
- Results and Visualizations
- License

---

## Introduction
This project demonstrates the use of Decision Tree Classifiers to classify breast cancer as Malignant (M) or Benign (B). It covers key aspects such as:

1. Building a Decision Tree Classifier.
2. Exploring overfitting by varying tree depths.
3. Optimizing the Decision Tree using hyperparameters like `max_depth` and `min_samples_split`.
4. Visualizing the decision tree and evaluating its performance.

## Dataset
The dataset used is the Breast Cancer Dataset, provided as a CSV file.

- **Features**: Measurements such as radius, texture, perimeter, area, and more.
- **Target**: The `diagnosis` column, where:
  - `M` → Malignant (1)
  - `B` → Benign (0)

## Workflow

1. Load and preprocess the dataset.
2. Split the data into training and testing sets.
3. Train a Decision Tree Classifier and evaluate its performance.
4. Visualize the decision tree and confusion matrix.
5. Explore overfitting using a deeper tree and mitigate it with optimized hyperparameters.
6. Plot accuracy vs. tree depth to illustrate overfitting and generalization.

## Results and Visualizations

### 1. Decision Tree Visualization
Displays the trained tree with features and decision rules, enabling better interpretability.

### 2. Confusion Matrix
A matrix illustrating the model's performance on test data, showing true positives, true negatives, false positives, and false negatives.

### 3. Depth vs. Accuracy
Plots training and testing accuracy against tree depth to show the impact of model complexity and overfitting.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

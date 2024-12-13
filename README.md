# Machine-Learning-Assignment
# Healthcare Dataset Analysis

This repository contains an analysis pipeline for the **healthcare-dataset-stroke-data**. The code performs data exploration, preprocessing, and builds a machine learning model to predict stroke occurrence.

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Dataset](#dataset)
- [Workflow](#workflow)
- [Results and Visualizations](#results-and-visualizations)
- [License](#license)

## Introduction
The project analyzes and preprocesses the healthcare dataset and builds a Random Forest Classifier to predict stroke occurrences. It handles missing values, categorical encoding, and addresses class imbalance using SMOTE.

## Prerequisites

Make sure you have the following libraries installed:

- pandas
- seaborn
- matplotlib
- numpy
- scikit-learn
- imbalanced-learn

You can install these dependencies using pip:

```bash
pip install pandas seaborn matplotlib numpy scikit-learn imbalanced-learn
```

## Dataset

The dataset used is `healthcare-dataset-stroke-data.csv`. Ensure this file is in the same directory as the script.

### Features:
1. Various patient details like gender, age, and BMI.
2. Health attributes like glucose levels, hypertension, and heart disease.
3. Target variable: `stroke` (1 for stroke occurrence, 0 otherwise).

## Workflow

1. **Load and Explore the Dataset:**
   - Display dataset structure, basic statistics, and check for missing values.
   
2. **Visualize Missing Data:**
   - Use heatmaps to display the distribution of missing data.

3. **Data Preprocessing:**
   - Fill missing BMI values with the mean.
   - Encode categorical variables using LabelEncoder.
   - Drop irrelevant columns (e.g., `id`) and handle anomalies (e.g., removing rows with gender `Other`).

4. **Feature Engineering:**
   - Generate correlation heatmaps for numeric variables.
   - Transform glucose levels using log transformation for better distribution.

5. **Class Imbalance Handling:**
   - Apply SMOTE to balance the target classes (`stroke`).

6. **Train-Test Split:**
   - Split the dataset into training and testing sets using `train_test_split`.

7. **Model Training:**
   - Train a Random Forest Classifier on the resampled dataset.

8. **Evaluation:**
   - Predict outcomes on the test set and evaluate using a confusion matrix.

## Results and Visualizations

1. **Correlation Heatmap:**
   - Displays the correlation between numerical features.

2. **Count Plots for Categorical Features:**
   - Visualizes the distribution of categorical variables.

3. **Confusion Matrix:**
   - Shows the model's performance on test data:

   ```python
   plt.figure(figsize=(8, 6))
   sns.heatmap(cm, annot=True, fmt='d', cmap='Blues', xticklabels=['No Stroke', 'Stroke'], yticklabels=['No Stroke', 'Stroke'])
   plt.title('Confusion Matrix')
   plt.xlabel('Predicted Label')
   plt.ylabel('True Label')
   plt.show()
   ```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Happy analyzing!

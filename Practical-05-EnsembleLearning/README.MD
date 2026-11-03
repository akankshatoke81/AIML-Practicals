# Ensemble Learning Techniques in Machine Learning

## Aim
To implement and compare different ensemble learning techniques such as Stacking, AdaBoost, and Voting Classifier by combining multiple base machine learning classifiers and evaluating their performance using classification metrics.

## Objectives
- Understand the concept of ensemble learning.
- Implement Stacking Ensemble using a meta-classifier.
- Implement AdaBoost Ensemble using weak classifiers.
- Implement Voting Ensemble using majority voting.
- Compare ensemble models with individual base classifiers.
- Evaluate models using accuracy, precision, recall, and F1-score.

## Dataset Description

**Dataset:** Breast Cancer Wisconsin Dataset

The dataset is available in the Scikit-learn library and is used to classify tumors as malignant or benign.

## Technologies Used
- Python
- Google Colab / Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

## Algorithms Implemented

### 1. Stacking Ensemble
Stacking combines multiple base classifiers using a meta-classifier.

**Base Classifiers:**
- Decision Tree
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

**Meta-Classifier:** Logistic Regression

**Working:**
1. Train multiple base classifiers.
2. Generate predictions using cross-validation.
3. Combine predictions into a new dataset.
4. Train the meta-classifier.
5. Generate the final prediction.

### 2. AdaBoost Ensemble
AdaBoost (Adaptive Boosting) combines multiple weak learners to create a strong classifier.

**Base Classifier:** Decision Stump (Decision Tree with maximum depth 1).

**Working:**
1. Assign equal weights to training samples.
2. Train the first weak classifier.
3. Identify incorrectly classified samples.
4. Increase the weights of incorrectly classified samples.
5. Train subsequent classifiers using updated weights.
6. Combine predictions using weighted voting.

### 3. Voting Ensemble
Voting combines predictions from multiple independent classifiers using majority voting.

**Base Classifiers:**
- Decision Tree
- KNN
- SVM

**Working:**
1. Train all base classifiers independently.
2. Generate predictions from each classifier.
3. Count the votes for each class.
4. Select the class receiving the maximum votes.
5. Generate the final prediction.

**Voting Method:** Hard Voting (Majority Voting).

## Base Machine Learning Models
The following individual classifiers are also implemented for comparison:

1. Decision Tree Classifier
2. K-Nearest Neighbors (KNN)
3. Support Vector Machine (SVM)

## Performance Evaluation Metrics

The performance of all models is evaluated using the following metrics:

- **Accuracy:** Measures the percentage of correctly classified predictions.
- **Precision:** Measures how many predicted positive samples are actually positive.
- **Recall:** Measures how many actual positive samples are correctly identified.
- **F1-Score:** Harmonic mean of precision and recall.

## Observations

1. Decision Tree shows comparatively lower performance than the other models.
2. KNN achieves good performance across all evaluation metrics.
3. SVM provides high accuracy and balanced classification results.
4. Stacking achieves the highest recall, approximately 1.00.
5. AdaBoost provides high recall but comparatively lower precision.
6. Voting achieves balanced performance across all four evaluation metrics.
7. Overall, Stacking and Voting demonstrate strong classification performance.

## Result

Stacking, AdaBoost, and Voting ensemble techniques were successfully implemented using Python and Scikit-learn. Their performance was compared with individual classifiers using accuracy, precision, recall, and F1-score.
The experiment demonstrates that ensemble learning can combine the strengths of multiple classifiers and provide reliable classification performance.

## Conclusion

In this practical, different ensemble learning techniques were implemented and evaluated. Stacking uses a meta-classifier, AdaBoost focuses on incorrectly classified samples, and Voting combines predictions through majority voting. The results show that ensemble techniques can provide better and more balanced classification performance depending on the dataset and model configuration.

## Future Scope

- Implement Random Forest and Gradient Boosting.
- Experiment with Soft Voting.
- Apply hyperparameter tuning.
- Test ensemble models on different datasets.
- Use cross-validation for more reliable evaluation.
- Compare computational time and model performance.

## How to Run the Project

1. Clone or download the repository.
2. Open the project in Google Colab or Jupyter Notebook.
3. Install the required libraries if they are not already installed:
pip install numpy pandas matplotlib scikit-learn
4. Open the Python notebook.
5. Run all cells sequentially.
6. Observe the classification reports, comparison table, and performance graph.


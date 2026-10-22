Classification Algorithms: Comparative Analysis

Overview
This practical implements and compares four supervised machine learning
classification algorithms using Python and the Iris flower dataset:
- Support Vector Machine (SVM)
- Decision Tree
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes
The models are evaluated using accuracy, precision, recall, F1-score,
and log loss.

Objectives
- Understand the working principles of common classification
  algorithms.
- Train and test SVM, Decision Tree, KNN, and Naive Bayes models.
- Evaluate the models using standard classification metrics.
- Compare the results and discuss the suitability of each algorithm.
  
Dataset
The Iris dataset is included in Scikit-learn, so no separate dataset
download is required.
- Samples: 150
- Features: 4
- Classes: 3
- Input features: sepal length, sepal width, petal length, and
  petal width
- Target classes: Iris setosa, Iris versicolor, and Iris virginica
The dataset is split into 80% training data and 20% testing data.
Stratified splitting is used to preserve class proportions.

Algorithms
1. SVM: Finds a decision boundary that separates classes; feature
   scaling is applied.
2. Decision Tree: Learns decision rules by splitting data based on
   feature values.
3. KNN: Predicts a class using the majority class among the five
   nearest training samples; feature scaling is applied.
4. Gaussian Naive Bayes: Predicts classes using Bayes' theorem and
   a Gaussian feature-distribution assumption.
   
Evaluation Metrics
- Accuracy: Fraction of predictions that are correct.
- Precision: Measures how many predicted class assignments are
  correct; this project reports weighted precision.
- Recall: Measures how many actual examples are correctly
  identified; this project reports weighted recall.
- F1-score: Harmonic mean of precision and recall; this project
  reports weighted F1-score.
- Log loss: Measures the quality of predicted class probabilities.
  Lower values are better.
  
Requirements
- Python 3.9 or later recommended
- NumPy
- pandas
- scikit-learn
Install dependencies:
python -m pip install numpy pandas scikit-learn

How to Run
1. Save the Python program as classification.py.
2. Open a terminal in the folder containing the file.
3. Install the dependencies using the command above.
4. Run:
python classification.py
The program prints each algorithm's metrics and predictions, followed by
a comparison table and a short interpretation of the results.

Example Results
The following values are the results previously reported for the
configured run. Run the program in your environment to verify the
results.

  Algorithm         Accuracy   Precision   Recall   F1-score   Log loss
  SVM                 0.9667      0.9697   0.9667     0.9666     0.1125
  Decision Tree       0.9333      0.9333   0.9333     0.9333     2.4029
  KNN                 0.9333      0.9444   0.9333     0.9327     0.1196
  Naive Bayes         0.9667      0.9697   0.9667     0.9666     0.1420

Interpretation: In the reported run, SVM and Naive Bayes had the
highest accuracy (96.67%). SVM had the lowest log loss. Results can vary
with library versions or changes to model settings.

Conclusion
This practical demonstrates how four classification algorithms can be
trained and compared on the same dataset. Using multiple metrics
provides a more complete view of model performance and helps select an
algorithm based on the requirements of a classification task.

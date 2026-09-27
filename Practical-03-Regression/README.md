# Practical Assignment-03: Performance Evaluation of Regression Model

## Application: House Price Prediction using Regression

This practical implements **Linear Regression** and **Gradient Descent-based Linear Regression** for predicting house prices.
A synthetic but realistic dataset is generated within the Python program, so the practical is **fully self-contained** and does not require downloading an external dataset.

## Objectives

* Develop a regression model for a real-world application.
* Predict house prices using different input features.
* Evaluate the performance of the regression model using appropriate metrics.
* Implement Gradient Descent manually for Linear Regression.
* Analyze the convergence of Gradient Descent using a cost-vs-iterations graph.
* Compare the performance of standard Linear Regression and Gradient Descent Regression.


## Technologies and Libraries Used

* **Python 3**
* **NumPy** – numerical computations
* **Pandas** – dataset creation and data handling
* **Matplotlib** – visualization and graph generation
* **Scikit-learn** – machine learning model, preprocessing, and evaluation

### Required Libraries
pip install numpy pandas matplotlib scikit-learn


## Dataset

The dataset is generated automatically when the program is executed.

It contains **300 house records** with the following features:

| Feature     | Description                      |
| ----------- | -------------------------------- |
| `area`      | Area of the house in square feet |
| `bedrooms`  | Number of bedrooms               |
| `bathrooms` | Number of bathrooms              |
| `age`       | Age of the house in years        |
| `price`     | House price (target variable)    |

The dataset is generated using a fixed random seed:
np.random.seed(42)

This ensures that the same dataset is generated every time the program is executed.

### Price Generation

The house price is generated using the following relationship:
Price = 50000
      + 120 × Area
      + 15000 × Bedrooms
      + 10000 × Bathrooms
      - 800 × Age
      + Noise
Random noise is added to make the dataset more realistic.


## Machine Learning Workflow

Create Dataset
      ↓
Data Preprocessing
      ↓
Train-Test Split
      ↓
Linear Regression
      ↓
Performance Evaluation
      ↓
Feature Scaling
      ↓
Manual Gradient Descent
      ↓
Performance Evaluation
      ↓
Generate Graphs
      ↓
Compare Results


## Models Implemented

### 1. Linear Regression

The first model uses the `LinearRegression` implementation provided by Scikit-learn.
lr_model = LinearRegression()
lr_model.fit(X_train, y_train)
y_pred_lr = lr_model.predict(X_test)

The model uses:

* Area
* Number of bedrooms
* Number of bathrooms
* Age of the house

to predict the house price.

### 2. Linear Regression using Gradient Descent

Gradient Descent is implemented manually without using a built-in Gradient Descent regression model.

The algorithm:

1. Initializes weights and bias.
2. Calculates predicted values.
3. Calculates the error.
4. Calculates the cost.
5. Calculates gradients.
6. Updates weights and bias.
7. Repeats the process for the specified number of iterations.

The implementation uses:
Learning Rate = 0.05
Iterations = 1000
Feature scaling using `StandardScaler` is performed before Gradient Descent to improve convergence.


## Graphs Generated

The program automatically generates three PNG graphs.

### 1. Actual vs Predicted House Price

**File:**

fig1_actual_vs_predicted.png

This graph compares the actual house prices with the prices predicted by the Linear Regression model.

The dashed diagonal line represents the ideal situation where:

Actual Price = Predicted Price


### 2. Regression Line: Area vs Price

**File:**

fig2_regression_line.png

This graph shows the relationship between house area and price.

It contains:

* Actual house-price data points
* A regression line representing the relationship between area and price


### 3. Gradient Descent Cost vs Iterations

**File:**

fig3_cost_vs_iterations.png

This graph shows how the cost function changes during Gradient Descent iterations.

A decreasing cost indicates that the optimization process is converging toward a solution.


## How to Run

### Using Jupyter Notebook

1. Open Jupyter Notebook.
2. Open the Python/Notebook file.
3. Run all cells.
4. The dataset will be generated automatically.
5. The regression models will be trained.
6. Evaluation metrics will be displayed.
7. The three graphs will be saved automatically.

### Using Google Colab

1. Open Google Colab.
2. Upload the Python notebook or paste the code.
3. Run all cells.
4. The dataset and graphs will be generated during execution.
5. The generated PNG files can be found in the Colab Files section.

### Using VS Code

Install the required libraries:
pip install numpy pandas matplotlib scikit-learn

Run:
python regression.py


## Expected Output

The program displays:

* First five rows of the generated dataset
* Missing-value information
* Linear Regression performance
* Gradient Descent Regression performance
* Final Gradient Descent cost
* Comparison table of both approaches

The final comparison contains:

| Model                       |                        MAE |                        MSE |                       RMSE |                         R² |
| --------------------------- | -------------------------: | -------------------------: | -------------------------: | -------------------------: |
| Linear Regression           | Generated during execution | Generated during execution | Generated during execution | Generated during execution |
| Gradient Descent Regression | Generated during execution | Generated during execution | Generated during execution | Generated during execution |

The exact values may depend on the dataset generation and program configuration.



## Gradient Descent Parameters

| Parameter       |          Value |
| --------------- | -------------: |
| Learning Rate   |           0.05 |
| Iterations      |           1000 |
| Initial Weights |              0 |
| Initial Bias    |              0 |
| Feature Scaling | StandardScaler |



## Key Observations

* Linear Regression provides a baseline model for house-price prediction.
* Gradient Descent can be used to learn the regression parameters iteratively.
* Feature scaling helps Gradient Descent converge smoothly.
* The cost generally decreases as the number of iterations increases.
* MAE, MSE, and RMSE measure prediction error, while R² measures the model's ability to explain variation in house prices.
* The two approaches can be compared using their test-set evaluation metrics.



## Conclusion

This practical demonstrates the use of regression for a real-world **house price prediction** problem. A standard Linear Regression model was implemented using Scikit-learn, and Linear Regression was also optimized manually using Gradient Descent.
The models were evaluated using **MAE, MSE, RMSE, and R² score**. Visualization of actual versus predicted prices, the regression relationship between area and price, and Gradient Descent cost reduction helps in understanding model performance and optimization.
The practical also demonstrates how a complete machine learning workflow can be implemented using Python, from dataset generation and preprocessing to model training, evaluation, and visualization.



# Linear Regression with Gradient Descent

## Overview

This project implements linear regression using gradient descent from scratch in Python, as part of CS-6470 homework. The code demonstrates how to fit a linear model to a small dataset with two features, visualize the results, and understand the underlying optimization process.

## Data Preparation

- The dataset is a small, synthetic set:
  ```python
  X = np.array([[1, 1], [1, 2], [2, 2], [2, 3]])
  y = np.dot(X, np.array([1, 2])) + 3
  ```
- `X` contains two features per instance.
- `y` is generated using a known linear relationship for validation.

## Model: Linear Regression Using Gradient Descent

- The model initializes weights (`m`) and bias (`c`) to zero.
- Gradient descent is performed for a set number of iterations (`n_iterations`), updating weights and bias to minimize the mean squared error.
- The update rules are vectorized for efficiency and correctness with multiple features.

## Visualization

- The code visualizes the actual vs. predicted values using the second feature for clarity.
- A scatter plot shows the true data, and a line plot shows the model's predictions.

## Notes & Learning

- **Gradient Descent**: Iteratively updates weights and bias to minimize loss.
- **Initialization**: Weights and bias start near zero.
- **Loss Calculation**: Uses mean squared error.
- **Update Direction**: Gradients indicate how to adjust weights and bias to reduce loss.
- **Convergence**: The process repeats until the model cannot reduce the loss further.

## Performance



## Comparison with Other Models

- The gradient descent implementation achieves the same performance as scikit-learn's `LinearRegression` on this dataset.

## Challenges

- **Vectorization**: Adapting the gradient descent update rules to handle multiple features required careful use of numpy operations.
- **Visualization**: With more than one feature, plotting predictions meaningfully required selecting a single feature for the x-axis.
- **Debugging**: Ensuring the gradients and updates were correct for multi-feature data was non-trivial.
- **Convergence**: Choosing appropriate learning rates and iteration counts was important to ensure the model converged.


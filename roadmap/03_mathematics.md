# 📘 Mathematics for Data Science

Mathematics is the backbone of Data Science and Artificial Intelligence. Understanding the core concepts of linear algebra, calculus, probability, and statistics is crucial for building and applying machine learning algorithms. This section covers the essential mathematical concepts you need to excel in Data Science.

---

## Table of Contents
1. [Linear Algebra](#linear-algebra)
2. [Calculus](#calculus)
3. [Probability](#probability)
4. [Statistics](#statistics)
5. [Applications in Data Science](#applications-in-data-science)

---

## Linear Algebra

Linear Algebra is essential for understanding how machine learning algorithms work, especially for algorithms like Principal Component Analysis (PCA) or Singular Value Decomposition (SVD). Some important concepts include:

- **Vectors and Matrices**: Understanding the representation of data in matrix format.
- **Matrix Operations**: Addition, subtraction, multiplication of matrices.
- **Determinants and Inverses**: Key properties used in optimization.
- **Eigenvalues and Eigenvectors**: Used in PCA for dimensionality reduction.

Example in Python (using NumPy):

```python
import numpy as np

# Creating a 2x2 matrix
matrix = np.array([[2, 3], [5, 6]])

# Finding determinant
det = np.linalg.det(matrix)

# Finding eigenvalues and eigenvectors
eigenvalues, eigenvectors = np.linalg.eig(matrix)

print(f"Determinant: {det}")
print(f"Eigenvalues: {eigenvalues}")
```
## Calculus

Calculus helps with optimization techniques used in training machine learning models. Gradient descent, a key optimization algorithm, is based on the principles of calculus.

**Key Concepts:**

- **Derivatives:** Measure the rate of change; used in optimization.
- **Integrals:** Used in finding areas under curves, important in probability distributions.
- **Gradients:** Multidimensional derivatives used for finding optimal solutions in machine learning.
Gradient Descent Example:

```python
# Gradient Descent Algorithm
def gradient_descent(x, y, lr=0.01, iterations=100):
    m = b = 0  # initial parameters
    n = len(x)
    
    for _ in range(iterations):
        y_pred = m * x + b
        m_gradient = (-2/n) * sum(x * (y - y_pred))
        b_gradient = (-2/n) * sum(y - y_pred)
        m -= lr * m_gradient
        b -= lr * b_gradient
        
    return m, b
```

---

## Probability
Probability theory is used to make predictions and handle uncertainty in machine learning models. Key concepts include:

- **Random Variables**: Variables that take on different values based on an experiment.
- **Probability Distributions:** Describes how probabilities are distributed over values.
- **Bayes' Theorem:** Widely used in classification problems.
- **Conditional Probability**: The probability of one event occurring given that another has occurred.
Example of calculating probabilities:

```python
# Calculating simple probability
p_a = 0.3  # Probability of event A
p_b = 0.6  # Probability of event B

# Probability of A and B happening
p_a_and_b = p_a * p_b
print(f"Probability of both A and B: {p_a_and_b}")
```
---

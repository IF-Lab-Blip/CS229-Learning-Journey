# Lecture 02 - Linear Regression

## What I covered today
- Hypothesis function for Linear Regression
- Cost Function (MSE) - why we use it
- Gradient Descent intuition
- Learning rate and how it affects convergence

## Key Notes

**1. Hypothesis:**
h(x) = theta0 + theta1 * x
We try to find best theta values.

**2. Cost Function:**
We use Mean Squared Error to measure how wrong our prediction is.
Goal is to minimize J(theta0, theta1).

**3. Gradient Descent:**
Start with random thetas, then take small steps downhill to find minimum cost.
Update rule: theta_j := theta_j - alpha * d/d(theta_j) J(theta)

- alpha is the learning rate. Too big = overshoot, too small = slow.
- Need to update thetas simultaneously.

**4. My understanding:**
Linear regression looks simple but the idea of minimizing cost with gradient descent is the core of almost all ML. Got more clarity on why we don't just solve it directly.

Next: Will implement gradient descent in Python from scratch.

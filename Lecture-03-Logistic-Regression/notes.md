# Lecture 03 - Weighted Regression, Logistic Regression

## What I covered today
- Problem of Underfitting and Overfitting
- Locally Weighted Regression (LWR)
- Probabilistic interpretation of Linear Regression
- Why we use Gaussian for errors
- Introduction to Logistic Regression for classification
- Newton's Method as an alternative to Gradient Descent

## Key Notes

**1. Underfitting / Overfitting:**
If model is too simple -> underfitting. Too complex -> overfitting. Need balance.

**2. Locally Weighted Regression (LWR):**
- Parametric vs Non-parametric. LWR is non-parametric, keeps entire training set.
- Gives more weight to points close to query point x.
- Weight: w(i) = exp( - (x(i) - x)^2 / 2*tau^2 )
- Tau is bandwidth parameter.

**3. Probabilistic Interpretation:**
- Why squared error? Assumed errors are Gaussian (Normal) distribution.
- We did Maximum Likelihood Estimation (MLE).
- This gave same result as minimizing MSE.

**4. Logistic Regression:**
- For classification (y = 0 or 1). Can't use linear regression.
- Hypothesis: h(x) = sigmoid(theta^T * x) = 1 / (1 + exp(-theta^T * x))
- Sigmoid squashes output between 0 and 1.
- Cost function is now different (Log Loss) because MSE would be non-convex.

**5. My Understanding:**
Today I understood WHY we use certain cost functions, not just HOW. Logistic regression is actually regression but used for classification. Newton's method converges faster than gradient descent but is expensive.

Next: Will implement Sigmoid and Logistic cost function in Python.

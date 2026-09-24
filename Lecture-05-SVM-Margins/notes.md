# Lecture 05 - Naive Bayes Revisited & Support Vector Machines

## What I covered today
- Laplace Smoothing in detail for Naive Bayes
- Multivariate Event Model vs Bernoulli for text
- Optimal Margin Classifier intuition
- Functional Margin vs Geometric Margin
- Support Vector Machines (SVM) formulation
- Lagrange Duality idea intro

## Key Notes

**1. Naive Bayes for Spam - Practical Issues:**
- We used Multinomial event model for text classification.
- Problem: if a word never seen in training for a class, p(word|class) = 0 and whole product becomes 0.
- Solution: Laplace Smoothing (add-1 smoothing) -> p = (count + 1) / (total + |V|). |V| is vocab size.
- Solves zero probability problem.

**2. Optimal Margin Classifier:**
- For SVM, we want a separator that not just separates, but separates with maximum gap.
- Intuition: More confident separation -> better generalization.

**3. Functional vs Geometric Margin:**
- Functional margin: y*(theta^T * x + b). It can be made large by scaling theta, so not reliable.
- Geometric margin: Actual Euclidean distance from point to hyperplane = Functional margin / ||theta||.
- We want to maximize Geometric margin.

**4. Support Vector Machines:**
- Optimization problem: Maximize geometric margin = minimize 1/2 * ||w||^2 subject to y(i)(w^T x(i) + b) >= 1
- This is a convex quadratic optimization problem.
- Only few points will have equality y(i)(w^T x + b) = 1. These are SUPPORT VECTORS. They define the boundary.
- SVM is less sensitive to outliers compared to logistic regression because it only cares about points near boundary.

**5. Lagrange Duality (Intro):**
- To solve constrained optimization efficiently, we will convert primal problem to dual problem.
- This will later allow us to use Kernels.

**My Understanding:**
Laplace smoothing is a small trick but very important in real projects. SVM ka main idea is simple: widest road between two classes. Support vectors are the only important points. Today I understood why SVM is considered so robust.

Next: Will study Lagrange duality in detail and implement SVM from scratch for simple data.

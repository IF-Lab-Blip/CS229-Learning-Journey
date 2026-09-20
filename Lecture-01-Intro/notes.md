# Lecture 01: Introduction to Machine Learning
Date: September 20, 2026
Course: Stanford CS229 - Andrew Ng

### Overview
This was an introductory lecture. Focused on what machine learning is, why it's important now, and the main types of learning problems.

### What is Machine Learning?
Definition by Arthur Samuel (1959):
"Field of study that gives computers the ability to learn without being explicitly programmed."

In simple terms - we give data to an algorithm and it learns patterns to make predictions.

### Why ML is booming now?
- Huge amount of data available
- Better algorithms
- More computing power (GPUs)
- Growth of IoT and sensors

### Types of Machine Learning

**1. Supervised Learning**
We have labeled data. We know the right answer for each example.
- x = input, y = output
- Goal: Learn mapping from x -> y

Two sub-types:
- Regression: Predict continuous value (e.g., house price based on size)
- Classification: Predict discrete category (e.g., email spam or not spam)

**2. Unsupervised Learning**
We only have x, no labels. The algorithm has to find structure by itself.
- Example: Clustering - grouping similar news articles together
- Example: Anomaly detection, Dimensionality reduction

### Key Terms from Lecture
- Training Set: Data used to train the model
- Learning Algorithm: The algorithm that learns from data
- Hypothesis: The model/function that makes predictions

### My Takeaway
ML is not magic. It's just data + a well-defined objective + optimization.
Supervised vs Unsupervised is the first big distinction. Next lectures will go into linear regression and how we actually train these models.

Next Up: Lecture 02 - Linear Regression, Cost Function, Gradient Descent

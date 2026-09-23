# Lecture 04 - GLM, GDA and Naive Bayes

## What I covered today
- Exponential Family
- Generalized Linear Models (GLM)
- Softmax Regression
- Generative vs Discriminative models
- Gaussian Discriminant Analysis (GDA)
- Naive Bayes

## Key Notes

**1. Exponential Family:**
A class of distributions that can be written in a specific form. Includes Gaussian, Bernoulli, Multinomial. Most of our models belong to this.

**2. Generalized Linear Models (GLM):**
We make 3 assumptions to derive GLM. Logistic regression and Linear regression are both special cases of GLM. Clean way to generate models.

**3. Generative vs Discriminative:**
- Discriminative: directly learns p(y|x) — e.g., Logistic Regression. Learns decision boundary.
- Generative: learns p(x|y) and p(y) and then uses Bayes rule to get p(y|x) — e.g., GDA, Naive Bayes.
- Discriminative is usually better if data is large. Generative works better with less data and can handle missing features.

**4. Gaussian Discriminant Analysis (GDA):**
- Generative model. Assumes p(x|y) is Gaussian (Multivariate Normal).
- We assume both classes have same covariance matrix but different means.
- Decision boundary comes out to be linear! Similar to logistic regression but assumptions are different.

**5. Naive Bayes:**
- Also generative. Makes strong assumption: features x_i are conditionally independent given y.
- p(x1,x2,...|y) = p(x1|y) * p(x2|y) * ...
- Despite being a very strong (and wrong) assumption, it works amazingly well for text classification / spam detection.
- Laplace smoothing to avoid zero probabilities.

**My Understanding:**
Today I finally understood difference between Generative and Discriminative. GDA and Logistic both give linear boundary but GDA makes stronger assumptions about data. If those assumptions are true, GDA needs less data. Naive Bayes is simple but powerful for spam/emails.

Next: Will implement GDA and compare with Logistic Regression.

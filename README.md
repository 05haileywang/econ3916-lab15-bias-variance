# econ3916-lab15-bias-variance

# The Bias-Variance Tradeoff: Choosing How Flexible a Model Should Be

## Objective
The goal of this lab was to understand how model complexity affects prediction accuracy and how to choose a model that performs well on new data.

## Methodology
- Generated simulated data with a known relationship between x and y
- Compared polynomial models of different degrees to understand bias and variance
- Compared training error with prediction error on 2,000 new observations
- Used 5-fold cross-validation to select the best polynomial degree
- Used nested cross-validation to see whether the original cross-validation results were too optimistic
- Created a function to calculate cross-validation error for different polynomial degrees and numbers of folds
- Explored double descent by testing models with very high polynomial degrees

## Key Findings
- Increasing model complexity initially reduced bias, but also increased the risk of overfitting
- Training error continued to decrease as models became more complex, even when prediction accuracy became worse
- Degree 5 had the lowest held-out prediction error
- 5-fold cross-validation selected degree 4, with an MSE of 0.1401
- Nested cross-validation produced a higher MSE of 0.2070, suggesting that selecting the lowest cross-validation error can make a model appear better than it actually is
- In the challenge, the degree 40 polynomial had a test MSE of approximately 155.155
- My double descent graph showed that prediction error increased dramatically before decreasing again as model complexity increased, although it remained higher than for simpler models

## Conclusion
This lab showed me that more complicated models are not necessarily better at making predictions. While complex models can fit training data closely, they may perform poorly on new observations. Cross-validation helps identify a model that balances complexity with prediction accuracy. The double descent challenge also showed that prediction error does not always follow a simple U-shaped curve.

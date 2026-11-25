# econ5200-lab16-regularization
# Regularization: Selection, Shrinkage and Valid Intervals

## Objective

I studied how LASSO variable selection and coefficient shrinkage affect causal estimation and statistical inference.

## Methodology

- Simulated a treatment effect of 1.0 with 100 candidate controls.
- Evaluated post-selection OLS confidence intervals across 200 simulated samples.
- Applied double selection to identify controls related to both the outcome and treatment.
- Compared LASSO coefficients with true coefficients and post-LASSO OLS estimates.
- Implemented cross-validation to select lambda, fitting the scaler inside each fold.

## Key Findings

- Naive post-selection OLS achieved only 82.5% coverage instead of the nominal 95%.
- Double selection improved coverage to 88.5%, retaining 26.5 controls on average.
- LASSO produced an average coefficient shrinkage of 4.6%. Post-LASSO OLS reduced this shrinkage.
- My cross-validation function matched GridSearchCV, selecting lambda = 0.0501 with a CV MSE of 1.0173.

These results show why LASSO coefficients should not be directly interpreted as causal effects and why variable selection matters for statistical inference.

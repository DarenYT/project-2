# Project 2
<br>
<br>

## Problem Statement 
Location, location, location! You have been commissioned by a real estate company that prides itself on its statement that location is the second-most important feature/predictor (after size) and have modelled their price predictive model based on this. 

<br>

## Our objectives:
1) Show if location is really the second most important feature/predictor after size (using corr graph, heatmap, prove with lasso regression reducing the coeff to 0, see which is left), and if it isn't, show which feature/predictor actually is

<br>

## Methodology:

### Location not the second most important feature
2(a) If location isn't the second most important feature/predictor after size, identify the feature/predictor that is and prove that it makes for a better model
- Compare their current predictive model (price as a function of size and location) with our predictive model (price as a function of size, location, whichever other feature/predictor that was fouind to be the second most important in determining price in part 1) to show that incorporating more/other features/predictors can help their business make better/more accurate predictions

### Location is the second most important feature
2(b) If location really is the second most important feature/predictor after size, show that their existing model can be improved by incorporating other features/predictors into their model
- Compare their current predictive model (price as a function of size and location) with our predictive model (price as a function of size, location, whatever other features/predictors we think would help from our lasso regression in part 1) to show that incorporating more/other features/predictors can help their business make better/more accurate predictions

### Method of comparison
Compare the two models using
- the best regression model between linear, ridge, lasso, elastic net
 - based on the model's
  - cross val score
  - the MSE of the training set
  - the MSE of the testing set
- jointplot of residuals of each model to show which one is more centered around 0
- maybe predicted vs actual output graphs of each model to show which one has a closer OLS to y=x

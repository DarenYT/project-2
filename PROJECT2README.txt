# Project 2
<br>
<br>
**Code should take about 3 minutes to run**
<br>
<br>

## Problem Statement 
Location, location, location! You have been commissioned by a real estate company that prides itself on its statement that 
location is the second-most important feature/predictor (after size) and have modelled their price predictive model based on this.
 Prove or disprove their model with the Ames housing dataset

<br>

## Our objectives:
1) Show if location is really the second most important feature/predictor after size (using corr graph, heatmap, prove with 
lasso regression reducing the coeff to 0, see which is left), and if it isn't, show which feature/predictor actually is.

<br>

### Location not the second most important feature
2(a) If location isn't the second most important feature/predictor after size, identify the feature/predictor that is and prove 
that it makes for a better model
- Compare their current predictive model (price as a function of size and location) with our predictive model (price as a 
function of size, location, whichever other feature/predictor that was fouind to be the second most important in determining 
price in part 1) to show that incorporating more/other features/predictors can help their business make better/more accurate 
predictions

### Location is the second most important feature
2(b) If location really is the second most important feature/predictor after size, show that their existing model can be 
improved by incorporating other features/predictors into their model
- Compare their current predictive model (price as a function of size and location) with our predictive model (price as a 
function of size, location, whatever other features/predictors we think would help from our lasso regression in part 1) to 
show that incorporating more/other features/predictors can help their business make better/more accurate predictions

## Method of comparison
Compare the two models using
- the best regression model between linear, ridge, lasso, elastic net
 - based on the model's
  - cross val score
  - the MSE of the training set
  - the MSE of the testing set
- jointplot of residuals of each model to show which one is more centered around 0
- predicted vs actual output graphs of each model to show which one has a closer OLS to y=x

## Data Dictionary

#### Location
1) `MS Zoning` (Nominal): Identifies the general zoning classification of the sale<br>
2) `Neighborhood` (Nominal): Physical locations within Ames city limits (map available)<br>
3) `Condition 1` (Nominal): Proximity to various conditions<br>
4) `Condition 2` (Nominal): Proximity to various conditions (if more than one is present)<br>


#### Structural Construction Materials and Updates
5) `Overall Qual` (Ordinal): Rates the overall material and finish of the house<br>


#### Age of the Home
6) `Year Built` (Discrete): Original construction date<br>

#### Design Style of the Home
7) `MS SubClass` (Nominal): Identifies the type of dwelling involved in the sale<br>
8) `House Style` (Nominal): Style of dwelling<br>

#### Curb Appeal
9) `Lot Frontage` (Continuous): Linear feet of street connected to property<br>
10) `Lot Config` (Nominal): Lot configuration<br>

#### Number of Bedrooms
11) `Bedroom Abvgr` (Discrete): Bedrooms above grade (does NOT include basement bedrooms)

#### Number of Bathrooms
12) `Bsmt Full Bath` (Discrete): Basement full bathrooms<br>
13) `Bsmt Half Bath` (Discrete): Basement half bathrooms<br>
14) `Full Bath` (Discrete): Full bathrooms above grade<br>
15) `Half Bath` (Discrete): Half baths above grade<br>

#### Square Footage
16) `Low Qual Fin SF` (Continuous): Low quality finished square feet (all floors)<br>
17) `Total Bsmt SF` (Continuous): Total square feet of basement area<br>
18) `Lot Area` (Continuous): Lot size in square feet<br>
19) `Gr Liv Area` (Continuous): Above grade (ground) living area square feet<br>

#### Heat and Air
20) `Central Air` (Nominal): Central air conditioning<br>
21) `Heating`	(Nominal): Type of heating<br>
22) `Utilities` (Ordinal): Type of utilities available<br>

#### Garage Space
23) `Garage Area` (Continuous): Size of garage in square feet<br>

#### Recent Home Renovations
24) `Year Remod/Add` (Discrete): Remodel date (same as construction date if no remodeling or additions)<br>
25) `Overall Cond` (Ordinal): Rates the overall condition of the house<br>

#### Comps
26) `Bldg Type` (Nominal): Type of dwelling<br>
27) `Pool QC` (Ordinal): Pool quality<br>

## Conclusion

For this particular dataset, LLL's predictive model using just location and living area was not very effective at accurately 
predicting the home values. The only location feature that showed to have any level of predictive power on the level of our other
 features such as the overall quality and the age of the house was `neighborhood` and even that was not very significant

## Sources
1) Factors influencing house price(1): https://www.opendoor.com/w/blog/factors-that-influence-home-value<br><br>
2) Factors influencing house price(2): https://www.moving.com/tips/7-key-factors-that-impact-the-value-of-your-home/<br><br>
3) Factors influencing house price(3): https://blog.bhhsmichiganrealestate.com/13-factors-that-determine-your-home-appraisal-value/<br><br>
4) Ames population density: https://www2.census.gov/programs-surveys/decennial/2020/data/01-Redistricting_File--PL_94-171/Iowa/<br><br>
5) New York City population density: https://www.census.gov/quickfacts/fact/table/newyorkcitynewyork/POP010220<br><br>
6) Factors of a good property location: https://www.investopedia.com/financial-edge/0410/the-5-factors-of-a-good-location.aspx<br>
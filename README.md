![seattle_banner](./Images/seattle_banner.jpg)

# Analyzing House Sales and Price Indicators in King County, WA

## Business Understanding

For this project, I used regression modeling to analyze house sales in King County, which is located in the U.S. state of Washington. The population was 2,269,675 in the 2020 census, making it the most populous county in Washington, and the 12th-most populous in the United States. The county seat is Seattle, also the state's most populous city.

Not all home improvements are created equally, so how do you choose between remodeling your kitchen or adding wood floors? How much would adding a bedroom or bathroom actually increase your home value?

This project seeks to advise homeowners about how home renovations might increase the estimated value of their homes.

## Data & Methods

This project uses the King County House Sales dataset, which includes 21,597 observations with 21 variables

The data includes many different types of information about each home sale in the County, including selling price, square footage, property type (waterfront or not), ZIP code, etc.

For this project, I used regression modeling to analyze house sales in King County, which is located in the U.S. state of Washington.


## Model

We interated through several models before arriving at a final model. We concluded with an R-squared value of 0.833 and an Adj. R-squared of 0.0832. Adj. R-squared describes the quality that your model’s R-squared value will never go down with additional variables, only equal or higher. Therefore, this model could look more accurate with multiple variables even if they are poorly contributing. The adjusted R-squared penalizes the R-squared formula based on the number of variables, therefore a lower adjusted score may be telling you some variables are not contributing to your model’s R-squared properly. There is a 0.001 difference in Model 3.

P>|t| is one of the most important statistics in the summary. It uses the t statistic to produce the p value, a measurement of how likely your coefficient is measured through our model by chance. The p value of 	0.531 for yr_built is saying there is a 53.1% chance the yr_built variable has no affect on the dependent variable, home Price, and our results are produced by chance.

Omnibus describes the normalcy of the distribution of our residuals using skew and kurtosis as measurements. A 0 would indicate perfect normalcy. Prob(Omnibus) is a statistical test measuring the probability the residuals are normally distributed. A 1 would indicate perfectly normal distribution. Skew is a measurement of symmetry in our data, with 0 being perfect symmetry. Kurtosis measures the peakiness of our data, or its concentration around 0 in a normal curve. Higher kurtosis implies fewer outliers.

A change of 1 standard deviation in X is associated with a change of β standard deviations of Y. 

For model 3, the dependent variable is log transformed and our independendent variables have been normalized. Log transforms typically help strengthen the linearity between features and the target. Interpret the coefficient as the percent increase in the dependent variable for every 1 standard deviation increase in the independent variable. Example: the coefficient of sqft_above is 0.196047. For every 1 standard deviation increase in the independent variable, our dependent variable (price) increases by about 0.20%. For x percent increase, calculate 1.x to the power of the coefficient, subtract 1, and multiply by 100. Example: For every 20% increase in the independent variable, our dependent variable increases by about (1.20^ 0.196047 – 1) * 100 = 3.6 percent.

## Conclusions and Next Steps

**Location, location, location**
* It's become an almost hackneyed phrase, but it still has meaning
* Where a home is located is the most important factor in it's value -- both now and in the future.

**Square Footage Matters**
* The top ~30 most important parameters refer to ZIP codes, but square footage contributes to value too.

Finally, we built a model that is fairly predictive of price with a R-squared of 0.833. The final model included 82 features, most of which are dummy variables for zipcodes. We can interpret the RMSE as the mean error in USD, so the average of the actual price will be $97,858 more or less than our predicted price.

**Next Steps**

Further investigation into sought after ZIP codes is warranted. Researching commuting time to downtown Seattle, and schools could be a good indicator, with better connected properties and homes near high-achieving schools potentially being valued higher.

More advanced models exist which may prove to be more accurate in predicting home values. Ensemble methods like gradient boosted decision trees would likely improve our prediction accuracy.

## For More Information

Please review my full analysis in my [Jupyter Notebook](./technical_notebook.ipynb) or my [presentation](./DS_Project_Presentation.pdf).

For any additional questions, please contact **Alex Casey @ alexcasey92@gmail.com**

## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── Technical Notebook.ipynb            <- Narrative documentation of analysis in Jupyter notebook
├── DS_Project_Presentation.pdf         <- PDF version of project presentation
├── data                                <- Both sourced externally and generated from code
└── images                              <- Both sourced externally and generated from code
```

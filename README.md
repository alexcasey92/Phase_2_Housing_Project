![seattle_banner](./images/seattle_banner.jpg)

# Analyzing House Sales and Price Indicators in King County, WA

## Business Understanding

For this project, I used regression modeling to analyze house sales in King County, which is located in the U.S. state of Washington. The population was 2,269,675 in the 2020 census, making it the most populous county in Washington, and the 12th-most populous in the United States. The county seat is Seattle, also the state's most populous city.

Not all home improvements are created equally, so how do you choose between remodeling your kitchen or adding wood floors? How much would adding a bedroom or bathroom actually increase your home value?

This project seeks to advise homeowners about how home renovations might increase the estimated value of their homes.

## Data Understanding

This project uses the King County House Sales dataset, which can be found in kc_house_data.csv in the data folder in this repo.

### Variable description
Here are some brief explanations of the variables used in this project :


* **id** - unique identifier for a house
* **date** - house was sold
* **price** -  is prediction target
* **bedrooms** -  # of Bedrooms
* **bathrooms** -  # of bathrooms
* **sqft_living** -  footage of the home
* **sqft_lot** -  footage of the lot
* **floors** -  floors (levels) in house
* **waterfront** - house with waterfront view
* **view** - has been viewed (prior to being sold)
* **condition** - condition of house
* **grade** - overall grade given to the housing unit, based on King County grading system
* **sqft_above** - square footage of house apart from basement
* **sqft_basement** - square footage of the basement
* **yr_built** - year built
* **yr_renovated** - year when house was renovated
* **zipcode** - zipcode
* **lat** - latitude coordinate
* **long** - longitude coordinate
* **sqft_living15** - the square footage of interior housing living space for the nearest 15 neighbors
* **sqft_lot15** - the square footage of the land lots of the nearest 15 neighbors


## Conclusions and Next Steps

**Location, location, location**
* It's become an almost hackneyed phrase, but it still has meaning
* Where a home is located is the most important factor in it's value -- both now and in the future.

Finally, we built a model that is fairly predictive of price with a R-squared of 0.831. The final model included 82 features, most of which are dummy variables for zipcodes. 

**Next Steps**

Further investigation into sought after ZIP codes is warranted. Researching commuting time to downtown Seattle, and schools could be a good indicator, with better connected properties and homes near high-achieving schools potentially being valued higher.

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

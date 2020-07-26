---
layout: post
title:      "Analyzing the Kings County Housing Data Set"
date:       2020-07-26 13:37:32 -0400
permalink:  analyzing_the_kings_county_housing_data_set
---


My goodness! What felt like a never-ending project is finally complete. I must say I learned  A LOT and have come to appreciate all the work that goes into analyzing data. Before enrolling here at Flatiron, I honestly thought data analysts would just click a button and boom, everything done and you have all your answers.

For this project, King County housing sales data was used to build a model for predicting home sale prices. First step was cleaning, the next step was exploring. I first checked for variables that did not have much impact on price and dropped those. Such as the picture below shows with year renovated

The target audience for this are real estate agents or brokers who can use this information to guide clients (buyers or sellers) on what to expect for home prices. 

This dataset in comprised of 21 variables listed below:

* id - unique identifier for a house
* dateDate - house was sold
* pricePrice - is prediction target
* bedroomsNumber - of Bedrooms/House
* bathroomsNumber - of bathrooms/bedrooms
* sqft_livingsquare - footage of the home
* sqft_lotsquare - footage of the lot
* floorsTotal - floors (levels) in house
* waterfront - House which has a view to a waterfront
* view - Quality of view
* condition - How good the condition is ( Overall )
* grade - overall grade given to the housing unit, based on King County grading system
* sqft_above - square footage of house apart from basement
* sqft_basement - square footage of the basement
* yr_built - Built Year
* yr_renovated - Year when house was renovated
* zipcode - zip
* lat - Latitude coordinate
* long - Longitude coordinate
* sqft_living15 - The square footage of interior housing living space for the nearest 15 neighbors
* sqft_lot15 - The square footage of the land lots of the nearest 15 neighbors

After this, I also added data on cities, which I added to reduce the noise in terms of geography. I grouped over 70 zip codes into roughly 15 cities or regions. I wanted complete geographic representation in my model, but I did not want to use more than 20 variables for it, so this seemed like a healthy compromise given the size and variety of King County.
 
# Data Cleaning:
One of my first steps was to make sure that price was normally distributed and performed a log transformation to do so.  The graphs below the before and after of the log transformation.

![]([Imgur](https://i.imgur.com/7vK3HIU.png?1)http://)      ![]([Imgur](https://i.imgur.com/glKDJFy.png)http://)


One of the variables I removed was yr_renovated, as the scatter plot did not show much impact on price. 
                                                          
Exploratory Data Analysis
I checked for multicollinearity and then explored the data before trying the model. I thought it best to make two dataframes, one for the categorical variables and one for the numeric variables. This help gave me a better picture on the impact of price and used box plots for visualizations. 

                    ![]([Imgur](https://i.imgur.com/Hjfvwrh.png)http://)

Here we can see that condition is a bit unclear on how it affects price. It appears that once condition goes to 3, price goes up a bit but then does not have much variation after.  I decided to drop this variable. 

Numerical variables were plotted with scatter plots. 
    
		![]([Imgur](https://i.imgur.com/pEfafgx.png)http://)
						                                   
                     
Modeling

From this we went on to our model using the two dataframes and additional made with dummy variables. The initial model was an OLS regression. The final model also has a high R Squared indicating that in theory the model explains over 85% of the variability of properties prices.
				![]([Imgur](https://i.imgur.com/3h62Hrz.png)

Conclusion

The three factors that affect price the most are location as expected, but also the grade and size which both show high positive correlation with price. The year a house is built or renovated does not seem to impact price significantly for properties in the King County area

 


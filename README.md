# Module 2 Project README- William Newton Online DS FT 030220

In this repo you will find the below deliverables and analysis for the Module 2 Project - Real Estate Multiple Linear Regression for the Full Time Online Data Science Curriculum

Data was pulled from the below sources:

- King County Real Estate Data Set
    - Included in notebook forked from Learn.co
    
This data was cleaned and combined into one master dataframe from which I derived all visualizations and findings

# Findings & Conclusion

Through analysis and building a multiple linear regression model, I was able to identify the most important predictors for home prices in the Seattle area and present recommendations to potential home sellers. 

Location is the largest predictor of home prices in model. R-squared value increased from .527 to .805 when I included one-hot encoded zipcode columns into my OLS Regression Model. I have included the dataframe in which I kept my model results below so you can see the differences it made between all iterations of the model. 

<img src='/figures/model_results.png' />

The final independent variables I used in my variable were ['bedrooms','bathrooms','sqft_living','condition','grade','has_basement','reno_new']. I also removed outliers in the bedrooms and bathroom column as well as the price column, to increase the normality of my model's QQ Plot. Despite this the distribution of the price column is positively skewed enough so that I was not able to completely satisfy the normality and homoscedacity assumption. Binning categorical features would most likely solve this issue but I was unable to explore this possibility successfully with the pd.cut() method

## Price Column Distribution

<img src='/figures/price_distro.png' />

## Homoscedacity Check for Final Model

<img src='/figures/homosched_check.png' />

## Normality Check for Final Model

<img src='/figures/norm_check.png' />

## Multicollinearity Check for Final Model

<img src='/figures/multi_check.png' />

Despite these limitations of the final model, I feel like I was able to correctly identify the correct variables to use in the model and build visualizations that are inforrmative and readable to include in my non-technical presentation. Using the gmaps library was an easy way to show geographic visualizations but it is a little limiting in it's functionality. Additional, I would have loved to to map zipcodes on the gmaps figure but I ran out of time. Had to make due with a sns.barplot to visualize the difference in zipcodes

<img src='/figures/top_ten.png' />

<img src='/figures/bottom_ten.png' />
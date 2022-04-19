# Phase 2 Project Description


## Project Overview and Business Problem 

Client: National Association for Real Estate Brokers (NAREB) A black led organization that focuses on bringing together the minority professionals in the real estate industry to promote the meaningful exchange of ideas about our business and how best to serve their clientele. For this case the clientele will focus on black intergenerational families.

How can home renovations increase the estimated value of homes for black families in King County, WA? (specifically focusing on intergenerational homes)


### Data Preparation and Understanding 

We begin by importing pandas, numpy, ols, plt, sns, durbin_watson, and statsmodels to analyze our data and perform our regressions. We also import our data as df.

In this analysis, we will perform multi-linear regression. We start by observing our columns to better understand what independent variables to analyze with price for our client.

The first model iteration for our case will focus on square foot living, square foot above, and bathrooms. Before we can get to the analysis, we will drop 'zipcode' as a variable, because the numbers in zipcode are not useful to us in this analysis without context of what each zipcode means.

We will convert our categorical data into something more useful for us in this analysis, and create dummy variablles that are considered categorical.


### Model 1 

When we look at our model, we can see that the model has generated have a lot of information that is useful to us. Our R-squared will assess our goodness of fit, and in this model, we can see that there is a good fit - 0.493 is a moderatly good fit, with 1 being a perfect fit. 

Our p value shows that square foot living and square foot above show no random chance in our analysis, however bathrooms shows some random chance - bathrooms may not be a good variable for this analysis moving forward.


We can also see that there is a positive correlation between square foot living and price. As square foot living increases so does price. We can also see that as square foot above increases price decreases, as does bathroom size.

We will use the Durbin-Watson score to check for homoskedasticity. This is a test for error homoskedasticity. We're looking for values between ~1.5 and ~2.5. This model shows that there is homoskedasticity in our model.¶

The normality assumption states that the model residuals should follow a normal distribution. This model does not follow a normal distribution. We will not continue our test for multicolliniarity, because this distribution is not normal. Therefore, we will move onto our second iteration.¶

### Model 2 

n this second iteration, we will keep square foot living from our first iteration, and analyze bedrooms and floors. These could be useful to our clients trying to purchase new homes. In this model our R-squared is 0.507, which has a better line of fit than the last model we saw. We can see as price increases, number of bedrooms increases, while square foot living and number of floors increases. In this iteration, floors has some random chance (more than bathrooms in the previous model). There is an acceptable level of homoscadascity in this second iteration. As we can see, there all correlations are below 0.7, which is acceptable.

### Model 3 

In this third model iteration, we can see we have the best line of fit (0.509), and can also see that there is zero random chance with all three variables in our model. There is a low correlation between these variables.  


### Conclusion and Next Steps

In the future, we as analysts should sharpen our focus on our normality testing, by dropping the outliers in this data. I recommend continuing to explore square foot living space, square foot lot space, and bedrooms space as variables. They have the lowest random chance, they also offer the most opportunity for renovation in the future. I would also recommend, webscraping for public health data about what black families need as they grow intergenerational families.





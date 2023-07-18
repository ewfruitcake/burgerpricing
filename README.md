# Price elasticity of a burger menu

This is a README describing a big data analytics research project on price optimization. It will contain a summary of the analysis and work completed. 

## Tentative overall methodology

![image](https://github.com/ewfruitcake/burgerpricing/assets/71989699/6ce6fa39-a800-4356-a478-3a9670de3da2)

## Dataset

> The dataset being used for the research project consists of a Google burger café’s transactions throughout the year. The dataset is publicly available.

## Introduction, justification and central topics

Price sensitivity is a great topic of interest in product pricing decisions. When price elasticity of certain products can be estimated accurately, optimal prices will maximize profit margins at the right level of demand. Price optimization is critical to businesses in the North American fast-food restaurant industry, an industry where profit margins are tight, and fast-food options are ubiquitous.

The application of data mining could help a restaurant chain evaluate when to prepare promotional offers during the year and for which items. 
Data mining can be used to better optimize pricing for menu items. 
Knowledge discovery will uncover patterns surrounding how certain beverages are performing and why. 
The results should aid in business decisions such as beverage menu changes, including beverage menu expansion or the removal of beverage items.
Hence, the topics of **data mining** and **knowledge discovery** are the central themes of this research project on the burger menu dataset.

## Programming languages and tools
Programming languages and tools include various Python to apply statistical techniques and visualization to answer the guiding research questions to analyze trends, patterns and distributions in the dataset.

## Statistical methods
Statistical methods such as regression, correlation, and feature transformation will be proposed to solve the stated problems and make informed predictions. 

## Descriptive statistics of the dataset

### Distribution
- Temperature appears to be bi-modal, with most sales happening somewhere around 35F, and around 80F
- Price appears to be at least bimodal (2 peaks) or multimodal (3 peaks). We see peaks at around $10.25, $11.50, and $12.75
- Quantity appears to be at least bimodal (2 peaks) or multimodal (3 peaks). Around quantity 25, 38 and 52 appear to be the most frequent occurrences for transaction sales.
- There is a possibility this both Quantity and Price multiple peaks is due to the categories of different groups of items being grouped together.

### Patterns and trends
- The mean price is $12.47 and mean quantity is 39.93.
- All beverages appear to be very closely priced together.
- There appear to be a more densely packed number of transactions between price at $12-$13.25 and quantity of 40.
- Lunar New Year, National Day, and Qing Ming Festival holidays have the most sales by product.
- Sales transactions during school breaks are much less than sales during the school year for most products. 
- Burgers and coke sell more during breaks, than coffee and lemonade.
- Most sales happen during the week instead of the weekend.
- Most items sold are outdoors.
- Most sales transactions are for combos than individual items.

## Applicable attributes and unusual patterns
I converted CALENDAR_DATE to date format, and both ITEM_NAME and HOLIDAY have been converted to categories. The rest of the columns in the dataset remain integer or float data types.


### Outlier detection
- We do see quite a number of outliers for price when price > $15
- We do see quite a number of outliers for quantity when quantity is roughly >88 or so
- We can either remove the outliers now for price and quantity or transform both price and quantity and see whether that helps. We will wait to see the results of transforming.

## Research questions
- “How does the time of year impact price elasticity of burger café menu items?” 
- “How can burger café menu item prices be modeled by time of year?” 
- “What factors influence certain beverages' sales volume and to what extent?”

## Regression
### Dependent & Independent variable selection
The dependent variable (y) will be quantity. The independent variable (x) will be price along with other independent variables for optimizing price by product and time of year.

## Relationships 
Correlation shows you how the two variables are related and the strength of the relationship between the two variables. Understanding this can help in dimensionality reduction.

Most notable pairs from the correlation matrix heat maps are listed below:
- PRICE and                SELL_ID               			-7.637177e-01
- SELL_CATEGORY and        PRICE                 		-7.634237e-01
- SELL_CATEGORY and        QUANTITY              		-7.472371e-01
- SELL_ID and             QUANTITY              		-7.463939e-01
- SELL_ID and             ITEM_ID               			-3.327415e-01
- SELL_CATEGORY and       ITEM_ID               		-3.320470e-01
- IS_WEEKEND and          QUANTITY              		-2.645138e-01
- SELL_CATEGORY and       SELL_ID                		  9.999971e-01
- AVERAGE_TEMPERATURE and   IS_OUTDOOR            	  5.497614e-01
- QUANTITY and            PRICE                  		  4.453556e-01

## Data Transformation: Standardization & Algorithm Considerations
Machine learning algorithms are best optimized when the distribution of numerical input features are shifted/scaled to a standard range (mean = 0, standard deviation = 1).  
We will apply standardization as a pre-processing step prior to modelling. This will place the features on a similar scale. 
This is typically done with regression models; where feature variables have differing weights attached.

## Experimental design
The Cross-validation technique of train-test split will be used to partition the dataset. A 70/30 split will be used.

## Modelling
Three regression models will be applied to the data and evaluated for best fit.
Model 1 - Linear regression model
Model 2 - Regression tree model
Model 3 - KNN regression model

## Comparative analysis of the models
Model 1 - Linear regression model.
This model made the Condition number very large. The OLS regression model results notes stated either strong multicollinearity or other problems. 
As a result, experimenting with different regression models by removing some independent features from the model may or may not improve the model.
This makes it tricky to get the prediction results.

Model 2 - Regression Decision Tree model.
This was the most informative model from the visualization results.
Our training data was comprised of 9 independent variables that were a combination of numeric and categorical.
By splitting the data into a tree shape of subsets, by each independent variable, to arrive at a prediction for quantity,
We are able to utilize each feature as it pertains to the prediction and the visualization summarized very clearly which features were the most useful based on the R^2 (the coefficient of determination) values.

Model 3 - KNN regression model.
The least amount of error was seen with K=2. However, it is generally recommended to have an odd number for K, so K=2 wouldn't be suitable.
KNN predications are less stable as K reaches closer to 1 because there are less groups or points from the predicted value.
This model was not as meaningful as model 1 or 2, because it's hyperparameters appeared problematic to improve based on the K value discussion.

## Conclusion
The best model would be Model 2 - Regression Decision Tree model based on the comparative analysis results to use for modeling time of year predictors for the burger cafe dataset to estimate quantity.

However, using both Models 1 & 2 for different purposes is useful to get a more holistic analysis.
Model 1 made it very clear that we can reject the null hypothesis, but did not give us confidence over the multicolinearity issues or other numeric problems.
Model 2 had the best restults to provide insights on the variable relationships as predictors of quantity.

From the decision tree results, the most important features are PRICE, SELL_ID, and IS_WEEKEND. 
AVERAGE_TEMPERATURE has some importance on predicting quantity, but nowhere as much as the most important features.
IS_OUTDOOR, YEAR and IS_SCHOOLBREAK have very little impact on predicting quantity.
ITEM_ID & SELL_CATEGORY have no notable impact.

We can conclude that it is possible for quantity to be predicted using price and time of year features, however with a level of importance that is either "moderate" or "low" depending on the time of year feature (IS_WEEKEND, AVERAGE_TEMPERATURE, IS_OUTDOOR, IS_SCHOOLBREAK) tested in the decision tree model.
We can say that the same features would influence beverage sales volume to the extent that they are important as predictors.

## References
- Javivaleiras. (n.d.). GitHub - javivaleiras/retail_price_optimization: Price optimization using price elasticity. GitHub. https://github.com/javivaleiras/retail_price_optimization
- Pratx. (2021). Price Elasticity. Kaggle. https://www.kaggle.com/code/pratx557/price-elasticity


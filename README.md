# Price elasticity of a burger menu

This is a README describing a big data analytics research project on price optimization depending on the time of year. It will contain a description of the work, a summary of the analysis, references and related works. 

## Overall methodology

![Graph final](https://github.com/ewfruitcake/burgerpricing/assets/71989699/6387cc40-dab0-4216-9325-72dbb085a8d6)

## Dataset

> The dataset being used for the research project consists of a Google burger café’s transactions throughout the year. The dataset is publicly available.

## Introduction, justification and central topics

Price sensitivity is a great topic of interest in product pricing decisions. When price elasticity of certain products can be estimated accurately, optimal prices will maximize profit margins at the right level of demand. Price optimization is critical to businesses in the North American fast-food restaurant industry, an industry where profit margins are tight, and fast-food options are ubiquitous. 

The application of data mining could help a restaurant chain evaluate when to prepare promotional offers during the year and for which items. 
Time of year is an important driving factor that influences many price optimization decisions.
Knowledge discovery aims to uncover patterns surrounding how certain beverages are performing, why and when. 
The results should aid in business decisions such as beverage menu changes, including beverage menu expansion or the removal of beverage items.
Hence, the topics of **data mining** and **knowledge discovery** are the central themes of this research project on the burger menu dataset.

## Programming languages and tools
Programming languages and tools include various Python libraries to apply statistical techniques, visualization, and machine learning models to answer the guiding research questions. They will also be applied to analyze trends, patterns and distributions of the dataset. The code will be run on a Jupyter notebook file (.IPYNB), this will be attached to the GitHub repository.

## Statistical methods
Statistical methods such as regression, correlation, and feature transformation will be proposed to solve the stated problems and make informed predictions. 

## Descriptive statistics of the dataset

### Distribution
- Assessing the distribution of Temperature; during which burger sales occur, we see a bi-modal distribution, with most sales happening somewhere around 35F, and around 80F
- Price appears to be at least bimodal (2 peaks) or multimodal (3 peaks) in the distribution. We see peaks at around $10.25, $11.50, and $12.75
- Quantity appears to be at least bimodal (2 peaks) or multimodal (3 peaks). Sales quantities of 25, 38 and 52 appear to be the most frequent occurrences for transactions. Perhaps these are bulk burger orders.
- It's possibile that both Quantity and Price's multiple peaks is due to categories of menu items being grouped together.

### Patterns and trends
- The mean price is $12.47 and mean quantity is 39.93.
- All beverages appear to be very closely priced together.
- There appear to be a more densely packed number of transactions between price at $12-$13.25 and quantity of 40.
- Lunar New Year, National Day, and Qing Ming Festival holidays have the most sales by product.
- Sales transactions during school breaks are much less than sales during the school year for most products. 
- Burgers and coke sell more during breaks, than coffee and lemonade.
- Most sales happen during the week instead of the weekend.
- Most items sold are outdoors. Presumably, the burger cafe has an indoor area.
- Most sales transactions are for combos than individual items.

## Applicable attributes and unusual patterns
I converted CALENDAR_DATE to date format so that these would be handled better by python's data science packages. Both ITEM_NAME and HOLIDAY have been converted to categories. The rest of the columns in the dataset remain integer or float data types.

### Outlier detection
- We do see quite a number of outliers for price when price > $15
- We do see quite a number of outliers for quantity when quantity is roughly >88 or so
- We can either remove the outliers now for price and quantity or transform both price and quantity and see whether that helps. We will wait to see the results of transforming and evaluate if necessary.

## Research questions
- “How does the time of year impact price elasticity of burger café menu items?” 
- “How can burger café menu item prices be modeled by time of year?” 
- “How can beverage sales volume be modeled by time of year?” 

## Regression
### Dependent & Independent variable selection
The dependent variable (y) will be quantity. The independent variable (x) will be price along with other independent variables for optimizing price by product and time of year.

## Relationships 
Correlation represents the strength of the relationship between two variables. 1 being strong, 0 being weak. Understanding this can help in dimensionality reduction.

Most notable pairs from the correlation matrix heat maps are listed below:
- PRICE and                SELL_ID               			-7.637177e-01 ~ -0.7637177
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
This is typically done with regression models; where feature variables have differing weights attached.
We will apply standardization as a pre-processing step prior to modelling. This will place the features on a similar scale. 

## Experimental design
The Cross-validation technique of train-test split will be used to partition the dataset. A 70/30 split will be deemed appropriate, with the training data serving the majority.

## Modelling
Three regression models will be applied to the data and evaluated for best fit.
- Model 1 - Linear regression model
- Model 2 - Regression tree model
- Model 3 - KNN regression model

## Comparative analysis of the models
Model 1 - Linear regression model.
This model made the "Condition" number very large on the OLS regression model results. The results notes stated either strong multicollinearity or other problems were present. As a result, experimenting with different regression models by removing some independent features from the model may or may not improve the model. Overall, these factors make it difficult to obtain reliable prediction results. You may reference the "Evaluation of OLS Regression Results" after .IPYNB file box [89] for details.

Model 2 - Regression Decision Tree model.
This was the most informative model from the visualization results. The visualization summarized very clearly which features were the most useful based on the R^2 (the coefficient of determination) values.
Our training data was comprised of 9 independent variables that were a combination of numeric and categorical.
By splitting the data into a tree shape where we evaluate predictions of quantity by each independent variable, we are able to utilize each feature as it pertains to the prediction, no matter the type of data in an effective manner.

Model 3 - KNN regression model.
The least amount of error was seen with K=2. KNN predictions are less stable as K approaches 1 because there are less groups or points from the predicted value, which is why it is generally recommended to have an odd number for K, and K=2 wouldn't be suitable or stable enough to have an effective KNN model in this case. Overall, this model was not as meaningful as model 1 or 2, because it's hyperparameters appeared problematic to improve based on the K value issue.

## Conclusion

## Concluding on models
The best model would be Model 2 - Regression Decision Tree model. This is based on the comparative analysis results for modeling time of year predictors to estimate quantity.

However, using both Models 1 & 2 for different purposes can be beneficial for a more holistic analysis.
To explain, Model 1 made it very clear that we can reject the null hypothesis, but did not give us confidence over the multicolinearity issues or other numeric problems. Whereas, Model 2 had the best restults to provide insights on the variable relationships as predictors of quantity.

From the decision tree results, the most important features are PRICE, SELL_ID, and IS_WEEKEND. 
AVERAGE_TEMPERATURE has some importance on predicting quantity, but no where as much as the most important features.
IS_OUTDOOR, YEAR and IS_SCHOOLBREAK have very little importance on predicting quantity.
ITEM_ID & SELL_CATEGORY have no notable importance.

## Concluding on research questions
We can conclude that it is possible for quantity to be predicted using price and time of year features, however the level of importance or strength of prediction is either "moderate" or "low" depending on the time of year feature (IS_WEEKEND, AVERAGE_TEMPERATURE, IS_OUTDOOR, IS_SCHOOLBREAK). You may reference the .IPYNB file box [101] "Decision Tree Model Regression - Important Features for the R^2 visualization" for details.

We could say that the same time of year features would influence beverage sales volume to the extent that they are important as predictors, but that would be a pre-mature conclusion without discussion of how this could be modeled and measured.

To predict beverage sales volumes by time of time of year (since there are only 3 beverages), one approach would be to make a slight modification to the dataset by setting up 3 new columns labelled, "IS_COFFEE", "IS_COKE" and "IS_LEMONADE". The values for the columns would be populated based on the "ITEM_NAME" column values (an existing column that describes the name of items sold in text). To set this up, for "IS_COFFEE", we would check if "ITEM_NAME" has coffee, if true, then the value would be 1, else it would be 0. Repeating the same steps for "IS_COKE" and "IS_LEMONADE".
We can then feed the new columns in our model to make predictions for specific beverages. Hyperparameters of the model should be re-assessed for model efficiency.

## Comparison of research against related-works
Other researchers have developed pricing models using the same dataset. 

One researcher states the problem as, “The objective is to set, for a specific day, the optimal price of a product, maximizing profits.” (Javivaleiras, n.d.). Another states, “As a data scientist, it is our task to figure out the optimal prices to set for these items.” (Pratx, 2021). 
While I had choosen a similar study on price elasticity for the burger café dataset as these researchers, my research focused on how the time of year related features are related to optimization. 
My problem, “How does the time of year impact price elasticity of burger café menu items?” analyzes how price optimization varies by product on factors such as temperature, school breaks, weekends and outdoor sales. My follow-up questions, “How can burger café menu item prices be modeled by time of year?" explores different types of regression models, and, “How can beverages' sales volume be modeled by time of year?” proposes how the data can be structured to have a model predict volume by beverage type that comprises relevant time of year features. 

By investigating price elasticity by time of year using a variety of regression based alogrithms, I was able to generate models to predict quantity. I was also able to evaluate model effectiveness and stability. Futhermore, steps to model beverage sales volume by time of year gather critical insight for business decisions surrounding seasonal pricing and marketing. The different focus areas on price elasticity give a unique data mining and knowledge discovery view of the burgermenu dataset.

## Analysis limitations, critical insights on improving the work

## Ethical considerations
While the burger menu dataset does not contain information on specific demographic populations, it does contain data on various holidays in China where burger menu items are sold. If certain holidays cater more to specific demographic groups than others, prices could be set unfairly during holidays to exploit the maximum they are willing to pay (Bergen, 2021). However, it is possible to structure promotional offers during holidays that cater to specific demographics without exploitation and this should be considered. For example, if a certain holiday is popular among parents and children, and a specific burger combo (SELL_ID) is popular among kids, shifting the price too high for the combo on those days could put parents at a disadvantage. Furthermore, the pricing strategy could be viewed as exploitive. 
 
## References of python libraries used
- math: https://docs.python.org/3/library/math.html
- matplotlib: https://matplotlib.org/
- numpy: https://numpy.org/
- pandas: https://pandas.pydata.org/
- seaborn: https://seaborn.pydata.org/index.html#
- scikit-learn: https://scikit-learn.org/stable/index.html
- scipy: https://docs.scipy.org/doc/scipy/tutorial/index.html#user-guide
- statsmodels: https://www.statsmodels.org/stable/index.html

## References for data prep and regression modelling
- How to Interpret Decision Tree Regressor Model Results in Python, Scikit-Learn, Matplotlib. https://www.youtube.com/watch?
  v=z9GDlJs1qDA&ab_channel=EvidenceN
- How to Use the Sklearn Predict Method. https://www.sharpsightlabs.com/blog/sklearn-predict/
- KNN. https://realpython.com/knn-python/
- Machine Learning in Python: Building a Linear Regression Model. https://www.youtube.com/watch?v=R15LjD8aCzc&ab_channel=DataProfessor
- Python Statistics Fundamentals: How to Describe Your Data. https://realpython.com/python-statistics/
- Regression Tree in Python. https://data36.com/regression-tree-python-scikit-learn/
- When and Why to Standardize Your Data. https://builtin.com/data-science/when-and-why-standardize-your-data

## References of related works on the dataset
- Javivaleiras. (n.d.). GitHub - javivaleiras/retail_price_optimization: Price optimization using price elasticity. GitHub. https://github.com/javivaleiras/retail_price_optimization
- Pratx. (2021). Price Elasticity. Kaggle. https://www.kaggle.com/code/pratx557/price-elasticity

## Other references
- Bergen, M. E. (2021, March 26). How AI Can Help Companies Set Prices More Ethically. Harvard Business Review. https://hbr.org/2021/03/how-ai-can-help-companies-set-prices-more-ethically


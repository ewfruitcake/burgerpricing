# Price Elasticity of a Burger Menu
This is a README describing a big data analytics research project on price optimization depending on the time of year. It will contain a description of the work, a summary of the analysis, references and related works. 

## Overall Methodology
You may access the GitHub repository at https://github.com/ewfruitcake/burgerpricing where all the project files will be stored, including the dataset .csv files, license, README and Jupyter Notebook (IPYNB) file for the code and results. The models to be used for price optimization depending on time of year will be regression-based. 

![Graph final](https://github.com/ewfruitcake/burgerpricing/assets/71989699/6387cc40-dab0-4216-9325-72dbb085a8d6)

## Abstract
When prices increase or decrease, demand is either influenced by this change or not impacted. Herein we refer to the concept of price elasticity, referring to the extent that demand is sensitive to movements in price. The greater the price sensitivity, the more demand will shift and vice versa. This is a great topic of interest in business product pricing decisions. When price elasticity of certain products can be estimated accurately, optimal product prices will maximize profit margins at the right level of demand. Price optimization is critical to businesses in the North American fast-food restaurant industry, an industry where profit margins are tight, and fast-food options are ubiquitous. For products not sensitive to demand movements, there may be other factors influencing sales that businesses can drive insights from. A thorough analysis on the topic will involve the big data analytics themes of data mining and knowledge discovery by channeling a business dataset to guide critical business decisions and predictions. The summary of research questions that will guide this study surrounding price optimization will be:

- “How does the time of year impact price elasticity of burger café menu items?” 
- “How can burger café menu item prices be modeled by time of year?” 
- “How can beverage sales volume be modeled by time of year?” 

Insight gained from the research questions could help a restaurant chain evaluate when to prepare promotional offers during the year and for which items. Additionally, how to better optimize pricing for their menu items. Knowledge discovery sheds light on how certain beverages are performing and why to uncover patterns that may aid in business decisions. Those decisions could include; beverage menu expansion or possibly the removal of beverage items.

The dataset that will be used for the research is publicly available and consists of a Google burger café’s transaction throughout the year. The dataset contains a variety of data attributes, ranging from date, numeric and character types.

Keywords: Price optimization, price elasticity, product pricing, data mining, knowledge discovery, regression, business decisions, burger menu dataset

## Statistical Methods
Statistical methods such as regression, correlation, and feature transformation will be proposed to solve the stated problems and make informed predictions.

## Programming Languages and Tools
Programming languages and tools include various Python libraries to apply statistical techniques, visualization, and machine learning models to answer the guiding research questions. They will also be applied to analyze trends, patterns and distributions of the dataset. The code will be run on a Jupyter notebook file (.IPYNB), this will be attached to the GitHub repository.

## Literature Review
What is knowledge discovery? It is finding knowledge in datasets using “previously unknown patterns”; a clear distinction from data mining which involves discovering patterns from large datasets that are “previously known” (Davedzec, 2021; Anoriega, 2021). Data mining is a critical aspect of the knowledge discovery process (Davedzec, 2021). This research project will help me understand how to solve price optimization problems using big data techniques such as regression analysis, feature transformation and model selection, but also understand how knowledge discovery and data mining can solve seemingly complex problems related to price optimization, and what the challenges are. It will be interesting to see how knowledge discovery will highlight previously unknown patterns within the burger menu dataset and how the predictive models developed can be improved. 

An article discussing data mining for price optimization mentions that increasing an entire menu by a fixed percentage, (say 2% or 4%) “won’t achieve long term returns restaurant investors are looking for. Instead, operators need to create a menu architecture that grows overall revenues without cannibalizing high margin items (Hunt, 2021)”. Price optimization analysis has great value to businesses in the restaurant industry with regards to revenue growth, however, the benefits don’t stop there, and can be found in numerous other competitive industries.

Another article discusses the concept of dynamic price optimization (Dorota-Owczarek, 2022). This is a tactic that Amazon uses to adjust their prices to keep up or outperform the competition in the online marketplace (Dorota-Owczarek, 2022). Dynamic price optimization finds the highest price that a customer is willing to pay while maximizing the likelihood of them buying the product considering changes to the pricing and customer environment (Dorota-Owczarek, 2022). This price optimization approach uses environment estimates that drive the price optimization algorithm, and the models can adjust in real-time (Dorota-Owczarek, 2022).

An interesting use of price optimization comes from an article that claims Artificial Intelligence (AI) could be used for setting ethical prices (Bergen, 2021). The article states that current price optimization techniques that companies use do not have an ethical component that address age, disability, or marginalized populations and can exploit the maximum those populations are willing to pay (Bergen, 2021). Another article by Biggs, Sun, & Ettl. (2021) mentions that while many companies are interested in employing personalized pricing for products, it can result in legal and fairness implications. While the burger menu dataset does not contain information on demographic populations, it is important to note the existence of ethical and legal implications for businesses with access to such data intending to employ personalized price optimization models. 

One study discusses how knowledge discovery of predictive formulas can help construct a mathematical optimization problem based on a whole set of predictive formulas (Ito & Fujimaki, 2017). Experiments performed on retail datasets were shown to significantly improve gross profit (Ito & Fujimaki, 2017). Such uses of knowledge discovery for optimizing price models could greatly enable better predictions.

An online clothing retailer; Rue La La, faced difficulties in predicting popularity of a specific clothing style in advance of it being sold (Harvard Business School et al., n.d.). This presented futher challenges in predicting revenue and demand (Harvard Business School et al., n.d.). Harvard Business School researchers suggested that a single price model aimed to maximize revenue is best for those type of predictions. The researchers further state that “relatively little research has been devoted to multi-product single-price optimization models in the retail industry”; something to note on the topic of data mining for price optimization given the industry (Harvard Business School et al., n.d.).

It is evident that the topics of knowledge discovery and data mining for price optimization have various implications in different industries on profit, predictions, and even ethical considerations. 

Other researchers have developed price elasticity models using the burgermenu dataset. One researcher using the burger menu dataset states the problem as, “The objective is to set, for a specific day, the optimal price of a product, maximizing profits.” (Javivaleiras, n.d.). Another states it as, “As a data scientist, it is our task to figure out the optimal prices to set for these items.” (Pratx, 2021). While I am choosing to perform a similar study on price elasticity for the burger café dataset as these researchers, the key difference is that I am applying a different timeframe to that question and have a different set of follow-up questions the authors do not tackle. My problem, “How does the time of year impact price elasticity of burger café menu items?” will analyze how price optimization varies by product on factors such as holidays, school breaks, weekends and outdoor sales. My follow-up questions are, “How can burger café menu item prices be modeled by time of year?” will provide insight on different models by product, and finally, “How can beverage sales volume be modeled by time of year?” will shed light on factors that influence beverage predictions by time of year.

The number of publicly available research articles on price elasticity using this dataset are few and far in between. By investigating price elasticity and variability in time of year, I may uncover a model to predict optimal prices more specific to current business pricing strategies. Lastly, looking what factors influence certain beverages' sales volume and to what extent can also gather unique insight for critical business decisions surrounding seasonal pricing and marketing and what further drives the model. Due to the different focus questions, my research provides a different insight into how price elasticity can be measured. The different focus areas provide depth on what has happened before from a data mining and knowledge discovery view. Nonetheless, my outcomes will be compared with prior research on the same dataset.

Upon researching price optimization using data mining and knowledge discovery topics, I found price optimization and price elasticity projects on different datasets. There was one where the author specified their intent to optimize pricing, but their efforts took data on pricing and fitted it to demand using linear regression (Li, 2018). Another researcher tackles how to calculate price elasticity using Python but not price optimization (Kharwal, 2021). With price optimization, the first step is determining price elasticity, but more work needs to be done to come to a price optimization conclusion. Throughout researching what exists on the topic of price optimization, a common analytics technique is the use of regression (Li, 2018; Hunt, 2021; Javivaleiras, n.d.; Pratx, 2023; Demand of Burger King - Managerial Economic, n.d.; Graddy, 2006; MattBirch, n.d.). Sklearn is a popular python library that is used for creating test and training sets and formulating prediction models (Javivaleiras, n.d.; Pratx, 2023). Several authors explicitly state the method of Ordinary Least Squares (OLS) Estimation to fit price data to demand (Li, 2018; Graddy, 2006). Some take it a step further to indicate that OLS findings should not be relied on and Instrumental Variables (IV) should be taken into account to determine the optimal price (Graddy, 2006; MattBirch, n.d.). It appears that Graddy (2006) prepared research on this topic and MattBirch (n.d.) followed to replicate the study using data tools.

## Descriptive Statistics of the Dataset

### Distribution
- Assessing the distribution of Temperature; during which burger sales occur, we see a bi-modal distribution, with most sales happening somewhere around 35F, and around 80F
- Price appears to be at least bimodal (2 peaks) or multimodal (3 peaks) in the distribution. We see peaks at around $10.25, $11.50, and $12.75
- Quantity appears to be at least bimodal (2 peaks) or multimodal (3 peaks). Sales quantities of 25, 38 and 52 appear to be the most frequent occurrences for transactions. Perhaps these are bulk burger orders.
- It's possibile that both Quantity and Price's multiple peaks is due to categories of menu items being grouped together.

### Patterns and Trends
- The mean price is $12.47 and mean quantity is 39.93.
- All beverages appear to be very closely priced together.
- There appear to be a more densely packed number of transactions between price at $12-$13.25 and quantity of 40.
- Lunar New Year, National Day, and Qing Ming Festival holidays have the most sales by product.
- Sales transactions during school breaks are much less than sales during the school year for most products. 
- Burgers and coke sell more during breaks, than coffee and lemonade.
- Most sales happen during the week instead of the weekend.
- Most items sold are outdoors. Presumably, the burger cafe has an indoor area.
- Most sales transactions are for combos than individual items.

## Applicable Attributes and Uusual Patterns
I converted CALENDAR_DATE to date format so that these would be handled better by python's data science packages. Both ITEM_NAME and HOLIDAY have been converted to categories. The rest of the columns in the dataset remain integer or float data types.

### Outlier Detection
- We do see quite a number of outliers for price when price > $15
- We do see quite a number of outliers for quantity when quantity is roughly >88 or so
- We can either remove the outliers now for price and quantity or transform both price and quantity and see whether that helps. We will wait to see the results of transforming and evaluate if necessary.

### Dependent & Independent Variable Selection
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

## Experimental Design
The Cross-validation technique of train-test split will be used to partition the dataset. A 70/30 split will be deemed appropriate, with the training data serving the majority.

## Modelling
Three regression models will be applied to the data and evaluated for best fit.
- Model 1 - Linear regression model
- Model 2 - Regression tree model
- Model 3 - KNN regression model

## Comparative Analysis of the Proposed Models
Model 1 - Linear regression model.
This model made the "Condition" number very large on the OLS regression model results. The results notes stated either strong multicollinearity or other problems were present. As a result, experimenting with different regression models by removing some independent features from the model may or may not improve the model. Overall, these factors make it difficult to obtain reliable prediction results. You may reference the "Evaluation of OLS Regression Results" after .IPYNB file box [89] for details.

Model 2 - Regression Decision Tree model.
This was the most informative model from the visualization results. The visualization summarized very clearly which features were the most useful based on the R^2 (the coefficient of determination) values.
Our training data was comprised of 9 independent variables that were a combination of numeric and categorical.
By splitting the data into a tree shape where we evaluate predictions of quantity by each independent variable, we are able to utilize each feature as it pertains to the prediction, no matter the type of data in an effective manner.

Model 3 - KNN regression model.
The least amount of error was seen with K=2. KNN predictions are less stable as K approaches 1 because there are less groups or points from the predicted value, which is why it is generally recommended to have an odd number for K, and K=2 wouldn't be suitable or stable enough to have an effective KNN model in this case. Overall, this model was not as meaningful as model 1 or 2, because it's hyperparameters appeared problematic to improve based on the K value issue.

## Concluding on Models
The best model would be Model 2 - Regression Decision Tree model. This is based on the comparative analysis results for modeling time of year predictors to estimate quantity.

However, using both Models 1 & 2 for different purposes can be beneficial for a more holistic analysis.
To explain, Model 1 made it very clear that we can reject the null hypothesis, but did not give us confidence over the multicolinearity issues or other numeric problems. Whereas, Model 2 had the best restults to provide insights on the variable relationships as predictors of quantity.

From the decision tree results, the most important features are PRICE, SELL_ID, and IS_WEEKEND. 
AVERAGE_TEMPERATURE has some importance on predicting quantity, but no where as much as the most important features.
IS_OUTDOOR, YEAR and IS_SCHOOLBREAK have very little importance on predicting quantity.
ITEM_ID & SELL_CATEGORY have no notable importance.

## Concluding on Research Questions
We can conclude that it is possible for quantity to be predicted using price and time of year features, however the level of importance or strength of prediction is either "moderate" or "low" depending on the time of year feature (IS_WEEKEND, AVERAGE_TEMPERATURE, IS_OUTDOOR, IS_SCHOOLBREAK). You may reference the .IPYNB file box [101] "Decision Tree Model Regression - Important Features for the R^2 visualization" for details.

We could say that the same time of year features would influence beverage sales volume to the extent that they are important as predictors, but that would be a pre-mature conclusion without discussion of how this could be modeled and measured.

To predict beverage sales volumes by time of time of year (since there are only 3 beverages), one approach would be to make a slight modification to the dataset by setting up 3 new columns labelled, "IS_COFFEE", "IS_COKE" and "IS_LEMONADE". The values for the columns would be populated based on the "ITEM_NAME" column values (an existing column that describes the name of items sold in text). To set this up, for "IS_COFFEE", we would check if "ITEM_NAME" has coffee, if true, then the value would be 1, else it would be 0. Repeating the same steps for "IS_COKE" and "IS_LEMONADE".
We can then feed the new columns in our model to make predictions for specific beverages. Hyperparameters of the model should be re-assessed for model efficiency.

## Comparison of Research against Related-Works
Other researchers have developed pricing models using the same dataset. 

One researcher states the problem as, “The objective is to set, for a specific day, the optimal price of a product, maximizing profits.” (Javivaleiras, n.d.). Another states, “As a data scientist, it is our task to figure out the optimal prices to set for these items.” (Pratx, 2021). 
While I had choosen a similar study on price elasticity for the burger café dataset as these researchers, my research focused on how the time of year related features are related to optimization. 
My problem, “How does the time of year impact price elasticity of burger café menu items?” analyzes how price optimization varies by product on factors such as temperature, school breaks, weekends and outdoor sales. My follow-up questions, “How can burger café menu item prices be modeled by time of year?" explores different types of regression models, and, “How can beverages' sales volume be modeled by time of year?” proposes how the data can be structured to have a model predict volume by beverage type that comprises relevant time of year features. 

By investigating price elasticity by time of year using a variety of regression based alogrithms, I was able to generate models to predict quantity. I was also able to evaluate model effectiveness and stability. Futhermore, steps to model beverage sales volume by time of year gather critical insight for business decisions surrounding seasonal pricing and marketing. The different focus areas on price elasticity give a unique data mining and knowledge discovery view of the burgermenu dataset.

## Analysis Limitations, Critical Insights on Improving the Work
Outliers handling
Normalizing data does not remove the presence of outliers in the dataset. Outliers were detected in each of the price and quantity box plots. It may be worth removing the outliers from the original dataset, and testing the models again to see if the removal of those outliers impacts model performance, and to what extent.

Missing Values
There was a large number of missing values in the HOLIDAY column. It may be worthwhile to assign a unique category to the missing values, such as NO HOLIDAY. This would impact the visualizations on items sold by HOLIDAY.

## Ethical Considerations
While the burger menu dataset does not contain information on specific demographic populations, it does contain data on various holidays in China where burger menu items are sold. If certain holidays cater more to specific demographic groups than others, prices should not be set unfairly during holidays to exploit the maximum they are willing to pay (Bergen, 2021). For example, if a certain holiday is popular among parents and children, and a specific burger combo (SELL_ID) is popular among kids, shifting the price too high for the combo on those days could put parents at a disadvantage. Such pricing strategies could be viewed as exploitive. 

## References

## Citing Python Libraries Used
- math: https://docs.python.org/3/library/math.html
- matplotlib: https://matplotlib.org/
- numpy: https://numpy.org/
- pandas: https://pandas.pydata.org/
- seaborn: https://seaborn.pydata.org/index.html#
- scikit-learn: https://scikit-learn.org/stable/index.html
- scipy: https://docs.scipy.org/doc/scipy/tutorial/index.html#user-guide
- statsmodels: https://www.statsmodels.org/stable/index.html

## Descriptive Statistics, Data Preperation, and Regression Modelling References
- Bonthu, H. (2023). Detecting and Treating Outliers | Treating the odd one out! Analytics Vidhya. https://www.analyticsvidhya.com/blog/2021/05/detecting-and-treating-outliers-treating-the-odd-one-out/
- Data Professor. (2020, April 2). Machine Learning in Python: Building a linear regression model [Video]. YouTube. https://www.youtube.com/watch?v=R15LjD8aCzc
- Ebner, J. (2022, May 2). How to use the Sklearn Predict Method - Sharp Sight. Sharp Sight. https://www.sharpsightlabs.com/blog/sklearn-predict/
- EvidenceN. (2020, December 17). How to interpret Decision Tree Regressor model results in Python, Scikit-Learn, Matplotlib [Video]. YouTube. https://www.youtube.com/watch?v=z9GDlJs1qDA
- GeeksforGeeks. (2022). Data Visualization with Python Seaborn. GeeksforGeeks. https://www.geeksforgeeks.org/data-visualization-with-python-seaborn/
- Jaadi, Z. (2019). When and why to standardize your data. Built In. https://builtin.com/data-science/when-and-why-standardize-your-data
- Pandas DataFrame iloc Property. (n.d.). https://www.w3schools.com/python/pandas/ref_df_iloc.asp
- Python, R. (2023). Python Statistics Fundamentals: How to Describe your Data. realpython.com. https://realpython.com/python-statistics/
- Ujhelyi, T. (2022, December 8). Regression tree in Python using Scikit-Learn (Code your Decision Tree #1). Data36. https://data36.com/regression-tree-python-scikit-learn/
- Zach. (2021). How to Make Heatmaps with Seaborn (With Examples). Statology. https://www.statology.org/seaborn-heatmap/
- Zach. (2022). How to perform OLS regression in Python (With example). Statology. https://www.statology.org/ols-regression-python/

## Abstract, Literature Review and Related Works References
- Anoriega. (2021, June 14). What Is Data Mining: Definition, Examples, Tools, and Techniques (For Beginners) | Georgia Tech Boot Camps. Georgia Tech Boot Camps. https://bootcamp.pe.gatech.edu/blog/what-is-data-mining/
- Bergen, M. E. (2021, March 26). How AI Can Help Companies Set Prices More Ethically. Harvard Business Review. https://hbr.org/2021/03/how-ai-can-help-companies-set-prices-more-ethically
- Biggs, Sun, & Ettl. (2021). Model Distillation for Revenue Optimization: Interpretable Personalized Pricing. https://arxiv.org/pdf/2007.01903.pdf
- Biggs, Sun, & Ettl. (2021). Model Distillation for Revenue Optimization: Interpretable Personalized Pricing. https://arxiv.org/pdf/2007.01903.pdf
- Demand of Burger King - Managerial Economic. (n.d.). Scribd. https://www.scribd.com/document/98069652/Demand-of-Burger-King-Managerial-Economic#
- Devedzic, V. (2001). KNOWLEDGE DISCOVERY AND DATA MINING IN DATABASES. In World Scientific Publishing Company eBooks (pp. 615–637). https://doi.org/10.1142/9789812389718_0025
- Dorota-Owczarek. (2022, December 1). Why Do You Need Dynamic Pricing Optimization? Machine Learning in Novel Pricing Strategies. nexocode. https://nexocode.com/blog/posts/pricing-optimization-machine-learning/
- Graddy, K. (2006). Markets: The Fulton Fish Market. Journal of Economic Perspectives, 20(2), 207–220. https://doi.org/10.1257/jep.20.2.207
- Harvard Business School, Ferreira, K. J., Alex Lee, B. H., & Simchi-Levi, D. (n.d.). Analytics for an Online Retailer: Demand Forecasting and Price Optimization. https://www.hbs.edu/ris/Publication%20Files/kris%20Analytics%20for%20an%20Online%20Retailer_6ef5f3e6-48e7-4923-a2d4-607d3a3d943c.pdf
- Hunt, P. (2021, December 11). What Should That Burger Cost? - Heated. Medium. https://heated.medium.com/what-should-that-burger-cost-cooking-up-a-high-impact-pricing-strategy-for-restaurants-c63c0463e4d8
- Javivaleiras. (n.d.). GitHub - javivaleiras/retail_price_optimization: Price optimization using price elasticity. GitHub. https://github.com/javivaleiras/retail_price_optimization
- Ito, S., & Fujimaki, R. (2017). Optimization Beyond Prediction. https://doi.org/10.1145/3097983.3098188
- Kharwal, A. (2021). Price Elasticity of Demand using Python. Thecleverprogrammer. https://thecleverprogrammer.com/2021/09/14/price-elasticity-of-demand-using-python/
- Li, S. (2018, December 6). Price Elasticity of Demand, Statistical Modeling with Python. Medium. https://towardsdatascience.com/calculating-price-elasticity-of-demand-statistical-modeling-with-python-6adb2fa7824d
- MattBirch. (n.d.). GitHub - MattBirch42/Fulton_Fish_IV_in_Python: This little mini project is intended to show why we might need instrumental variables (IV) to estimate demand elasticities, and to demonstrate how to implement IV in Python. GitHub. https://github.com/MattBirch42/Fulton_Fish_IV_in_Python/tree/main
- Pratx. (2021). Price Elasticity. Kaggle. https://www.kaggle.com/code/pratx557/price-elasticity



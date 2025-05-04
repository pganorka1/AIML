### Project Title
Revenue Management of Superstore Sales Data: 
**Prashant Ganorkar**

#### Executive summary
The DBSCAN classification of sales data shows 3 distinct clusters, however when grouping data by regions shows 10 distinct clusters. Time series model can predict accuractly if weekly orders are more or less than 6 order per week as a target and consistantly the orders have been below the target excepts for fews weeks
#### Rationale
Why should anyone care about this question?
The sales trend, classification, clustering and forecasting is important to determine sales strategy to increase reveneue
#### Research Question
What are you trying to answer?
If the weekly orders forcasting are above or below the target 6 orders per week
#### Data Sources
What data will you use to answer you question?
https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting
#### Methodology
What methods are you using to answer the question?
Classification, Trend analysis and Time Series modeling for forecasting
#### Results
What did your research find?
In short the time series logistic regression is better with predicting weekly data rather than logistic regression with daily order data to answer the question on hand. Also it is challenging to deal with time series data and forecasting is an art and one needs to careful with the predictions from modeling as it is influence by many arbitary factors as well
Detailed results are as follows:
The first section of the data was about “know your data” which involved identifying duplicate rows and columns and removing them. Converting lowercase, strip leading and trailing spaces and removing special characters. Dropped nine rows with missing values. Identified outliers using ZScore, interquartile range and Box plot. They all identified different sets of outliers based on different criteria. Used Zs ZScore core to remove outliers (123 rows)
Used feature engineering to extract and transform the “Sales” column and then scaled the column as the Violin plot shows wide variation in the data set. Visualized sales data based on category, subcategory and region, Top states based on sales where CA, NY, and TX, however when grouped by city top three where NYC, LA and SF. Trend line showed decrease in sales from 2015 to 2016 but he steady increase from 2016 to 2018. Month to month/week to week line plot shows lot of variation in sales.
I conducted DBSCAN modeling and found three distinct clusters. The DBSCAN conducted based on regions showed ten distinct clusters. KMEANS clustering showed three distinct clusters as well. Then conducted Time Series Modeling, where the data needed to be further verified and prepared for modeling such as sort by order date, transform order date to numerical column. Made sure tested for singularity needed for time series modeling and made the data regular by just looking at daily ordered data only and filling the days with no sales with zero sales. Looking at the trend showed noisy data so smoothed the data based on exponential weighting and plotted the trend line. Then split the data into train and test the data then ran Linear Regression to show as MAE as 45% and MSE as 48% which were low. Please note this model taking just the daily order led to an oversimplified model. Then to improve the model, we used weekly data and ran Logistic Regression model with criteria of if orders <6 then output is zero and if greater than 6/week then the output is 1 and improved the accuracy to 95.2%.

#### Next steps
What suggestions do you have for next steps?
1.  Predict future sales based on product type, customer segment, seasonality, customer location and discounts
2.  Customer segmentation based on purchase frequency, total spend , product purchased etc.
3.  Product Recommendation based on shared category purchase
4.  Profitability analysis
5.  Predict delivery time for products

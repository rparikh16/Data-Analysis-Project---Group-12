# Data Preprocessing: 
First, we imported the two excel files and merged them into a single data frame: Using the pandas library to load the two datasets into two separate data frames. 

Before we began building the model, we cleaned and prepared the data. This included handling missing values, dealing with outliers, and converting categorical variables into numerical values. In our case, we had some missing values and since we were unable to source the data for those columns we used the mean function to populate the cells. In the real-world case, this function will be sparingly used!

One of the tables had data in a quarterly format, so we converted it to an annual format to merge the two tables for the analysis. Using the merge function, the two data frames were combined into a single data frame, ensuring that the common columns were used as keys to align the data correctly.

# Exploratory data analysis: 
We used visualization techniques to understand the relationship between the dependent variable (delinquency rate) and the independent variables (median household income, consumer price index, labour force participation rate, unemployment rate, real disposal income, average value of new loans, and residential mortgage arrears rates).

## In the first plot, a line chart of the Mortgage_delinquency_rate over the Years has been shown. It indicates the rate of mortgage delinquency over the years. The mortgage delinquency rate has decreased over the years and reached its lowest in 2021.
  
## In the second plot, Scatter Plot of Average_Value_New_Loans vs Real_Median_Household_Income
the Real_Median_Household_Income over the Years has been shown. It indicates the real median household income over the years. The real median household income has increased over the years. 

## In the third plot, a line chart of the Labour_Force_Participation_Rate over the Years has been shown. It indicates the labour force participation rate over the years. The labour force participation rate has decreased over the years.

## In the fourth plot, a line chart of the Unemployment_Rate over the Years has been shown. It indicates the unemployment rate over the years. The unemployment rate has decreased over the years, with a few fluctuations.

## In the fifth plot, a line chart of the Real_Disposal_Income_Percent_Change over the Years has been shown. It indicates the change in real disposal income over the years. The real disposal income has increased over the years with fluctuations.

## Scatter Plot: A scatter plot is used to show the relationship between two variables. In the scatter plot, we can see how the real median household income and the average value of new loans are related. If the points on the scatter plot are closely aligned along a line, then it indicates that there is a positive linear relationship between the two variables. If the points are spread out, it indicates a weaker or no relationship.

In the scatter plot between the Real Median Household Income and Consumer Price Index percent change, you can observe a positive relationship between the two variables. As the Real Median Household Income increases, the Consumer Price Index percent change also increases. This suggests that as household income goes up, the cost of living, as represented by the Consumer Price Index, also increases.

## In the box plot, you can see the distribution of the values for the Unemployment Rate. The box shows the interquartile range (IQR) and the median, which is represented by the line inside the box. The IQR is the range between the first and the third quartile and covers 50% of the data. The "whiskers" represent the range of the data excluding the outliers, which are plotted as individual dots outside the whiskers. You can see that the median of Unemployment Rate is around 7%, and most of the values are within the range of 6.5% to 7.5%. There are a few outliers with values above 8%.

## A heatmap is a graphical representation of data where individual values are represented as colours. In a heatmap, the values are usually represented on a colour scale, with the colour intensity indicating the magnitude of the value. The colour scale can range from cool colours, such as blue or green, to warm colours, such as red or yellow, and everything in between.



In the context of feature selection, a heatmap is often used to visualize the correlation between different features. The goal is to identify features that are highly correlated with each other, which can indicate that one or more features may be redundant. Visualizing the correlations can help in the process of reducing the number of features in a dataset and improving the performance of machine learning models.

# Feature selection: Selected the most important features to use as predictors for the model. There are several feature selection techniques such as correlation analysis, decision trees, or recursive feature elimination to select the best predictors. We used correlation analysis to identify the highly correlated variables. 

# Model building: Used the selected features to train the model. Tried the linear regression machine learning algorithms to predict delinquency rates.

# Model evaluation: Evaluated the performance of the model using the accuracy rate. To my utter shock and horror, the accuracy was Accuracy:  -84297.5380255628.  A negative score is never ideal so I probed further to find that some of the reasons could be: 

## Overfitting or underfitting: This can occur if the model is too complex or too simple for the data. In this case, try adjusting the model's hyperparameters, such as the number of features, to find the right balance between complexity and simplicity.

## Insufficient data: If the data is too small, the model may not be able to learn the underlying patterns in the data, resulting in poor accuracy.

## Inadequate feature engineering: It's important to choose the right features for the model to ensure that it can learn the relationships between the independent and dependent variables. If the features are not properly selected, this can result in poor accuracy.

In our case, it seems that we have a very small dataset. We will try to find additional data for the same. 

# Model refinement: Since the performance is not satisfactory, we will refine the model by adjusting the parameters, adding more features, or trying a different machine learning algorithm.


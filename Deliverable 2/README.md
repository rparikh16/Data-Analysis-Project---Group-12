# Data Preprocessing: 
First, we imported the two excel files and merged them into a single data frame: Using the pandas library to load the two datasets into two separate data frames. 

<img width="1054" alt="Data_table_mortgages" src="https://user-images.githubusercontent.com/111670866/216486847-d5e340a6-c865-46ba-8cad-b26658979a30.png">


Before we began building the model, we cleaned and prepared the data. This included handling missing values, dealing with outliers, and converting categorical variables into numerical values. In our case, we had some missing values and since we were unable to source the data for those columns we used the mean function to populate the cells. In the real-world case, this function will be sparingly used!

One of the tables had data in a quarterly format, so we converted it to an annual format to merge the two tables for the analysis. Using the merge function, the two data frames were combined into a single data frame, ensuring that the common columns were used as keys to align the data correctly.

<img width="1054" alt="Annual_data" src="https://user-images.githubusercontent.com/111670866/216486892-2fc4ec17-d8c4-420c-999c-e852c7a191d4.png">


# Exploratory data analysis: 
We used visualization techniques to understand the relationship between the dependent variable (delinquency rate) and the independent variables (median household income, consumer price index, labour force participation rate, unemployment rate, real disposal income, average value of new loans, and residential mortgage arrears rates).

## In the line chart of the Mortgage_delinquency_rate over the Years has been shown. It indicates the rate of mortgage delinquency over the years. The mortgage delinquency rate has decreased over the years and reached its lowest in 2021.

  <img width="927" alt="Line_plot_Mortgage Delinquency Rate" src="https://user-images.githubusercontent.com/111670866/216486926-ba08a0ad-cdae-4d13-8f68-ced3ab731d91.png">

## In the  Scatter Plot of Average_Value_New_Loans vs Real_Median_Household_Income 
The Real_Median_Household_Income over the Years has been shown. It indicates the real median household income over the years. The real median household income has increased over the years. 

<img width="789" alt="Scatter_plot_Average_Value_New_Loans vs Real_Median_Household_Income" src="https://user-images.githubusercontent.com/111670866/216486995-f7323f57-871f-4133-bdaf-65ca93b55bd9.png">


## In the scatter plot between the Real Median Household Income and Consumer Price Index percent change, you can observe a positive relationship between the two variables. As the Real Median Household Income increases, the Consumer Price Index percent change also increases. This suggests that as household income goes up, the cost of living, as represented by the Consumer Price Index, also increases.

<img width="789" alt="Scatter Plot of Real_Median_Household_Income vs Consumer_Price_Index_Percent_Change" src="https://user-images.githubusercontent.com/111670866/216487234-982ff232-e51e-4a8c-9991-dafd4cb0081d.png">


## In the box plot, you can see the distribution of the values for the Unemployment Rate. The box shows the interquartile range (IQR) and the median, which is represented by the line inside the box. The IQR is the range between the first and the third quartile and covers 50% of the data. The "whiskers" represent the range of the data excluding the outliers, which are plotted as individual dots outside the whiskers. You can see that the median of Unemployment Rate is around 7%, and most of the values are within the range of 6.5% to 7.5%. There are a few outliers with values above 8%.

<img width="789" alt="Bar Plot of Unemployment_Rate by Years" src="https://user-images.githubusercontent.com/111670866/216487292-eb8f607b-1308-408a-97c4-fb1c974eeb98.png">

## A heatmap is a graphical representation of data where individual values are represented as colours. In a heatmap, the values are usually represented on a colour scale, with the colour intensity indicating the magnitude of the value. The colour scale can range from cool colours, such as blue or green, to warm colours, such as red or yellow, and everything in between.

<img width="789" alt="heatmap(corr_matrix)" src="https://user-images.githubusercontent.com/111670866/216487338-e53e1068-a4f7-417d-8a53-1c028be525c9.png">


In the context of feature selection, a heatmap is often used to visualize the correlation between different features. The goal is to identify features that are highly correlated with each other, which can indicate that one or more features may be redundant. Visualizing the correlations can help in the process of reducing the number of features in a dataset and improving the performance of machine learning models.

# Feature selection: Selected the most important features to use as predictors for the model. There are several feature selection techniques such as correlation analysis, decision trees, or recursive feature elimination to select the best predictors. We used correlation analysis to identify the highly correlated variables. 

# Model building: Used the selected features to train the model. Tried the linear regression machine learning algorithms to predict delinquency rates.

# Model evaluation: Evaluated the performance of the model using the accuracy rate. To my utter shock and horror, the accuracy was Accuracy:  -84297.5380255628.  A negative score is never ideal so I probed further to find that some of the reasons could be: 

## Overfitting or underfitting: This can occur if the model is too complex or too simple for the data. In this case, try adjusting the model's hyperparameters, such as the number of features, to find the right balance between complexity and simplicity.

## Insufficient data: If the data is too small, the model may not be able to learn the underlying patterns in the data, resulting in poor accuracy.

## Inadequate feature engineering: It's important to choose the right features for the model to ensure that it can learn the relationships between the independent and dependent variables. If the features are not properly selected, this can result in poor accuracy.

In our case, it seems that we have a very small dataset. We will try to find additional data for the same. 

# Model refinement: Since the performance is not satisfactory, we will refine the model by adjusting the parameters, adding more features, or trying a different machine learning algorithm.


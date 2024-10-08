# How Much Did it Rain Kaggle Challenge  
My Kaggle Challenge for DATA 3402  
[Link to challenge](https://www.kaggle.com/competitions/how-much-did-it-rain-ii/overview/evaluation)
## The goal of this challenge is to use machine learning to predict hourly rainfall from polarimetric radars ##   
After looking at the data, I noticed that there is an "Expected" column. That specific column is the value I want to attain using machine learning, making this a regression task.   
With this, I understood that my input would be all features excluding the "Expected" value, and my output would be the "Expected".  
# Problems I faced  
- The first problem I faced was that my laptop could not process the full dataset, therefore I had trimmed the data.  
- The second problem I faced was the amount of time it took to train the data, for the SVR model I had let it train overnight.
  # Prep before beggining the task
- Firstly I had to trim the data to 100,000 data points as stated above.
- Secondly, I plotted the distribution of the "Expected" value, which I will attach below.
  ![](expected.png)
  - I also needed to deal with NaN values before training. After examining the dataset, I found that there weren't that many values that were NaN, therefore I filled those values with 0.
# Models I used  
 - Originally, I had used a **Linear Regression model**, however after plotting my results I figured to try a different model as well. This led to me trying a **Support Vector Regression** model.
# Results  
After training using both a LR model and SVR model, I printed my mean squared error and plotted my results. For plotting, I plotted a histogram of the difference between my predicted values and actual expected values.  
What I found was that the SVR gave me a much skinnier distribution, which is great but the mean squared error was higher than for the LR model.  
  
  
![Linear Regression Distribution](LinearRegression.png)  ![Support Vector Regression Distribution](SVR.png)
# What I would do with what I know now
I think that one of the things I would change in how I approached this problem is to group the data points by each hour, rather than the random data points. This would help predict **hourly** rainfall better.
# How to Reproduce Results
To reproduce these results, you would need to split your data by the "Expected" column. Then, you would need to apply a regression model of your choice. After finishing training, you would need to apply a mean squared error function on your predicted values against the actual expected value. You may then visualize this data via histogram or scatter plot to examine the distribution.  

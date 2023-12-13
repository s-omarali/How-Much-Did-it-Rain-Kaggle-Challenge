# How Much Did it Rain Kaggle Challenge  
My Kaggle Challenge for DATA 3402  
## The goal of this challenge is to use machine learning to predict hourly rainfall from polarimetric radars ##   
After looking at the data, I noticed that there is an "Expected" column. That specific column is the value I want to attain using machine learning, making this a regression task.   
With this, I understood that my input would be all features excluding the "Expected" value, and my output would be the "Expected".  
# Problems I faced  
- The first problem I faced was that my laptop could not process the full dataset, therefore I had trimmed the data.  
- The second problem I faced was the amount of time it took to train the data, for the SVR model I had let it train overnight.
  # Prep before beggining the task
- Firstly I had to trim the data to 100,000 data points as stated above.
- Secondly, I plotted the distribution of the "Expected" value, which I will attach below.
  ![](Screenshot 2023-12-13 101241.png)
# Models I used  
 - Originally, I had used a **Linear Regression model**, however after plotting my results I figured to try a different model as well. This led to me trying a **Support Vector Regression** model.
# Results  
After training using both a LR model and SVR model, I printed my mean squared error and plotted my results. For plotting, I plotted a histogram of the difference between my predicted values and actual expected values. 

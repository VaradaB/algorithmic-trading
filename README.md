Microsoft Azure Machine Learning Scholarship Project Showcasing Challenge
Team:
@Lin C. @Somya Dwivedi @Varada.B @Garima Sharma @Gayathri Rajan, @tejas, @Varsha.Gore @Akhilesh @ Lamiae Hana

Problem Statement
Our project showcase challenge is to take an algorithmic approach to stock trading. On Kaggle we found an open data set of the Dow Jones Industrial Average (DJIA),  covering eight years and also the top 27 Reddit news during that same time frame (citation Daily News for Stock Market Prediction). Our problem was to use machine learning models to explain and forecast. Specifically we applied various regression algorithms to the Dow Jones industrial average and used natural language processing (NLP) analysis on the Reddit news to see if it had a predictor influence on whether the Dow Jones close daily price went up, down or stayed the same.
 
Why is this problem statement an important one? 
The stock market is fundamentally a financial institution for companies to raise capital. A share in a stock represents an ownership of a fractional piece of the company. Wall Street, a collective of where stocks are bought, sold, and where capital is raised, is often thought of as having a ‘random walk’ ( Citation: Random Walk Down Wall Street).  This means the underlying data set has statistical attributes that are defined as random. 
Financial markets are highly adversarial in nature and non-stationary. They change all the time, driven by political, social, economic or natural events. As human emotions and psychology are the driving force behind investment decisions and Wall Street.  
 
We believed the top Reddit news is a capable proxy for human emotions. An important component of a stock is it’s price and what it represents. It represents the sum of all future earnings, taken to its current net present value. We are using the DJIA as a proxy for the broad US stock market and it’s stock values. As an index, the DJIA has transparency or openess, meaning it’s value is reported continuously, during open trading hours, visible to anyone with the internet.  The approach of using algorithmic trading is often proprietary, tightly held secrets of an investment company. With the advent of machine learning, it would be interesting to see if the underlying data sets and machine learning models can be exploited to forecast and explain DJIA and reddit news’ influences. 
 
We were eager to try out our own hands with algorithmic trading using machine learning.
 

Using Azure for Implementation based on Course Material (30%)
We used Azure Machine Learning Studio (classic).  Based on our knowledge gained from our class, we applied Azure to our Algorithmic trading, specifically using the regression analysis.    We applied our key learnings to gain insights on how well our models worked to explain DJIA. 
We used machine learning models in Jupyter notebook with classic preprocessing of the data set, then using text NLP algorithms, time series forecasting (ARIMA) and Recurrent Neural Networks.


Innovation and Creativity (20%):
This project is an innovative outcome of predicting the volatility of the stock market in terms of its opening, closing, high, low and average volume price combined with the sentiments of top news that affected it. The combination of numerical as well as NLP part has made this project show some fruitful results.
Our project has also supported the results done from Azure and through manual coding. 
Impact & Potential (15%) 
As an index, the DJIA has transparency or openess, meaning it’s value is reported continuously, during open trading hours, visible to anyone with the internet. Obtaining real time price quotes allows for an orderly buying and selling of stocks. Based on algorithmic trading, companies will have more predictable valuation when going through initial public offerings and individual investors benefit from quantifying their investment risks. So when these technologies are deployed correctly, they will make investors more efficient so when people invest, they will invest following scientific approaches rather than making wild speculation.

Dataset:
We used dataset from Kaggle : - Daily News for Stock Market Prediction

Azure- Model Architecture, training/validation, and metrics.

Model Architecture: We applied eight regression models: Bayesian linear regression, decision forest regression, boosted decision tree regression, fast forest quantile regression, neural network regression, ordinal regression and Poisson regression. We compared the output for each. See Figure 1. 
Model Training: We split the dataset 80% for training, and 20% for testing with the dates column. 
Model Metrics: We used RMSE with Bayes Linear Regression and Linear Regression gave the lowest RMSE. 

Figure 1


Table 1: RMSE Results by Algorithm
Dow Jones Index- Regression
Data split ( 80/20)
Target 'High' RMSE
Target 'Close' RMSE
Notes
Decision forest Regression
<01/01/2015
91
100


Boosted Decision Tree Regression
<01/01/2015
121
121


Bayes Linear Regression
<01/02/2015
54
61


Linear Regression
<01/01/2015
54
61


Poisson Regression
<01/01/2015
563
573


Ordinal Regression
<01/01/2015
NA
NA
Not applicable
Fast Forest Quantile Regression
<01/01/2015
82
87
50% quantile loss
Neural Network Regression
<01/01/2015
Error
Error
Error in output


5. Responsible AI : 
The predictions results from our models and analysis  will not be used for any wrong purposes. Models used here will perform safely and will be secure. As far as privacy is concerned the dataset we used is an open dataset on Kaggle, which is public. We have stacked stocks from different companies and our models are NOT biased towards any company's stock. All the fair practices have been used in the analysis  and all steps including coding are transparent. Explanations are given in detail and our models are not just black box one. Most importantly our team has included everyone in the team for tasks. Our team is an intentionally diverse team, where members have collaborated from four different time zones across the globe successfully.

NLP (Natural Language Processing)

NLP was used to understand how much the news impacted the stock market. The combination of numerical analysis and NLP analysis gave us fruitful results. The dataset that we obtained from Kaggle consisted of Top 25 news from Reddit WorldNews Channel. The NLP was carried out using three different models. This was done so that we could compare which model gave us better results.

MODEL 1

We concatenated all the News Headlines of a single day into one. We used TF-IDF (Term Frequency–Inverse Document Frequency) vectorization to extract a feature vector. The classifier we used was a SVM ( Support Vector Machine) with RBF (Radial Basis Function) kernel without optimization of hyperparameters.

RESULT :- We obtained an Accuracy of 53.9% and ROC-AUC  of 0.52 

MODEL 2

For model 2 we used Count vectorizer and Logistic Regression. n-grams are basically a set of co-occurring words within a given window and when computing the n-grams you typically move one word forward. We have tested with 1-gram,2-gram and 3-gram.

RESULT :- 

n-gram
Accuracy
1-gram
83%
2-gram
84%
3-gram
85.7%

The ROC - AUC of the model is 0.95

MODEL -3 

For model 3 we combined the columns of numerical part (open, high, low, close, volume, adj close) and Sentiment columns (subjectivity, objectivity, positive, neutral, negative) of the dataset.

RESULT : - 

 The Linear Discriminant Analysis score is 0.943 and ROC -AUC is 0.5

MODEL -4

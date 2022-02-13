# Machine Learning Model
For the purposes of this project, we could use the following statistical techniques and machine learning models:

## Correlation analysis
First of all, as we are interested on identify the linear relationship between some variables and compute their association, we must set up a correlation analysis also this will help us to identify the potential variables of interest, high correlation points to a strong relationship between the two variables. The result will show us the direction of the relationship (positive or negative correlation) or if not exist correlation.

## Principal Component Analysis
We will use this statistical technique to group similar variables reducing the number of dimensions by transforming a large set of variables into a smaller one that contains most of the information. Using this technique will depend in the number of variables that could be correlated. 

## Linear and multiple linear regression
We will use linear regression and multiple linear models as an exploratory tool to quantify and measure the variability of two or more correlated variables, in fact linear regression is an extension of the correlation analysis. Linear regression could help us to know if values from some variables let us predict values for our dependent variable. Using a multiple linear regression, we can try with multiple independent variables to account for parts of the total variance observed in the dependent variable.

We will use the significancy for each independent variable to determine if there is a significant relationship with the dependent variable. Once we have evaluated each independent variable, we'll evaluate the r-squared value of the model to determine if the model sufficiently predicts our dependent variable.

Assumptions:
1.	The input data is numerical and continuous.
2.	The input data should follow a linear pattern.
3.	There is variability in the independent x variable. 
4.	The residual error (the distance from each data point to the line) should be normally distributed.

## Machine learning models
We believe we can use some supervised model to deal with our research question, as we know who the winner for every race was. Machine learning models let us predict, based on data from previous patients who driver could win based on some features

### Supervised Learning
Logistic regression predicts binary outcomes and evaluates the probability of an occurrence, so we can calculate the percentage of possibility for one drive who own to one constructor to win a race using multiple variables as qualify position, time on pit stops, drivers experience and also tracks. The model would take features into account and decide whether a driver can or not win meaning that there are only two possible outcomes.

Like logistic regression, Support vector machine (SVM) is another supervised learning model that we can use to classify if a sample is categorized into one of two possibilities (win or lose). Finally applying a Random forest algorithm, we can rank the importance of input variables in order to remove some variables that could be affecting the model. 

Depending in our final dataset, if It has many data points or complex features, may overwhelm the previous models, in that case we could attempt to use a deep learning model as neural networks to evaluate every interaction within and across neurons. 

### Unsupervised Learning
At this moment, we cannot rule out the use of an unsupervised learning model, even when we know the previous result on our database. We can use this type of model to find hidden patterns.

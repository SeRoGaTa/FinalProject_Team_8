# Machine learning models

## Description of preliminary data preprocessing

To answer the research question, it was necessary to explore all the available tables to identify which variables could be used for the models.

The tables that were initially selected have information from 1950 to 2021. Carrying out a preliminary exploration of the tables, the table that has the greatest amount of information is results.csv, which has 18 columns and a total of 25,399 observations, being this the main table for this project.

imagen 1

However, due to the modifications in the formula 1 regulations, changes in the scoring and classification formats, the project period would cover from 2018 to 2021. Once the filter was made, the table was left with 1619 observations.

imagen 2

Regarding the information from this table, it can be identified that the variable that give an answer to the study question is the column called positionOrder (Final Position) that presents the final positions of all the drivers for each race. Determining which are the most relevant factors to predict the result of the race requires knowing the final result.

To obtain the name of the constructors and drivers, we perform a merge of our main dataframe (maindf) with the constructors.csv and drivers.csv tables. In this way some patterns can be identified.

imagen 3

From the graph it can be interpreted that the most successful teams in the study period are Mercedes, Red Bull and Ferrari, while those that obtain the most negative results are Williams, Haas and AlfaRomeo.

imagen 4 y 5

Plotting the final results by driver, we can see that the drivers with the best results are Hamilton, Max Verstappen and Bottas. While the drivers with the worst ratings are Pietro Fittipaldi and Mazepin.

But what does the result of an F1 race depend on, the constructor or the driver? 

From the original database, the starting position variable (Grid) is identified, which could be related to the driver's ability to start the race in a good position. Carrying out the first correlations, it is observed that the starting position is highly related to the final position.

imagen 6

It can be seen that it is more common for a driver who starts in the first places to end up in the first places, it is even observed the difficulty that a driver who starts in the last positions get to the first positions, however, it is more common for drivers who start in the first places to finish in last places, so it is understood that in addition to the starting position there are other variables that could explain who is the winner of a race.

Referring to the weight of the constructor in determining the winner of a race, we can identify the rankfast variable (Rank) that ranks the cars according to the times of the fastest laps of the entire race. This variable refers to the maximum speed that a vehicle can reach and therefore it can be determined that it depends more on the constructor.

imagen 7

The results of the correlation graph indicate a high relationship between the maximum speed of a car and the final position, where the slowest cars in general always finish in the last places, however, there are cases where fast cars end in last places, showing that there are other factors that affect the final result.

### Description of preliminary feature engineering and preliminary feature selection, including their decision-making process

With this in mind, more variables are created and analyzed to explain the principal factor that determined the final result of a race. The variables were classified according to their relationship with the driver or constructor. All the code for the calculation of these variables can be found in the CleaningData folder named PreprocessingData.ipynb

**Constructor**

- Pit-stops strategy 

In the pit-stops variable, the relationship between the winner of the race is not determinant. This can be easily seen, since a constructor that finishes first and a constructor that finishes last can have the same number of pit stops. The variation between the number of stops per team is not representative in the graph. Likewise, in this graph you can see cases where there are more pit-stops than what is estimated on average among constructors.

Imagen 8

- Constructor points per season

During each race, each constructor gets a sum of point depending on the final place, at the end of the season the constructor end with a total sum of points. Regarding the correlation between the season points and the final position, it is shown that the constructor that has more points accumulated during the season, will be the constructor that end in the first place.

Imagen 9

- Constructor points per circuit

As mention before, the constructor gets points in every circuit, in this correlational chart is shown almost the same behavior that it is shown in the last variable (points per season). If a constructor gets more points in a circuit it will be the winner of that circuit, also it is important to mention, that this is a constructor analysis, meaning that the total of points is the sum of points that every pilot gets for the team.

Imagen 10

- Constructor failures average per circuit

In every race it is common that at least one constructor present a failure during a race, as shown in the next image, in average the majority of the constructor has between 0 and 1 failure during a circuit. In rare cases there are constructors that has more than 5 failures during a circuit, but this is not a normal behavior.

Imagen 11

- Constructor Failures Average per circuit to each driver 

To understand the behavior of this variable, the average number of failures per pilot was also calculated, which are related to manufacturer failures. In general, the number of faults is never greater than 1 for each circuit.

1magen 12

According to the data, the manufacturers with the highest number of failures are Ferrari and McLaren, while the drivers with the highest average number of failures are Alonso and Ricciardo. In the next graphics it is shown the number of failures each constructor had has, and also per driver.

1magen 13 y 14

**Driver**

- Drivers experience by number of years competing


To calculate the experience variable, the total number of years that each driver has driven was counted and the Rank() function was applied to order in descending order, where the value of 1 represents the runner with the most experience.

imagen 15 

This correlation presents a relationship between the runners with the greatest number of years of competition and the final position of the race.

- Total number of races 

To calculate this variable, we add the total number of races that each of the drivers has run, then the Rank() function is applied to order them in descending order, where the value of 1 represents the runner with the most experience.

Imagen 16

It is observed that the greater experience, the more possibilities a pilot has to remain in the first positions, but not so the pilots with less experience, who usually remain in the last places.

- Most winning drivers by position

This variable was calculated by filtering the runners who have won a race, then the sum per runner is obtained and the column is added to the maindf, then the Rank() function was applied to order in descending order, where the value of 1 represents the runner with the highest number of wins.

Imagen 17

In this case, although the relationship is not strong, it is observed that the runners who have won once have a good chance of winning again, however, the result is not totally determinant.

- Number of times driver has run each circuit (Track experience)

To calculate this variable, we add the total number of races that each of the drivers has run on each of the tracks, then the Rank() function was applied to order in descending order, where the value of 1 represents the runner with the most experience. on each of the tracks.

imagen 18

For this correlation, such a linear relationship is not observed, which can be explained because there are some tracks that have been run a few times and even so there is a winner or there are drivers who, despite having a lot of experience, can end up in the last places.

- Drivers Qualifying pole wins 

To calculate this variable, the sum of the times a driver has a qualifying position for all the races is obtained.

imagen 19

It is observed that the pilots who have had the pole position at some time are more likely to be in the first places than those who have never won it.

- Average of crashes per pilot

In a F1 race, crashes are one thing that happen and affect the result of the race. In average a pilot has less than 0.14 crash, but as it is shown in the graphic as higher is the number of crashes, the result will be losing the race.

imagen 20

- Driver total points

Points are awarded to drivers in every race they finish, the winner receives 25 points, the second finisher 18 points, and so on. The next image shows how the points are distributed by driver, and it is shown that the distribution of point per driver is divided between all drivers.

imagen 21

**External factors**

- Weather 

Taking in count the weather variable we can see that is not a determinant variable, it can  affect the race, but as seen on the graph, the result remain the same. This may be due to the fact that adverse weather conditions affect all pilots in general in the same way.

imagen 21a

To obtain this variable, a webscrapping code was adopted that obtains the information directly from Wikipedia. The webscrapping code is in the CleaningData folder named Weather.ipynb

### Correlation analysis

With the obtained variables, it was decided to carry out the modeling process, the code of these calculations can be found in the CleaningData folder named MachineLearningMode.ipynb

We are interested on identify the linear relationship between some variables and compute their association, set up a correlation analysis also will help to identify the potential variables of interest, high correlation points to a strong relationship between the two variables. The result will show us the direction of the relationship (positive or negative correlation) or if not exist correlation.

In order to know how the variables are related, it was decided to make a correlation matrix that would present us with the dependence of each one.

imagen 22

The variables with the greatest relationship between them are those that refer to the experience of the driver (rank_yrs_exp_driver and rank_exp_driver)

### Multiple linear regression

Multiple linear models could work as an exploratory tool to quantify and measure the variability of two or more correlated variables, in fact linear regression is an extension of the correlation analysis. Linear regression could help us to know if values from some variables let us predict values for our dependent variable. 

Using a multiple linear regression, we can try with multiple independent variables to account for parts of the total variance observed in the dependent variable. To understand the relationship between the variables and their degree of significance, a multiple linear regression model was run.

imagen 23

The results show that despite having a significant R squared of 89%, there are indications of multicollinearity in our variables, that is, there are variables that have a high correlation between more than two explanatory variables.

To try to solve the multicollinearity problem, it was decided to create a specific model for the variables that corresponded to the driver and another for the constructor.

imagen 24 y imagen 25

From the results it is observed that the pilot model also presents multicollinearity problems, on the other hand, the constructor model does not present problems and obtains an R squared of 81%. The complete results can be reviewed in detail in the code of the models

Finally, we fit a model considering only the variables that presented a high correlation in the Pearson correlation result. With 7 variables, the model adjusted to 88%, resulting in all variables being significant at 95%. As a result the r-squared value mean that the model predicts the dependent variable.

imagen 26

## Description of how data was split into training and testing sets 

The dataset was split into two: train and test datasets in order to know how well the model will perform when it encounters unseen data. As the model uses the training dataset to learn from it then uses the testing dataset to assess its performance it's important to set aside a portion of your dataset to evaluate the model.

Scikit-learn's train_test_split module takes X and y as arguments and splits each into training and test sets. The train_test_split() function has four arguments. The random_state was settled on “0” in order to get the same rows assigned to train and test sets, respectively. Also the stratify argument was added to divide the data proportionally finally for the test size we use the default value (25%) In other words, 75% of the dataset were allocate to the training set, and 25% to the testing set. 

imagen 27

## Explanation of model choice, including limitations and benefits

### Supervised Learning Models 

Supervised machine learning model type could deal with the research question, as the database have a columnn with the final position for every race. Machine learning models helps to predict, based on data from previous patients who driver could win based on some features.

For the exercise, 4 different types of model were run, logistic regressions, Support Vector Machines, Random Forest Classifier and Gradient Boosting Classifier.

Logistic regression predicts binary outcomes and evaluates the probability of an occurrence. The model would take features into account and decide whether a driver can or not win meaning that there are only two possible outcomes.

imagen 28

Like logistic regression, Support vector machine (SVM) is another supervised learning model that can be uses to classify if a sample is categorized into one of two possibilities (win or lose).

imagen 29

Applying a Random forest algorithm, we can rank the importance of input variables in order to remove some variables that could be affecting the model. 

imagen 30

Gradient boosting is a type of machine learning boosting. It relies on the intuition that the best possible next model, when combined with previous models, minimizes the overall prediction error. The key idea is to set the target outcomes for this next model in order to minimize the error.

imagen 31

To compare the performance of all the models, a comparative table was created, it is observed that logistic regression model is the one that presents the highest precision and the highest result in the F1 Score.

imagen 32

Because the results are low, even for the logistic regression model, it was decided to run a neural network model to evaluate every interaction within and across neurons. With two hidden layers we can get a Loss of 0.27 and an accuracy of 0.95.

### Next steps

Component Analysis statistical technique, could group similar variables reducing the number of dimensions by transforming a large set of variables into a smaller one that contains most of the information. The use of this technique will depend in the number of variables that could be correlated. 

Another alternative is to try to improve the performance of the logarithmic model by reducing the number of variables in the model, since some could be generating noise.
# Formula 1
The selected topic for our project is "Formula 1 history through data analysis", the purpose of this project is to show the relevance of data analysis through this sport, provide a better understanding of the sport to existing fans and provide an introduction through hard data to new fans.

Formula 1 has raised a lot of debate about the importance of the cars, the skill of the drivers as well as the teams´ performance, from the very beginning of the sport.
F1 is a racing competition that has an incredible history through all these years, being the 50’s when all this started. The F1 has a lot of data and statistics that are used to get more information about how to improve the performance in every race.

With every single competition or race performed, hard data from the event is provided just like racing times, number of laps, pit stops, drivers’ final positions, etc. that can help analyze more intangible characteristics, just like skill, teams´ preparation or drivers’ resilience through data analysis.

The data for analysis is available and verifiable, also, the data is diverse (times, stop counts, accidents, mechanical failures, etc.) so is perfect to demonstrate and place in practice the importance of data analysis for understanding sports, businesses, history and almost every topic that can be measured.

In this project, we are interested in identifying and determining the main factors that have an effect in a race and its impact in the outcome.
Formula 1 races have two fundamental elements that constantly interact, the drivers and the cars.


## Database Source

We looked for information that can be usable for these purposes, the characteristics of the data that we could use for the purposes of our project are the following:
•	Should be accurate.
•	Should be verifiable.
•	Should be diverse enough to perform our analysis.

Accuracy

Through the research of readily an accurate data the project team identified a compile that is useful for this purpose.
The project team inspected randomly some of the data to verify its accuracy through researching on motorsport websites and news to compare the data to the events reported on specialized media. 

The project team concluded that the data is accurate and can be used for the purpose of this project.
Diversity

An important aspect of the data sources was the diversity of the available data, on the compile can be identified diverse datasets that are useful for the project, a list and description of the datasets is as follows:
![image](https://user-images.githubusercontent.com/90175232/155905116-522c211d-8a8e-4821-b211-2afd9d1d663f.png)


Table 1.- Circuits

The information included in this dataset is circuit reference, name, location, country, lat & long, altitude.
 
The data provided in this data set is a description and location of the places where the races have occurred from 1950 to 2021.

Table 2.- Constructor results

The data set includes the Raceid, constructor id, points, status
 
This dataset includes a list of teams of car manufacturers and an identifier number from 1950 to 2021, also displays the number of points earned per race. In this dataset we can identify for the first time the raceid, which assigns an identifier and unique number to every single race taken from 1950 to 2021.

Table 3.- Constructor standings

This dataset includes the following data: Raceid, constructor id, points, position, positionText, wins.
The information presented in this dataset details the results of the constructors per race id.
Every constructor has two cars per race, however this data is presented per constructor and not per car.

Table 4.- Constructors

This dataset includes the following information: Constructor id, constructor ref, name, nationality.
This is basic information of the constructor team and it’s assigned identifier number.

Table 5.- Driver standings

This data set includes the following information: Raceid, driverid, points, position, positionText, wins.
What this dataset represents is the outcome of every single pilot through all races run from 1950 to 2021, meaning as outcome the position achieved at the end of the race and points earned during the session. 

Table 6.- Drivers

This dataset includes the following information: Driverid, driver ref, number, code, forename, surname, dob, nationality
 
This dataset displays basic information about every pilot that has raced in Formula 1 from 1950 to 2021, it assigns as well as a unique identifier number so it can be used in other datasets.

Table 7.- Lap Times

The dataset includes the following information: Raceid, driverid, lap, postion, time, milliseconds.
This dataset includes the time taken for every single driver to drive a lap in every course for every race from 1950 to 2021.

Table 8.- Pit stops

The dataset includes the following information: Raceid, driverid, stop, lap, time, duration, milliseconds.
As a reference, a pit stop is a “break” taken during the race to change tires, fuel the car or repair any problem with the car, every single race usually requires at least one pit stop per driver.
The dataset provides a list of the pit stops taken by driver for every single race and the duration (in time) that each pit stop took.

Table 9.- Qualifying

The dataset includes the following information: Qualifyid, raceid, driverid, constructorid, number, position, q1, q2, q3.
As a reference, the position from where a pilot will start a race is determined by the previous qualification, for most of the cases the qualification consist in driving the course where the race will be taken place, the pilot that takes the least time In completing a lap is the pilot who will start in first place and so on, there are some other qualification models for a few races where a brief race with less laps is considered for qualification, the position where the pilots finish this race, will be the position where the pilots will start in the main race.
The dataset assigns an identifier for the qualification event, the race that is corresponds, the drivers that participated in the qualification, as well as the outcome.

Table 10.- Races
The dataset includes the following information: Raceid, year, round, circuitid, name, date, time
 
This dataset includes basic information about every race taken place from 1950 to 2021 and assigns a unique identifier number.

Table 11.- Results

The dataset includes the following information: Resultid, raceid, driverid, constructorid, number, grid, position, positionText, points, laps, time, rank, statusid.
This dataset consolidates many of the date detailed  in the datasets described above and provides information about a general outcome of every race and the results of every pilot.

Table 12.- Seasons

The dataset includes the following information: Years
This dataset describes the year of the season to identify when the races took place.

Table13.- Status

The dataset includes the following information: Statusid, status.
This dataset describes and assigns an identifier number to the status of the driver at the end of the race, example: if the pilot finished the race, if he had an accident, an engine malfunction, crashing incidents, etc.
The project team concluded that the databases are diverse enough to be used in this project.
The compilation can be found in the following URL:
Formula 1 World Championship (1950 - 2021)
URL: https://www.kaggle.com/rohanrao/formula-1-world-championship-1950-2020

## Questions to be answered

The objective of the project is to display all the relevant data generated from this sport to obtain and understanding of the sport through data analysis for fans and new enthusiasts of the sport.

Build a narrative of how the results and outcomes per race are built through data analysis and use this information and understanding to predict the outcome of the incoming races and consequently the season winner.

Some of the questions we have initially designed with the available datasets are the following:

•	How relevant is the driver vs the car to determine a championship output?
•	How relevant is the pit stop average time to a championship output?
•	Which are the most relevant mechanical failures to determine a constructor, championship output?
•	How relevant is the number of pole positions to the championship output?
•	Which factor is the determinant to get a F1 winner?
•	Factors like time in the pits, type of tracks, crucial faults, qualifying times affect the result?

For us to get to the answer we are going to analyze the data regarding some important racing factors.

•	Pits times
•	Qualification
•	Wins per constructor
•	Wins per pilot
•	Lap times
•	Circuits characteristics
•	Race results

## Database integration

Once that the project team has obtained a useful data source, the next step will be analyzing the data and integrate all the useful information to calculate new relevant variables for the project.
The datasets are formatted in csv, so the team inspected datatypes in jupyter notebook, looked for null data or any other anomaly on the datasets that would need to be cleaned.
Once cleaned, we inspected the datatypes, the datatypes for the relevant inputs are the following:


We performed in jupyter notebook with Python code changes to datatypes to numerical data presented as object to perform calculations and determine correlations between data.

To start the database integration we followed the following steps:
•	Read the CSV files with PySpark.
•	Convert CSV to dataframes.
•	Use Postgress to map the dataframes and run a squema to build a single database that integrates all the relevant data from different dataframes.
•	Merge the dataframes to create a single “Main” database.
•	Upload the database to AWS.
The results of the mapping of the dataframes to integrate the database is as follows:
![image](https://user-images.githubusercontent.com/90175232/155905084-6e6f8c09-37ef-418b-a5c1-6eee31fe2597.png)

![image](https://user-images.githubusercontent.com/90175232/155905091-5c8ebd89-5043-4867-8b06-62435fcf4e89.png)


## Machine learning models

After cleaning and grouping the relevant datasets, we will use a non supervised machine learning model to expose relevant correlations that are not evident, select the most meaningful ones and then predict possibles outcomes through supervised machine learning.

For the purposes of this project, we could use the following statistical techniques and machine learning models:

### Correlation analysis

First of all, as we are interested on identify the linear relationship between some variables and compute their association, we must set up a correlation analysis also this will help us to identify the potential variables of interest, high correlation points to a strong relationship between the two variables. The result will show us the direction of the relationship (positive or negative correlation) or if not exist correlation.

### Principal Component Analysis

We will use this statistical technique to group similar variables reducing the number of dimensions by transforming a large set of variables into a smaller one that contains most of the information. Using this technique will depend in the number of variables that could be correlated.

### Linear and multiple linear regression

We will use linear regression and multiple linear models as an exploratory tool to quantify and measure the variability of two or more correlated variables, in fact linear regression is an extension of the correlation analysis. Linear regression could help us to know if values from some variables let us predict values for our dependent variable. Using a multiple linear regression, we can try with multiple independent variables to account for parts of the total variance observed in the dependent variable.

We will use the significancy for each independent variable to determine if there is a significant relationship with the dependent variable. Once we have evaluated each independent variable, we'll evaluate the r-squared value of the model to determine if the model sufficiently predicts our dependent variable.

Assumptions:

- The input data is numerical and continuous.
- The input data should follow a linear pattern.
- There is variability in the independent x variable.
- The residual error (the distance from each data point to the line) should be normally distributed.

### Supervised Learning

We believe we can use some supervised model to deal with our research question, as we know who the winner for every race was. Machine learning models let us predict, based on data from previous patients who driver could win based on some features

Logistic regression predicts binary outcomes and evaluates the probability of an occurrence, so we can calculate the percentage of possibility for one drive who own to one constructor to win a race using multiple variables as qualify position, time on pit stops, drivers experience and also tracks. The model would take features into account and decide whether a driver can or not win meaning that there are only two possible outcomes.

Like logistic regression, Support vector machine (SVM) is another supervised learning model that we can use to classify if a sample is categorized into one of two possibilities (win or lose). Finally applying a Random forest algorithm, we can rank the importance of input variables in order to remove some variables that could be affecting the model.

Depending in our final dataset, if It has many data points or complex features, may overwhelm the previous models, in that case we could attempt to use a deep learning model as neural networks to evaluate every interaction within and across neurons.

### Unsupervised Learning

At this moment, we cannot rule out the use of an unsupervised learning model, even when we know the previous result on our database. We can use this type of model to find hidden patterns.

## Communication protocols

We decide to use direct messages for only team members in Slack and establish a daily meetup time for everyone on saturdays.

We use GitHub as a communication protocol by creating a personal branch for each member. Git allow us to save the progress of the project and keep the tracks of our work.

### Create a branch

Using branches let us work on our local repository to then update to the main branch and have the chance to review the branch or offer suggestions. In this space we can test modifications in the code without the problem of affecting the global code or the advances made

```ruby
git Branch -d nomeofbranch
```

### Open a pull request

After having tested our code locally, we proceed to perform a pull request to merge the code

```ruby
git status
git add .
git commmit -m "Commit message"
git push --set upstream origin <Branch-Name>
```

### Discuss and review

At least one teammate has to review the pull request, if it is necessary suggest changes and approve the changes to be merged

  Merge and deploy

  After approval, the member who pull the request can merge the changes into the main branch

### Week logs

**Week 1**

During the first week, all the members of the team investigated topics of interest that would help us to decide on a topic to work on. By vote the team decided on the topic, later we agreed on the research question.
The team decided that each member of the team review the databases to become familiar with the data and meet over the weekend to determine which databases to use, if any transformations or joins are needed, and define the model to use.

## Database integration

  In the link mentioned above, we found datasets related to Formula 1 racing from the year 1950 to 2021, the datasets that we will use are formatted in csv and contain information about:

  circuits.csv constructor_results.csv constructor_standings.csv constructors.csv driver_standings.csv drivers.csv lap_times.csv pit_stops.csv qualifying.csv races.csv results.csv seasons.csv status.csv


  The database that we are using has information regarding some important aspects about F1.
  
- Circuits
  - Constructor results
  - Constructor standing
  - Constructors
  - Driver standings
  - Drivers
  - Lap times
  - Pit stops
  - Qualifying
  - Races
  - Results
  - Seasons
  - Status

We are going to analyzed this data and clean it, and get only the information that will help us to get the answered that we are looking for. The answer to our question “- Which factor is the determinant to get a F1 winner?”.

  The data is presented in csv format.

  **Table 1.- Circuits**

  Circuit reference, name, location, country, lat & long, alt
  
  <img width="848" alt="Screen Shot 2022-02-13 at 15 56 56" src="https://user-images.githubusercontent.com/90534703/153774805-0d3824af-ebed-447b-82c9-39ab67ad3fd1.png">

  **Table 2.- Constructor results**

  Raceid, constructor id, points, status
  
  <img width="854" alt="Screen Shot 2022-02-13 at 15 57 03" src="https://user-images.githubusercontent.com/90534703/153774813-05474566-94d3-4032-b898-879a9b193a4f.png">

  **Table 3.- Constructor standings**

  Raceid, constructor id, points, position, positionText, wins

  **Table 4.- Constructors**

  Constructor id, constructor ref, name, nationality

  **Table 5.- Driver standings**

  Raceid, driverid, points, position, positionText, wins

  **Table 6.- Drivers**

  Driverid, driver ref, number, code, forename, surname, dob, nationality
  
 <img width="835" alt="Screen Shot 2022-02-13 at 15 57 07" src="https://user-images.githubusercontent.com/90534703/153774821-d120ea1b-550d-4292-9551-700d4fba41ad.png">

  **Table 7.- Lap Times**

  Raceid, driverid, lap, postion, time, milliseconds

  **Table 8.- Pit stops**

  Raceid, driverid, stop, lap, time, duration, milliseconds

  **Table 9.- Qualifying**

  Qualifyid, raceid, driverid, constructorid, number, position, q1, q2, q3

  **Table 10.- Races**

  Raceid, year, round, circuitid, name, date, time
  
  <img width="860" alt="Screen Shot 2022-02-13 at 15 57 12" src="https://user-images.githubusercontent.com/90534703/153774834-6ba1a58d-d952-4b28-a879-d605eeabe2c1.png">

  **Table 11.- Results**

  Resultid, raceid, driverid, constructorid, number, grid, position, positionText, points, laps, time, rank, statusid

  **Table 12.- Seasons**

  Years

  **Table13.- Status**

  Statusid, status

## Visual representation and dashboards

The results and graphic representation of the project will be displayed in Tableau.
The objective of the project is to give an appropriate context of the sport through data before trying to predict the outcome of future races, so we will create and plot worksheets with relevant information to give the user a complete story and relevant data of the sport.

The worksheets and the visual representation that will be used are as follows:

![image](https://user-images.githubusercontent.com/90175232/155905196-ea0753ae-e1ff-4e3e-bb0b-bd2420ef8927.png)
The final dashboard will include a combination of this worksheets visual representation.



## Technologies Used

Data Cleaning and Analysis

  Pandas will be used to clean the data and perform an exploratory analysis. Further analysis will be completed using Python. As a query techonoly we will use some SQL in Postgres to merge and analyze the complete data prior to start our analysis.

  - Database Storage

  Postgres will be the tool we will use to store our data in SQL, we will use pandas to read the information out from a CSV source and will move those dataframes into a SQL databases.

  We will use 13 F1 related data.

- Machine Learning

  For Correlation analysis we will use R geom_point() plotting function combined with the cor() function to quantify the correlation between variables. Also we will use the lm() function in R or the sklearn for linear regression module in python to calculate the multiple linear regression model. The idea is to apply linear regression to define the level of relationship between variables

  For Machine Learning we are planning to use sklearn (LogisticRegression, SVC and RandomForestClassifier) module and hvplot for ploting mainly. Also if it is necessary we will use tensorflow to run a neural network model
  
  Other statistical techniques as PCA will help us to create clusters and with that define if either the constructor or the pilot has more leverage on winning a race.

- Dashboard
  
  In order to create visual graphs and the story telling about our analysis, we will use Tableau and python as the visualisation tool among others. With this we will be able to share our findings in a more graphical manner for our collaborators.

## Team members

  -Ricardo Barba @ -Sergio Gaytan @ -Jorge Ponce @ -Raciel Tavitas @

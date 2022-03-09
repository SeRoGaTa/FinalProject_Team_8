# FinalProject_Team_8

Topic selected	Why we choose the topic?
	Question to be answered
Technologies used	Data cleaning and analysis
	Database storage
	Machine Learning
	Dashboard
Database	Extraction and description
	Data exploration and analysis
	Database integration
Machine learning models	Logistic regressions
	Support vector machines
	Random forest classifier
	Gradient boost classifier
Visual representation and dashboards	Visual representation of context data
	Visual representation of ML models
Links	Presentation
	Interactive dashboard
![image](https://user-images.githubusercontent.com/90175232/157557810-35017bb7-e196-4c89-8bdc-64c7f77ada23.png)






### Team members

  -Ricardo Barba @ -Sergio Gaytan @ -Jorge Ponce @ -Raciel Tavitas @

# Formula 1
The selected topic for our project is "Formula 1 history through data analysis", the purpose of this project is to show the relevance of data analysis through this sport, provide a better understanding of the sport to existing fans and provide an introduction through hard data to new fans.

Formula 1 has raised a lot of debate about the importance of the cars, the skill of the drivers as well as the teams´ performance, from the very beginning of the sport.
F1 is a racing competition that has an incredible history through all these years, being the 50’s when all this started. The F1 has a lot of data and statistics that are used to get more information about how to improve the performance in every race.

With every single competition or race performed, hard data from the event is provided just like racing times, number of laps, pit stops, drivers’ final positions, etc. that can help analyze more intangible characteristics, just like skill, teams´ preparation or drivers’ resilience through data analysis.

The data for analysis is available and verifiable, also, the data is diverse (times, stop counts, accidents, mechanical failures, etc.) so is able to demonstrate and place in practice the importance of data analysis for understanding sports, businesses, history and almost every topic that can be measured.

In this project, we are interested in identifying and determining the main factors that have an effect in a race and its impact in the outcome.
Formula 1 races have two fundamental elements that constantly interact, the drivers and the cars.

## Questions to be answered

The objective of the project is to display all the relevant data generated from this sport to obtain and understanding of the sport through data analysis for fans and new enthusiasts of the sport.

Build a narrative of how the results and outcomes per race are built through data analysis and use this information and understanding to predict the outcome of the incoming races and consequently the season winner.

Some of the questions we have initially designed with the available datasets are the following:

•	How relevant is the driver vs the car to determine a race output?

•	How relevant are the number of pit stop to determine a race output?

•	Are the mechanical failures relevant to determine a race output or winner?

•	How relevant are the number of pole positions to determine a race output or winner?

•	Which factors are the determinant to get a F1 race winner?

•	Identify which other variables could be relevant to affect the result of a race.

### Technologies Used

 - Data Cleaning and Analysis

Python pyspark and pandas will be used to clean the data and perform an exploratory analysis. As a query technology we will use SQL in PG Admin4  to merge and query the complete data prior to start our analysis.
 
 - Database Storage

AWS RDS, AWS S3, Python Pyspark and postgres will be the tools we will use to store and read our data from SQL cloud service, we will use python to read the information out from SQL source and will start the analysis from there.


  We will use 15 F1 related data.

- Machine Learning

For Correlation analysis we will use python to quantify the correlation between variables. Also we will use the sklearn for linear regression module in python to calculate the multiple linear regression model. The idea is to apply linear regression to define the level of relationship between variables

For Machine Learning we are planning to use sklearn (LogisticRegression, SVC and RandomForestClassifier) module. Also if it is necessary we will use tensorflow to run a neural network model

 - Dashboard

In order to create visual graphs and the story telling about our analysis, we will use Tableau and python as the visualization tool among others. With this we will be able to share our findings in a more graphical manner for our collaborators.

### Database

The database is the main input for the project, the databse processing will be distributed as follows:

•	Extract

•	Data exploration and transformation

•	Load database for use


## Extraction and description

The first step of the project is to identify useful sources and databaes for the purposes of this project, the characteristics of the database are:

•	Should be accurate.

•	Should be verifiable.

•	Should be diverse enough to perform our analysis.

Through the research of readily an accurate data the project team identified a compile that is useful for this purpose.

The project team inspected randomly some of the data to verify its accuracy through researching on motorsport websites and news to compare the data to the events reported on specialized media. 

The project team concluded that the data is accurate and can be used for the purpose of this project the compilation can be found in the following URL:
Formula 1 World Championship (1950 - 2021)

<details><summary>Tables Description</summary>

A description of the datasets extracted is detailed below:

**Table 1.- Circuits**

The information included in this dataset is circuit reference, name, location, country, lat & long, altitude.
 
The data provided in this data set is a description and location of the places where the races have occurred from 1950 to 2021.
  
<img width="700" alt="Screen Shot 2022-02-13 at 15 56 56" src="https://user-images.githubusercontent.com/90534703/153774805-0d3824af-ebed-447b-82c9-39ab67ad3fd1.png">

**Table 2.- Constructor results**

The data set includes the Raceid, constructor id, points, status
 
This dataset includes a list of teams of car manufacturers and an identifier number from 1950 to 2021, also displays the number of points earned per race. In this dataset we can identify for the first time the raceid, which assigns an identifier and unique number to every single race taken from 1950 to 2021.
  
<img width="700" alt="Screen Shot 2022-02-13 at 15 57 03" src="https://user-images.githubusercontent.com/90534703/153774813-05474566-94d3-4032-b898-879a9b193a4f.png">

**Table 3.- Constructor standings**

This dataset includes the following data: Raceid, constructor id, points, position, positionText, wins. The information presented in this dataset details the results of the constructors per race id. Every constructor has two cars per race, however this data is presented per constructor and not per car.

**Table 4.- Constructors**

This dataset includes the following information: Constructor id, constructor ref, name, nationality.

This is basic information of the constructor team and it’s assigned identifier number.

**Table 5.- Driver standings**

This data set includes the following information: Raceid, driverid, points, position, positionText, wins.

What this dataset represents is the outcome of every single pilot through all races run from 1950 to 2021, meaning as outcome the position achieved at the end of the race and points earned during the session. 

**Table 6.- Drivers**

This dataset includes the following information: Driverid, driver ref, number, code, forename, surname, dob, nationality
 
This dataset displays basic information about every pilot that has raced in Formula 1 from 1950 to 2021, it assigns as well as a unique identifier number so it can be used in other datasets.

<img width="835" alt="Screen Shot 2022-02-13 at 15 57 07" src="https://user-images.githubusercontent.com/90534703/153774821-d120ea1b-550d-4292-9551-700d4fba41ad.png">

**Table 7.- Lap Times**

The dataset includes the following information: Raceid, driverid, lap, postion, time, milliseconds.

This dataset includes the time taken for every single driver to drive a lap in every course for every race from 1950 to 2021.

**Table 8.- Pit stops**

The dataset includes the following information: Raceid, driverid, stop, lap, time, duration, milliseconds.

As a reference, a pit stop is a “break” taken during the race to change tires, fuel the car or repair any problem with the car, every single race usually requires at least one pit stop per driver.

The dataset provides a list of the pit stops taken by driver for every single race and the duration (in time) that each pit stop took.

**Table 9.- Qualifying**

The dataset includes the following information: Qualifyid, raceid, driverid, constructorid, number, position, q1, q2, q3.

As a reference, the position from where a pilot will start a race is determined by the previous qualification, for most of the cases the qualification consist in driving the course where the race will be taken place, the pilot that takes the least time In completing a lap is the pilot who will start in first place and so on, there are some other qualification models for a few races where a brief race with less laps is considered for qualification, the position where the pilots finish this race, will be the position where the pilots will start in the main race.

The dataset assigns an identifier for the qualification event, the race that is corresponds, the drivers that participated in the qualification, as well as the outcome.

**Table 10.- Races**

The dataset includes the following information: Raceid, year, round, circuitid, name, date, time
 
This dataset includes basic information about every race taken place from 1950 to 2021 and assigns a unique identifier number.
  
<img width="860" alt="Screen Shot 2022-02-13 at 15 57 12" src="https://user-images.githubusercontent.com/90534703/153774834-6ba1a58d-d952-4b28-a879-d605eeabe2c1.png">
  
**Table 11.- Results**

The dataset includes the following information: Resultid, raceid, driverid, constructorid, number, grid, position, positionText, points, laps, time, rank, statusid.

This dataset consolidates many of the date detailed  in the datasets described above and provides information about a general outcome of every race and the results of every pilot.

**Table 12.- Seasons**

The dataset includes the following information: Years

This dataset describes the year of the season to identify when the races took place.

**Table13.- Status**

The dataset includes the following information: Statusid, status.

This dataset describes and assigns an identifier number to the status of the driver at the end of the race, example: if the pilot finished the race, if he had an accident, an engine malfunction, crashing incidents, etc.

</details> 
</details>  

We are going to analyzed this data and clean it, and get only the information that will help us to get the answered that we are looking for. The answer to our question “- Which factor is the determinant to get a F1 winner?”.

## Data exploration and analysis

To answer the research questions, it was necessary to explore all the available tables to identify which variables could be used for the models.

The tables that were initially selected have information from 1950 to 2021. Carrying out a preliminary exploration of the tables, the table that has the greatest amount of information is results.csv, which has 18 columns and a total of 25,399 observations, being this the main table for this project.

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/97ae729293d3cbca9cf8f71370919f7f0acb455b/Images/Imagen1.png" width="550">

However, due to the modifications in the formula 1 regulations, changes in the scoring and classification formats, the project period would cover from 2018 to 2021. Once the filter was made, the table was left with 1619 observations.

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/97ae729293d3cbca9cf8f71370919f7f0acb455b/Images/Imagen2.png" width="550">

Regarding the information from this table, it can be identified that the variable that give an answer to the study question is the column called positionOrder (Final Position) that presents the final positions of all the drivers for each race. Determining which are the most relevant factors to predict the result of the race requires knowing the final result.

To obtain the name of the constructors and drivers, we perform a merge of our main dataframe (maindf) with the constructors.csv and drivers.csv tables. In this way some patterns can be identified.

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/97ae729293d3cbca9cf8f71370919f7f0acb455b/Images/Imagen3.png" width="850">

From the graph it can be interpreted that the most successful teams in the study period are Mercedes, Red Bull and Ferrari, while those that obtain the most negative results are Williams, Haas and AlfaRomeo.

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/97ae729293d3cbca9cf8f71370919f7f0acb455b/Images/Imagen4.png" width="850">

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/97ae729293d3cbca9cf8f71370919f7f0acb455b/Images/Imagen5.png" width="850">

Plotting the final results by driver, we can see that the drivers with the best results are Hamilton, Max Verstappen and Bottas. While the drivers with the worst ratings are Pietro Fittipaldi and Mazepin.

## Database integration

Once that the project team has obtained a useful data source, the next step will be analyzing the data and integrate all the useful information to calculate new relevant variables for the project.
The dataset was pushed into SQL from S3 storage in AWS, so the team inspected datatypes in google colab, looked for null data or any other anomaly on the datasets that would need to be cleaned.
Once cleaned, the data was written to the AWS RDS database with the help of postgres, the schema was previously created with PG Admin4. 

We performed in jupyter notebook with Python and google colab with pyspark code changes to datatypes to numerical data presented as object to perform calculations and determine correlations between data.

To start the database integration, we followed the following steps:
- Create an S3 bucket in AWS repository and save the CSV files (15) that will be used in the project.
- Read the CSV files with PySpark in google colab and clean datatypes for all the dataframes.
- Create a RDS instance in AWS to store the database
- Use PG Admin 4 to create the schema of the database in AWS RDS
- Use Pyspark and Postgress to write the dataframes into the database’s tables previously created.
- Use SQL in PG Admin to filter and then merge results and status tables to create a main table that will be used to start the complete analysis.

This is the visual schema and the relationships we will use:

![image](https://user-images.githubusercontent.com/90175232/155905084-6e6f8c09-37ef-418b-a5c1-6eee31fe2597.png)

![image](https://user-images.githubusercontent.com/90175232/155905091-5c8ebd89-5043-4867-8b06-62435fcf4e89.png)

## Machine learning models

Supervised machine learning model type could deal with the research question, as the database have a columnn with the final position for every race. Machine learning models helps to predict, based on data from previous patients who driver could win based on some features.

For the exercise, 4 different types of model were run, logistic regressions, Support Vector Machines, Random Forest Classifier and Gradient Boosting Classifier.

**Logistic regressions**

Logistic regression predicts binary outcomes and evaluates the probability of an occurrence. The model would take features into account and decide whether a driver can or not win meaning that there are only two possible outcomes.

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/2335a30a302771dd0b6621d410fcada671f61eeb/Images/Imagen28.png" width="350">

**Support Vector Machines**

Like logistic regression, Support vector machine (SVM) is another supervised learning model that can be uses to classify if a sample is categorized into one of two possibilities (win or lose).

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/2335a30a302771dd0b6621d410fcada671f61eeb/Images/Imagen29.png" width="350">

**Random Forest Classifier**

Applying a Random forest algorithm, we can rank the importance of input variables in order to remove some variables that could be affecting the model. 

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/2335a30a302771dd0b6621d410fcada671f61eeb/Images/Imagen30.png" width="350">

**Gradient Boosting Classifier**

Gradient boosting is a type of machine learning boosting. It relies on the intuition that the best possible next model, when combined with previous models, minimizes the overall prediction error. The key idea is to set the target outcomes for this next model in order to minimize the error.

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/2335a30a302771dd0b6621d410fcada671f61eeb/Images/Imagen31.png" width="350">

To compare the performance of all the models, a comparative table was created, it is observed that logistic regression model is the one that presents the highest precision and the highest result in the F1 Score.

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/2335a30a302771dd0b6621d410fcada671f61eeb/Images/Imagen32.png" width="450">

Because the results are low, it was decided to run a neural network model to evaluate every interaction within and across neurons. With two hidden layers we can get a Loss of 0.10 and an accuracy of 0.95.

In order to improve the model quality, the Random Forest Classifier and Gradient Boosting Classifier Regression models, both with the best F1-Score result were selected for adjustments. First calculating the feature importance in the Random Forest model 'rank_yrs_exp_driver' and 'constructor_failures_driver_constructor' the two variables with less importance were removed. Additionally, considering the imbalance in the classification modeling, the SMOTEENN technique is applied to oversample the minority class and subsampling the majority class in order to balance the data set.

<img src="https://github.com/SeRoGaTa/FinalProject_Team_8/blob/2335a30a302771dd0b6621d410fcada671f61eeb/Images/Imagen33.png" width="450">

For more details visit the [machine learning models description](machine_learning_model.md)

## Visual representation and dashboards
 
### Tableau

Tableau is a visual analytics platform transforming the way we use data to solve problems—empowering people and organizations to make the most of their data
Tableau is acknowledged as one of the leaders in industry to cover BI&A (Business Intelligence and Analytics) just behind Power BI as per Gartner 2021 magic quadrants for BI&A

![image](https://user-images.githubusercontent.com/90204875/155926860-8287bc8c-87cd-4f45-9061-8483528aa887.png)


The results and graphic representation of the project will be displayed in Tableau.
The objective of the project is to give an appropriate context of the sport through data before trying to predict the outcome of future races, so we will create and plot worksheets with relevant information to give the user a complete story and relevant data of the sport.

Some examples of the visual representation of context data from the sport are as follows:

![image](https://user-images.githubusercontent.com/90175232/157268328-45dbdf7c-f4dd-45a0-b899-d6dd221937a3.png)

![image](https://user-images.githubusercontent.com/90175232/157268437-9695faa0-f67d-449d-82e7-0af97315260d.png)





A visual representation of the models created is as follows:

![image](https://user-images.githubusercontent.com/90175232/157268724-5baade7a-5e32-49df-9194-7d0d25ab2f39.png)

![image](https://user-images.githubusercontent.com/90175232/157268801-31058847-16ea-4bf8-af69-cd4ae7d54cad.png)

![image](https://user-images.githubusercontent.com/90175232/157268898-a310e045-562e-4e90-b460-8f5bf690f99d.png)


### Presentation

A link to the presentation to the summary of this project is the following:

https://docs.google.com/presentation/d/1Qmr-si_AAy_0k_wWwyQI-lI4nOjMow6y7V-ttSQJkt0/edit#slide=id.p

https://public.tableau.com/app/profile/raciel3899/viz/FINALPROJECT8/F1PROJECT?publish=yes

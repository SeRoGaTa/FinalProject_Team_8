# FinalProject_Team_8
Repositorio para proyecto final

=======

# Formula 1 history through data analysis

The selected topic for our project is "Formula 1 history throughugh data abalysis", we seleceted this topic because of all the available and verifyable information available, the diverse variables that determine the outcome of this sport and twy to solve through data, the main questions all F1 fans have asqued themselves at some point. What provides the best leverage in the sport, the man, the machine or the strategy?

### Dataset 

We looked for information that can be usable for this purposes, the characteristics of the data that we could use for the purposes of our project are the following:

* Should be accurate.
* Should be verifyable.
* Should be diverse enough to perform our analysis.

We found a group of datasets that could be useful for our pusposes on the following link:

https://www.kaggle.com/williamhaworth/formula-1-kaggle-learning/data

In the link mentioned above, we found datasets related to Formula 1 racing from the year 1950 to 2021, the datasets that we will use are formatted in csv and contain information about:

circuits.csv
constructor_results.csv
constructor_standings.csv
constructors.csv
driver_standings.csv
drivers.csv
lap_times.csv
pit_stops.csv
qualifying.csv
races.csv
results.csv
seasons.csv
status.csv

## Questions to be answered

Ww will try to answer through data, questions that fans and analysts have asked about this sport since its very beginning, which is more important? The man, the machine or the strategy? we will leave budget ans sponsors out of the analysis this time.

Some of the questions we have initially designed with the available datasets are the following:

* How relevant is the driver vs the car to determine a championship output?
* How relevant is the pit stop average time to a championshio output?
* Which are the most relevant mechanical failures to determine a constructor, championship output?
* How relevant is the number of pole positions to the championship output?


## Machine learning models

After cleaning and grouping the relevant datasets, we will use a non supervised machine learning model to expose relevant correlations that are not evident, select the most meaningulf ones and then predict possibles outcomes through supervised machine learning.












1.- Quién puede ganar el proximo F1?


Posiciones
Eliminar puntos

Corredores

2. Es probable que el que sale en primer lugar termina en primer lugar

3. Tiempos de pits afectan el resultado final

4. Fallas mas cruciales en equipos de los últimos lugares

5. Constructores históricos por malos resultados

6. A los cuantos resultados negativos el constructor deja de participar


7. Tiempos de pits stops proporcionales a la posición en la carrera

8. Variables pits stops, tiempos de calificación

9. Factor mas determinante

10. Modelos de años anteriores, de años atrás 

11. Factores que han cambiado en la F1 

12. Standing de los corredores en la f2, en charting, indi

Si siempre estas en el numero uno en la f2 en la f1

### Que factor es mas importante en la carrera, el piloto o la constructora.

Cuales son los factores que tienen mas peso en el resultado de la carrera

Cuales son los factores que afectan el resultado de una carrera?
-   Tiempos de pits
-   Ganar calificación
-   Cantidad de campeonatos de constructora
-   Cantidad de fallas de constructora
-   An;os de experiencia del piloto
-   Mejores tiempos /lap times
-   Pista que se corre
-   Resultados previos de constructoras y pilotos

Cluster de factores de la escuderia y del piloto
main

sergio_gaytan - este es mi prueba de commit


--------------------------------------------------------
Proposal by Jorge

# Formula 1 Analysis

## Overview 
In this project, we are interested in identifying and determining the main factors that intervene in a race and what of those have an impact on the final result.

Formula 1 races have two fundamental elements that constantly interact, the drivers and the cars, which of these two factors is more relevant in the final result?

Factors like time in the pits, type of tracks, crucial faults, qualifying times affect the final result?

## Research question

Determining the factors that are most relevant to determining the winner of some race.
Some of the factor to considerer are:

-Pit times
-Earn rating
-Number of constructor championships
-Number of construction failures
-Years of pilot experience
-Best times / lap times
-Tracks
-Previous results of constructors and pilots

## Database Source
Formula 1 World Championship (1950 - 2021)

The dataset consists of all information on the Formula 1 races, drivers, constructors, qualifying, circuits, lap times, pit stops, championships from 1950 till the latest 2021 season.

URL: https://www.kaggle.com/rohanrao/formula-1-world-championship-1950-2020

## Communication protocols 

We decide to use direct messages for only team members in Slack and establish a daily meetup time for everyone on saturdays.

We use GitHub as a communication protocol by creating a personal branch for each member. Git allow us to save the progress of the proyect and keep the tracks of our work.

**Create a branch** 

Using branches let us work on our local repository to then update to the main branch and have the chance to review the branch or offer suggestions. In this space we can test modifications in the code without the problem of affecting the global code or the advances made

```ruby
git Branch -d nomeofbranch
```

**Open a pull request** 

After having tested our code locally, we proceed to perform a pull request to merge the code

```ruby
git status
git add .
git commmit -m "Commit message"
git push --set upstream origin <Branch-Name>
```

**Discuss and review**

At least one teammate has to review the pull request, if it is necesarry suggest changes and approve the changes to be merged

**Merge and deploy**

After approval, the member who pull the request can merge the changes into the main branch

## Week logs 

### Week 1

During the first week, all the members of the team investigated topics of interest that would help us to decide on a topic to work on. By vote the team decided on the topic, later we agreed on the research question.

The team decided that each member of the team review the databases to become familiar with the data and meet over the weekend to determine which databases to use, if any transformations or joins are needed, and define the model to use.

## Team members
-Ricardo Barba @
-Sergio Gaytan @
-Jorge Ponce @
-Raciel Tavitas @

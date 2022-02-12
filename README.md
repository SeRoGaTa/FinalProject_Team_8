## F1, which factor is the determinant to get a F1 winner?

The F1 topic was selected because the interest and knowledge that each member of the team has in the topic. 

F1 is a racing competition that has an incredible history through all this years, being the 50’s when all this started. 

The F1 has a lot of data and statistics that are used to get more information about how to improve the performance in every race.


### Source of data

Our source of data is a F1 database with information from the years 1950 to 2021.

This data has information regarding the drivers, races, circuits, lap times, pit stops, championships and constructors.


### Question to resolve

Discussing about the topic we came to a question that any of us were able to give a concrete answer.

- Which factor is the determinant to get a F1 winner?

For us to get to the answer we are going to analyzed the data regarding some important racing factors.

- Pits times
- Qualification
- Wins per constructor
- Wins per pilot
- Lap times
- Circuits characteristics
- Race results


### Database integration

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

Table 1.- Circuits

Circuit reference, name, location, country, lat & long, alt

Table 2.- Constructor results

Raceid, constructor id, points, status

Table 3.- Constructor standings

Raceid, constructor id, points, position, positionText, wins

Table4.- Constructors

Constructor id, constructor ref, name, nationality

Table 5.- Driver standings

Raceid, driverid, points, position, positionText, wins

Table 6.- Drivers

Driverid, driver ref, number, code, forename, surname, dob, nationality

Table 7.- Lap Times

Raceid, driverid, lap, postion, time, milliseconds

Table 8.- Pit stops

Raceid, driverid, stop, lap, time, duration, milliseconds

Table 9.- Qualifying

Qualifyid, raceid, driverid, constructorid, number, position, q1, q2, q3

Table 10.- Races

Raceid, year, round, circuitid, name, date, time

Table 11.- Results

Resultid, raceid, driverid, constructorid, number, grid, position, positionText, points, laps, time, rank, statusid

Table 12.- Seasons

Years

Table13.- Status

Statusid, status

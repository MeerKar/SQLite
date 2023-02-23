# SQLite

# Background

 In this project as a part of a  trip planning to Honalulu Hawaii,  climate analysis about the area has been done using the various steps . 
 For doing this a Python Pandas file has been created and link is  https://github.com/MeerKar/SQLite/blob/main/climate_starter.ipynb 
 These tasks has been divided into two parts.

# Part 1: Analyze and Explore the Climate Data


In this section,  Python and SQLAlchemy to do a basic climate analysis and data exploration of your climate database. 
Specifically,  SQLAlchemy ORM queries, Pandas, and Matplotlib. To do so, complete the following steps:

By  using the provided files (climate_starter.ipynb and hawaii.sqlite)  climate analysis and data exploration has completed.

SQLAlchemy create_engine() function is used  to connect to your SQLite database.

SQLAlchemy automap_base() function is used to reflect your tables into classes, and then saved references to the classes named station and measurement.

Then  Python to link the database by creating a SQLAlchemy session.

A precipitation analysis and then a station analysis is performed by completing the steps in the following two subsections.

# Precipitation Analysis

The most recent date in the dataset is found.

Using that date,  the previous 12 months of precipitation data by querying the previous 12 months of data has been calculated.

BY selecting only the "date" and "prcp" values,the query results into a Pandas DataFrame, and set the index to the "date" column.

Then sorted the DataFrame values by "date".

Then ploted the results by using the DataFrame plot method, as the following image shows:

<img width="983" alt="image" src="https://user-images.githubusercontent.com/116701851/220811822-9545333f-1591-4687-8ff0-e327a791e65a.png">



# Station Analysis


For the station analysis  a query is designed to calculate the total number of stations in the dataset.

And  a query is designed  to find the most-active stations (that is, the stations that have the most rows). To do so, complete the following steps:

.  List the stations and observation counts in descending order.

.  Answer the following question: which station id has the greatest number of observations?

A query that calculates the lowest, highest, and average temperatures that filters on the most-active station id found in the previous query.

 A query to get the previous 12 months of temperature observation (TOBS) data. To do so, complete the following steps:

.  Filter by the station that has the greatest number of observations.

.  Query the previous 12 months of TOBS data for that station.

 Plotted the results as a histogram with bins=12, as the following image shows:
 
 <img width="707" alt="image" src="https://user-images.githubusercontent.com/116701851/220812501-89a0efb5-2842-43ea-858c-e1a71a67599b.png">
 
 # Part 2: Design Climate App
 
 
Now that completed the initial analysis, a Flask APIis designed  based on the queries that  just developed. 
To do so, Flask is used to create  routes as follows:

/

Start at the homepage.

List all the available routes.

/api/v1.0/precipitation

Convert the query results from the precipitation analysis (i.e. retrieve only the last 12 months of data) to a dictionary using date as the key and prcp as the value.

Return the JSON representation of the dictionary.

/api/v1.0/stations

Return a JSON list of stations from the dataset.
/api/v1.0/tobs

Query the dates and temperature observations of the most-active station for the previous year of data.

Return a JSON list of temperature observations for the previous year.

/api/v1.0/<start> and /api/v1.0/<start>/<end>

Return a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start or start-end range.

For a specified start, calculate TMIN, TAVG, and TMAX for all the dates greater than or equal to the start date.

For a specified start date and end date, calculate TMIN, TAVG, and TMAX for the dates from the start date to the end date, inclusive.















# sqlalchemy-challenge

### Vacation Climate Analysis in Honolulu, Hawaii

This repository contains the necessary files and instructions for performing a climate analysis and creating a Flask API for vacation planning in Honolulu, Hawaii. Follow the steps below to complete the analysis and design your API.

### Part 1: Analyze and Explore the Climate Data

Connect to the SQLite database using SQLAlchemy create_engine() function.

Reflect the tables into classes using SQLAlchemy automap_base() function. Save references to the classes named station and measurement.

Create a SQLAlchemy session to link Python to the database.


Perform a precipitation analysis:

Find the most recent date in the dataset.

Get the previous 12 months of precipitation data based on the most recent date.

Load the query results into a Pandas DataFrame and sort by date.

Plot the precipitation data using the DataFrame plot method.

Print the summary statistics for the precipitation data.

Perform a station analysis:

Calculate the total number of stations in the dataset.

Find the most-active stations and their observation counts.

Calculate the lowest, highest, and average temperatures for the most-active station.

Query the previous 12 months of temperature observation (TOBS) data for the most-active station.

Plot the TOBS data as a histogram with bins=12.

### Part 2: Design Your Climate App
Design a Flask API with the following routes:
/: Homepage that lists all the available routes.
/api/v1.0/precipitation: Convert the query results from the precipitation analysis to a dictionary and return the JSON representation.
/api/v1.0/stations: Return a JSON list of stations from the dataset.
/api/v1.0/tobs: Query the temperature observations of the most-active station for the previous year of data and return a JSON list.
/api/v1.0/<start> and /api/v1.0/<start>/<end>: Return a JSON list of the minimum, average, and maximum temperatures for a specified start or start-end range.

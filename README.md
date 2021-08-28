### Climate Analysis and Exploration
Used Python and SQLAlchemy to do basic climate analysis and data exploration of a climate database. The analysis has been completed using SQLAlchemy ORM queries, Pandas, and Matplotlib.

* Used [starter notebook](climate_starter.ipynb) and [hawaii.sqlite](Resources/hawaii.sqlite) to complete climate analysis and data exploration.

* Used SQLAlchemy `create_engine` to connect to sqlite database.

* Used SQLAlchemy `automap_base()` to reflect tables into classes and save a reference to those classes called `Station` and `Measurement`.

* Linked Python to the database by creating an SQLAlchemy session.

### Precipitation Analysis

* Started by finding the most recent date in the data set.

* Using this date, I retrieved the last 12 months of precipitation data by querying the 12 preceding months of data. *

* Selected only the `date` and `prcp` values.

* Loaded the query results into a Pandas DataFrame and set the index to the date column.

* Sorted the DataFrame values by `date`.

* Plotted the results using the DataFrame `plot` method.

 <img width="468" alt="precipitation" src="https://user-images.githubusercontent.com/80393628/131209215-1c4f11b8-9d70-47ef-883c-25e456390950.png">

* Used Pandas to print the summary statistics for the precipitation data.

### Station Analysis

* Designed a query to calculate the total number of stations in the dataset.

* Designed a query to find the most active stations (i.e. which stations have the most rows).

  * Listed the stations and observation counts in descending order.

  * Used the most active station id to calculate the lowest, highest, and average temperature.

* Designed a query to retrieve the last 12 months of temperature observation data (TOBS).

  * Filtered by the station with the highest number of observations.

  * Querried the last 12 months of temperature observation data for this station.

  * Plotted the results as a histogram with `bins=12`.

    <img width="478" alt="station-histogram" src="https://user-images.githubusercontent.com/80393628/131209213-a448aceb-686d-40a7-a002-3c7a5c3ff354.png">

### Climate App

* Designed a Flask API based on the queries that I had developed.

* Used Flask to create routes.

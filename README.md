# Data Modeling with Postgres
*Project and Info courtesy - Udacity*

## Project Description
A startup called **Sparkify** wants to analyze data on songs and user activity on their new music streaming app. The data resides in a directory of JSON logs. We will define fact and dimension tables for a star schema for a particular analytic focus. Then write an ETL pipeline that transfers data from files in two local directories into these tables in Psotgres.

#### Tools used for the task:
- Python
- SQL

## Data Schema
#### Fact Table
`songplays` - records in log data associated with song plays i.e. records with page **NextSong**
- songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

#### Dimension Tables
`users` - users in the app
- user_id, first_name, last_name, gender, level

`songs` - songs in the music database
- song_id, title, artist_id, year, duration

`artists` - artists in music database
- artist_id, name, location, latitude, longitude

`time` - timestamps of records in **songplays** broken down into specific units
- start_time, hour, day, week, month, year, weekday

## Project Template
The project workspace contains six files for template:

1. `test.ipynb` - displays the first few rows of each table to let you check the database.
2. `create_tables.py` - drops and creates the tables. This file could be run to reset the tables before each time the ETL scripts are run.
3. `etl.ipynb` - reads and processes a single file from **song_data** and **log_data** and loads the data into the tables. This notebook contains detailed instructions on the ETL process for each of the tables.
4. `etl.py` - eads and processes files from **song_data** and **log_data** and loads them into the tables. This could be filled out based on the work in the ETL notebook.
5. `sql_queries.py` - contains all the sql queries, and is imported into the last three files above.
6. `README.md` - provides discussion on the project.

## How to run
1. Run `create_tables.py` in terminal to create the databases and tables.
2. Run `etl.py` to load, extract and insert the data from the queries used in `create_tables.py`.
3. Run `test.ipynb` to confirm whatever commands are being run.

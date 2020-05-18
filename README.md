<p>Sparkify is a startup that wants to analyze their song and user activity data. Their main interest is to understand which songs users are listening to. Hence, the main goal of this project is to create a database for their analytics team to understand the relationships with the easist way. </p>

<p>Star schema is used for the database schema design and. 1 fact and 4 dimension tables are created. ETL pipeline transfers the data from files in two local directories into these table using Python and SQL.<p>

*The tables are like this:*

### Fact Table
    
songplays - records in log data associated with song plays i.e. records with page NextSong
songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

### Dimension Tables
users - users in the app
user_id, first_name, last_name, gender, level

songs - songs in music database
song_id, title, artist_id, year, duration

artists - artists in music database
artist_id, name, location, latitude, longitude

time - timestamps of records in songplays broken down into specific units
start_time, hour, day, week, month, year, weekday


*The files in the repository are like this:*

test.ipynb displays the first few rows of each table to let you check your database.
create_tables.py drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts. To run this file, at the command prompt, type `python create_tables.py`.
etl.ipynb reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables. 
etl.py reads and processes files from song_data and log_data and loads them into your tables. To run this file, at the command prompt, type `python etl.py`.
sql_queries.py contains all your sql queries, and is imported into the last three files above.



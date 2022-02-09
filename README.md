# Summary
Create an ETL pipeline that takes JSON data on disk and creates a star schema in a PostgreSQL database that is optimized for queries on song play analysis.
## Sources
1. log_data
2. song_data
## Data Model
A star schema model optimized for queries on song play analysis
### Fact table:
##### **songplays**
- songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent
### Dimension tables:
##### **users**
- user_id, first_name, last_name, gender, level
##### **songs**
- song_id, title, artist_id, year, duration
##### **artists**
- artist_id, name, location, latitude, longitude
##### **time**
- time_id, start_time, hour, day, week, month, year, weekday

# Files
## ETL Pipeline
- **create_tables.py** drops and creates your tables. Run before etl.py
- **etl.py** reads and processes files from song_data and log_data and loads them into your tables
- **sql_queries.py** contains all the sql queries
## Test, Debug, and Analyze
- **test.ipynb** displays the first few rows of each table to let you check your database.
- **etl.ipynb** reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables.
- **analysis.ipynb** visualizes data in notebook form

# Run
To run enter:
 python create_tables.py
 python etl.py

You can test the resulting database with **test.ipynb** and debug the ETL pipeline with **etl.pynb**.

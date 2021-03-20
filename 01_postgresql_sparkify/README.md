# Document Process

## Discuss the purpose of this database in the context of the startup, Sparkify, and their analytical goals.

 The purpose of this database is to enable Sparkifty and their analytics team to
    
   1. Develop a better understanding for their user behavior in various dimensions such as user, song, artist, and geo-location. Sparkify team can develop a customer segmentation based on the provided database.
   2. Sparkift can develop a propensity to subscribe model to identify who will likely to convert from free to paid level given the transaction timestamp as well as the date that customer convert from the free to paid level.
   3. The customer insight dashboard can be built upon the provided data. The example of metric is daily average number of user in the Sparkify platform. 
        
## State and justify your database schema design and ETL pipeline.

The provided database consists of 1 fact table and 4 dimension tables as following.
Schema design concept - **STAR Schema**

### Fact Table
**songplays** - records in log data associated with song plays i.e. records with page NextSong
Columns  - `songplay_id`, `start_time`, `user_id`, `level, song_id`, `artist_id`, `session_id`, `location`, `user_agent`

### Dimension Tables
**users** - users in the app
Columns  - `user_id`, `first_name`, `last_name`, `gender`, `level`
**songs** - songs in music database
Columns  - `song_id`, `title`, `artist_id`, `year`, `duration`
**artists** - artists in music database
Columns  - `artist_id`, `name`, `location`, `latitude`, `longitude`
**time** - timestamps of records in songplays broken down into specific units
Columns  - `start_time`, `hour`, `day`, `week`, `month`, `year`, `weekday`

### ER Diagram
<iframe width="560" height="315" src='https://dbdiagram.io/embed/6055d53decb54e10c33c61c9'> </iframe>
 
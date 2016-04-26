# postgresqldatabase_maptables
This is a PostgreSQL database dump of the spatial (map) tables used by Tripodmaps Chui edition


Restoring Map tables in PostgreSQL
------------
These tables contain spatial information /maps of Kenya
1. Using pgAdmin III,  <b>Left click</b> on the pre-installed  <b>postgres database</b> and select it

2.Click on the  <b>SQL</b> button at the top. The  <b>Query</b> window appears

3. Type the following
CREATE EXTENSION postgis;
CREATE EXTENSION postgis_topology;

4. Click  <b>Run</b> (The green play button). Clost the  Query window

5.  <b>Right click</b> on the  <b>postgres</b> database and select  <b>Restore</b>

6. Navigate to the location where you downloaded the file with the link below

https://dl.dropboxusercontent.com/u/313489686/Postgresql/postgres95_postgresmaptables_db_rolenamepostgres.backup


8. Select <b>postgres</b> from the <b>role name</b> list

9. Click  <b>OK</b> to restore the database

# postgresqldatabase_maptables
This is a PostgreSQL database dump of the spatial (map) tables used by Tripodmaps Chui edition

Extracting the files
-----------

Use <b>7zip</b> to Extract the files. Start with the file ending with <b>.001</b>



Restoring Map tables in PostgreSQL
------------

1. Using pgAdmin III,  <b>Left click</b> on the pre-installed  <b>postgres database</b> and select it

2. Click on the  <b>SQL</b> button at the top. The  <b>Query</b> window appears

3. Type the following<br>
CREATE EXTENSION postgis;<br>
CREATE EXTENSION postgis_topology;<br>

4. Click  <b>Run</b> (The green play button). Clost the  Query window

5. <b>Right click</b> on the  <b>postgres</b> database and select  <b>Restore</b>

6. Navigate to the location where you downloaded the files

7. In pgAdmin III, select <b>postgres</b> from the <b>role name</b> list

8. Click on <b>OK</b> to restore the database



Other sources of this file
-----------
This file is also available on DropBox via the link below.

https://dl.dropboxusercontent.com/u/313489686/Postgresql/postgres95_postgresmaptables_db_rolenamepostgres.backup



Using certificates
------------
REF: http://ubuntuforums.org/showthread.php?t=735020

It is important to include SSL verification early on in your system. The instructions below will help you with setting up Postgresql servers with SSL. This certificate(s) can also be used by your software applications as well.

    openssl req -new -text -out server.req
    openssl rsa -in privkey.pem -out server.key
    rm privkey.pem
    openssl req -x509 -in server.req -text -key server.key -out server.crt
    chmod og-rwx server.key
    chown postgres : postgres server.key

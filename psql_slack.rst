Como configurar Flicket-PostgreSQL en Slackware
=======

Creando la base de datos
-------------
1. # su postgres
2. createuser -P -e flicket
3. Configurar el conector psycopg2==2.8.6 en los requirements.txt, comentando pymysql  
4. Ejecutar python -m scripts.create_json colocando las config de la base de datos
   el puerto 5432, en localhost
5. Crea la base de datos en postgres
   createdb "nombre_db" --owner "usuario_en_flicket"
6. Probamos que todo halla quedado bien ingresando con nuestro usuario a la base
   de datos
   psql -U "usuario_en_flicket" "nombre_db"

Can I See It Working?
---------------------
I have a working version at: https://flicket.evereux.uk/. If you'd like access
drop an email to me at evereux@gmail.com. Tell me username / email you would
like to use. Currently, all the views require login so I'll have to create an 
account for you.

Alternatively, see the screenshots that can be found in the documentation link.


Upgrading From Earlier Versions
-------------------------------

See the changelog for changes and additional steps to take when upgrading.


Requirements
------------
Prior to installing and running Flicket please read these requirements.

* Python =>3.6

* SQL Database server with JSON support (for example PostgreSQL >=9.2,
  MySQL >=5.7, MariaDB >=10.2, SQLite >=3.9)

* PostgreSQL see psql_slack.rst

Production Environment
----------------------

To serve Flicket within a production environment webservers such as Apache
or nginx are typically used. See the documentation for how to install Apache
on Windows.

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

Salida con problemas
python manage.py db upgrade


# dockerizeSpringBoot
# Composición de docker para desplegar un entorno que consiste en:
   - Frontend de Angular   
   - Backend de Sepringboot   
   - Base de datos MySQL   
   - Gestores de base de datos: Adminer y phpMyAdmin   
# Ubicación código ya compilado
 initialfe: Carpeta que incluye código de prueba de Angular. (Sustituye por tu propio código)   
 initialbe: Carpeta que incluye código de prueba de Sprngboot y fichero de inicialización de la base de datos (Sustituye por tu propio código)   
#
 Para poner en marcha el ejemplo modificar en env-example la variable basepath   
 Para poner en marcha tu propio código incluye tu código en las carpetas correspondientes y ajusta los valores en env-example
# 

# Los comandos que se realizan a continuación se ejecutan desde este directorio.

Puesta en marcha   
docker compose --env-file env-example up -d   

Posibilidad de hacer un mysql -u root -p < backup.sql   
docker-compose exec mysql mysqldump --user=root --password=password myapp01 > dump_file_20221119.sql   

docker-compose exec mysql mysql --host=localhost --user=root --password=password myapp01 < dump_file_20221119.sql   


# ADVERTENCIA: Cuando realices cambios es importante que hagas una limpieza del entorno para que tengan efecto:

 Limpieza del entorno para empezar de cero   
 Eliminar los contenedores que se arrancaron y estan parados   
    docker container prune # Decir yes para borrar todos los contenedores parados   
 Eliminar las imágenes creadas:   
    docker image rm example/proxy   
    docker image rm example/java   
 Eliminar volumen de la base de datos que se ha creado   
    docker volume rm [dockerizeSpringBoot]_mysql_data   
   
 Para más información lee el fichero info.txt  
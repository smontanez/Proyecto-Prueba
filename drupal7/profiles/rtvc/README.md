ProfileRTVC
===========

Prueba Profile RTVC
# Drupal 7 Perfil de instalacion para rtvc radio #

Perfil de instalacion Drupal7 para rtvc radio

## Requerimientos ##

* Una maquina con **Apache**, **MySQL**, **git** and **drush** se ha instalado.
* Una base de datos MySQL se ha creado para Drupal, con un usuario con todos los permisos a esta.

## Instalacion ##

Copiar el archivo **build-rtvc.make** a su directorio home

Ejecutar en la línea de comandos:
 
  drush make build-rtvc.make /var/www/rtvc
  
  cd /var/www/rtvc
  
  drush site-install rtvc --db-url=mysql://<database_user>:<database-user-password>@<database host>/<database name> 




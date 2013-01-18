ProfileRTVC
===========

Prueba Profile RTVC
# Drupal 7 Perfil de instalacion para rtvc radio #

Perfil de instalacion Drupal7 para rtvc radio

#Opción 1#
## Requerimientos ##

* Una maquina Linux con **Apache**, **MySQL**, **git** y **drush** instalada.
* Crear una base de datos MySQL para Drupal, con un usuario con todos los permisos a esta.

##Pasos para la Instalación drush en Linux:##

Prerrequisitos: 

Ejecutar en el home los siguientes comandos:

pear config-create ${HOME} ${HOME}/.pearrc

pear install -o PEAR

Abrir el .bash_profile y editarlo con vi:

vi .bash_profile

y adicionar las siguientes dos líneas:

export PHP_PEAR_PHP_BIN=/usr/php/53/usr/bin/php

export PATH=${HOME}/pear:/usr/php/53/usr/bin/php:${PATH}

Correr el siguiente comando:

pear channel-discover pear.drush.org

pear install drush/drush


# Instalacion Profile#

Copiar el archivo **build-rtvc.make** a su directorio home

Ejecutar:
 
  drush make build-rtvc.make /var/www/rtvc
  
  cd /var/www/rtvc
  
  drush site-install rtvc --db-url=mysql://<database_user>:<database-user-password>@<database host>/<database name>

#Opción 2#
## Requerimientos ##

* Una maquina Windows con **Apache**, **MySQL** y **git** instalada.
* Crear una base de datos MySQL para Drupal, con un usuario con todos los permisos a esta.

## Instalacion ##

Instalar drupal siguiente las instrucciones de http://drupal.org/documentation/install/windows

Instalar la versión del core de drupal que se encuentra en el archivo: build-rtvc.make disponible en este repositorio.

Instalar los módulos y versiones que se encuentran en el archivo rtvc.make disponible en este repositorio a la anterior instalación del core de drupal. 

#Opción 3#
## Requerimientos ##

* Una maquina Windows con **Apache**, **MySQL** y **git** instalada.
* Crear una base de datos MySQL para Drupal, con un usuario con todos los permisos a esta.
* Descargar en su home el profile comprimido llamado drupal7_profile.tar.gz que se encuentra en este repositorio.
* Cambiar el archivo settings.php para que se conecte a la Base de datos que acaba de crear.
* Probar en el navegador la instalación.

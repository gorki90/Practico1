# Dockerfile para PARCIAL DEAW
# A partir de la imagen de Ubuntu 18.04
FROM ubuntu:18.04

# Responsable del fichero
LABEL \
	version="1.0" \
	description="Parcial - PRACTICO 1" \
	creationDate="Gorruiz@birt.eus 29/01/2024"

# Ejecutamos comandos
RUN \
	apt-get update \ 
    && apt-get install apache2 --yes \
	&& apt-get install nano  \
	&& mkdir /var/www/html/privado

# Copiamos ficheros necesarios
COPY html/index.html /var/www/html/
COPY html/css_parcial/ /var/www/html/


COPY html/privado.html /var/www/html/privado
COPY html/css_privado/ var/www/html/privado

COPY conf/000-default.conf /etc/apache2/sites-enabled
COPY conf/passwd etc/apache2/passwd

# Exponemos puertos
EXPOSE \
 80:80 443:443

### Crea un contenedor con las siguientes especificaciones: 

### a. Utilizar la imagen base NGINX haciendo uso de la versión 1.19.3
### b. Al acceder a la URL localhost:8080/index.html aparecerá el mensaje HOMEWORK 1
### c. Persistir el fichero index.html en un volumen llamado static_content

-------

## Solución

1. **Se crea un contenedor** y se descarga la imagen de ngnix con la version 1.19.3 escuchando en el puerto 8080 con el siguiente comando:

`docker create --name hw-1 -p 8080:80 nginx:1.19.3`

Con esto hemos creado el contenedor como tal que contiene una imagen con base de nginx, sin embargo, todavia no la podemos visualizar hasta que sea construida y encendida por el engine de docker, lo cual se hace en los siguientes pasos.

2. Se realiza el **build del contenedor** el cual se define por el Dockerfile, esto con el siguiente comando:

`docker build . -t hw-1`

En el Dockerfile se le dio la instruccion de crear un folder en nginx donde se coloca el index html, posteriormente, se copio el html personalizado *(index.html)* a la carpeta creada en ngnix para la personalizacion de la apgina de inicio.

3. Se **corre el contenedor** adjuntando el html personalizado como un volumen con el siguiente comando

`docker run -it --rm -p 8080:80 -v static_content:/usr/share/nginx/html hw-1`

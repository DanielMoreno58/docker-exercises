### Crea una imagen docker a partir de un Dockerfile. Esta aplicación expondrá un servicio en el puerto 8080 y se deberá hacer uso de la instrucción HEALTHCHECK para comprobar si la aplicación está ofreciendo el servicio o por si el contrario existe un problema.

## Solución

1. **Se crea un contenedor y se realiza el buid** con la imagen de ngnix con la version 1.19.3 con el siguiente comando mediante el Dockerfile:

`docker build . -t go-healtcheck`

2. Se **corre el contenedor** para inicializarlo con el puerto 8080

`docker run -it -p 8080:80 -v static_content:/usr/share/nginx/html go-healtcheck`

3. Se teclea Control C para salir del proceso

4. Se busca el contenedor mediante el siguiente comando:

`docker ps -a`

5. Se da start con el siguiente comando:

`docker start <container_name>`

6. Para visualizar el health check revisamos el estado con el siguiente comando:

`docker ps`
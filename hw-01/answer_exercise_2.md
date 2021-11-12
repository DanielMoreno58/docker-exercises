### Indica la diferencia entre el uso de la instrucción ADD y COPY (Dockerfile)

La diferencia es que en el ADD puedes descargar ficheros y agregarlos mediante URLs en una imagen docker, así como también puedes obtener un fichero tar. 

Esto antes mencionado no lo puede hacer el COPY, ya que solo se limita a copiar un archivo local en una imagen docker.
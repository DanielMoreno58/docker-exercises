### Indica la diferencia entre el uso de la instrucción CMD y ENTRYPOINT (Dockerfile)

La diferencia es que el Entrypoint indica el punto de entrada que usara el CMD para ejecutar la instruccion que esta en CMD, por defecto es */bin/sh -c*, por lo que si no le das un Entrypoint usara ese.

El comando CMD ejecutara los comandos que se ingresen con base a la informacion del Entrypoint
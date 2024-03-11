# Práctica Docker
	

> Por Federico López Pérez
## Fichero docker-compose con los servicios Drupal y MySQL

Para la configuración de este fichero utilizamos dos servicios, el primero siendo Drupal, que tomará la última imagen de drupal que encuentre en docker hub, mapeara el puerto 80 del contenedor al 81 del equipo local para poder acceder a través de él a la web de Drupal, establecemos su dependencia del servicio de mysql, para no tener posibles problemas de que no encuentre la base de datos, en el entorno le damos los datos de la base de datos y por último establecemos el volumen que va a utilizar.

El segundo servicio será el de mysql, cuya configuración es idéntica, pero nos saltamos el mapeo de puerto, puesto que no lo necesitamos.

Por último, le decimos los dos volúmenes que utilizaremos.

## Fichero docker-compose con los servicios WordPress y MariaDB

En este fichero utilizaremos también dos servicios, el primero el de WordPress, cuya configuración es idéntica a la de Drupal, excepto que cambiamos el puerto 81 por el 82, lo conectamos a la red redDocker y quitamos la dependencia, ya que no la necesitamos por que conectaremos ambos contenedores a la misma red, y el volumen, porque no nos lo han pedido.

Para el servicio de MariaDB, hacemos exactamente lo mismo que para el de WordPress pero quitando el puerto que, de nuevo, no lo necesitamos.

Por último, establecemos la red a usar: redDocker.

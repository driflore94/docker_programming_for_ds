# Tarea Docker Compose

**Objetivo**: Especificar y levantar una infraestructura usando `docker compose`

En esta carpeta hay tres archivos:
* `generator.py`: Genera datos a partir de un algoritmo que se inicializa con una semilla (usa tu clave única!). Estos datos son mandados a una cola de RabbitMQ
* `consumer.py`: Este script consume la cola de rabbit e inserta estos datos a una base de datos de PostgreSQL
* `analysis.ipynb`: Por último, este _notebook_ utiliza los datos cargados a Postgres para hacer un pequeño análisis. Este es el único archivo que puedes modificar.

Necesitarás especificar un archivo `docker-compose.yaml` que incluya todos los elementos necesarios para llegar a la parte de análisis. En la libreta hay un ejemplo
de cómo se verá esto al final. Puedes usar tantos Dockerfile como sea necesario, pero configuración (variables de ambiente, argumentos default, etc) deberá ser especificado
en el YAML. 

Hints:
* Presta atención a las variables de ambientes y argumentos de línea de comando usados por los scripts
* Existen imágenes oficiales de `rabbitmq` y `postgres` en DockerHub. Úsalas
* Recuerda que puedes levantar servicios específicos con `docker-compose up` si necesitas experimentar con una de las imágenes
* No es necesario volverte experto en las herramientas, sólo entiende que está haciendo cada script (con los tutoriales básicos debe ser suficiente!)
* No es necesario dejar mucho tiempo levantada la infraestructura, es suficiente con que llegues al punto donde el coeficiente de x en las regresiones del _notebook_ se
parece al generado por el script `generator.py`

Tienes hasta el **jueves 30 de noviembre a las 11:59** para entregar esta tarea. Recuerda los criterios de evaluación y calificación.

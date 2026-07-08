¿Qué es Apache Spark Distribuido?

Apache Spark es un motor de procesamiento de datos de código abierto diseñado para trabajar con grandes volúmenes de información de manera rápida y eficiente. A diferencia de un procesamiento tradicional donde todos los datos son manejados por un solo equipo, Spark permite distribuir las tareas de procesamiento entre varios equipos conectados formando un clúster.

Un entorno de Spark distribuido está compuesto principalmente por un nodo coordinador o Master, encargado de administrar los recursos y asignar tareas, y varios nodos de procesamiento llamados Workers, que ejecutan las operaciones asignadas sobre los datos.

Esta arquitectura permite aprovechar la capacidad de múltiples dispositivos para realizar cálculos de forma paralela, reduciendo el tiempo de procesamiento y facilitando el análisis de grandes conjuntos de datos.

Arquitectura básica de Spark Distribuido

El objetivo de este laboratorio es implementar una arquitectura similar a la siguiente:

                    +----------------------+
                    |       Zeppelin       |
                    |                      |
                    +----------+-----------+
                               |
                               |
                               v
                    +----------------------+
                    |    Nodo Master      |
                    | Gestión del clúster |
                    | Asignación de tareas |
                    +----------+-----------+
                               |
              +----------------+----------------+
              |                |                |
              v                v                v
     +---------------+ +---------------+ +---------------+
     |   Worker 1    | |   Worker 2    | |   Worker 3    |
     | Procesamiento | | Procesamiento | | Procesamiento |
     |    de datos   | |    de datos   | |    de datos   |
     +---------------+ +---------------+ +---------------+

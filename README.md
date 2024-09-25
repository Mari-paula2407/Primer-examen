# Primer-examen
Pregunta 1
1. Por qué es necesario hacer resize del vector cuando este se llena y es necesario seguir almacenando elementos?. A caso no sería una mejor opción apartar un espacio en memoria para seguir almacenando los elementos que se van a insertar en el futuro así se deba llevar registro dentro de la clase de que los elementos del vector pueden estar almacenados en diferentes lugares de la memoria?

R\\No es mejor dado que una de las ventajas de utilizar vectores es el echo de que permite de manera eficiente acceder a los elementos al ser almacenados de manera continua, dicho esto si en ves de resize (redimensionarlo) lo dividimos en diferentes espacios de memorias el vector dejaria de ser tan eficiente, siendo asi que seria similar a como trabaja una lista enlazada.

Además, tener que llevar un registro de las ubicaciones separadas de los elementos introduciría una complejidad adicional en la implementación del vector, lo cual afectaría su rendimiento en varias operaciones.

2. Si comparamos el vector con una lista enlazada como la implementada en el curso creeusted que la lista pueda ser más eficiente?. Justifique su respuesta.

R\\Depende de la necesidad, pues si necesitamos almacenar mucha informacion sin un acceso claro o aleatorio de manera rapida y con informacion en movimiento, es mejor la lista enlazada, por el contrario si lo que se necesita es informacion con un facil y rapido acceso de manera aleatoria o sin muchos cambios en la informacion almacenada el vector es el mejor.

Pregunta 2
1. Para cada uno de los vectores especifique cuál es su capacidad final y el desperdicio en el que incurre.

R\\ 
Vector x:
Capacidad inicial: 5 elementos
Política de crecimiento: 2.0 (duplicación de la capacidad cada vez que se redimensiona) Hasta llegar a 10000.
La capacidad inicial de x es de 5 cuando se añaden 6 elementos la capacidad se duplica a 10 y así sucesivamente, hasta que se alcance al menos 10,000 elementos.
Por consiguiente el proceso es:
- 5 → 10 → 20 → 40 → 80 → 160 → 320 → 640 → 1280 → 2560 → 5120 → 10240.
  Vector x: Capacidad final = 10,240, Desperdicio = 240 elementos

Vector y:
Capacidad inicial:10 elementos
Política de crecimiento:1.8 (incrementa su capacidad por un factor de 1.8 cada vez que se redimensiona) Hasta llegar a 10000
La capacidad inicial de y es 10.
Cuando se añaden 11 elementos, la capacidad se multiplica por 1.8: 10*1.8 = 18, para 19 elementos, la capacidad se vuelve: 18*1.8=32.4 → 32, y así sucesivamente, hasta que se alcance al menos 10,000 elementos.
Por consiguiente el proceso es:
- 10 → 18 → 32 → 57 → 102 → 184 → 331 → 596 → 1072 → 1930 → 3474 → 6253 → 11255.
Vector y: Capacidad final = 11,255, Desperdicio = 1,255 elementos

Vector z:
Capacidad inicial:100 elementos
Política de crecimiento:2.0 (duplicación de la capacidad cada vez que se redimensiona)
La capacidad inicial de z es 100 después de añadir 101 elementos, la capacidad se duplica a 200, y así sucesivamente, hasta que se alcance al menos 10,000 elementos.
Por consiguiente el proceso es:
- 100 → 200 → 400 → 800 → 1600 → 3200 → 6400 → 12800.
Vector z: Capacidad final = 12,800, Desperdicio = 2,800 elementos

2. Cuál de los vectores resultó ser más eficiente a la hora de ejecutar el programa?
Justifique clara y concisamente su respuesta.

R\\Si bien pareciera que a simple vista el vector x es el mas eficiente pues es el que tiene menor desperdicio, es de echo el vector z el mas eficiente esto gracias a que tiene la misma politica de crecimiento que x, pero teniendo una mayor capacidad, lo que provoca una velocidad mayor en la maquina.

 Pregunta 3
1. Proponga una implementación en C++ de la clase AdjacencyList , defina apropiadamente sus atributos y sus operaciones. Usted puede utilizar para esto cualquiera de las estructuras de datos discutidas en clase.

R\\ 





























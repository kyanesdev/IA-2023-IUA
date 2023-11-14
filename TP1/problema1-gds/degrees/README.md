### Resolucion de problemas - Grado de separacion

El código proporcionado busca la ruta más corta entre dos personas en función de sus conexiones en películas compartidas. A continuación, se destacan las funciones principales:

- **`load_data(directory)`**: Lee información de archivos CSV y carga los datos en diccionarios en memoria para personas y películas.

- **`main()`**: Función principal que ejecuta el programa.
  - Carga los datos en memoria.
  - Solicita nombres de personas al usuario.
  - Busca el camino más corto entre las dos personas y muestra los resultados.

- **`shortest_path(source, target)`**: Encuentra la ruta más corta entre dos personas usando un algoritmo de búsqueda en grafos.
  - Utiliza una cola para explorar conexiones entre personas.
  - Devuelve la ruta más corta si existe o `None` si no hay conexión.

- **`person_id_for_name(name)`**: Obtiene el ID de una persona basado en su nombre, manejando posibles ambigüedades.

- **`neighbors_for_person(person_id)`**: Devuelve pares de (ID de película, ID de persona) para personas que han trabajado en películas con una persona dada.

El código demuestra un algoritmo de búsqueda de rutas cortas utilizando grafos para encontrar conexiones entre personas a través de películas compartidas.

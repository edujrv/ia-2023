# Degrees - Encontrar la conexión entre actores a través de películas

Este script en Python, `degrees.py`, permite encontrar la conexión más corta entre dos actores a través de las películas en las que han trabajado. Utiliza un algoritmo de búsqueda en anchura para encontrar el camino más corto entre dos actores dados.

## Requisitos

- Python 3.x

## Instalación

1. Clona o descarga el repositorio en tu máquina local.
2. Asegúrate de tener instalado Python 3.x.
3. Asegúrate de tener los archivos CSV con la información de las personas, películas y conexiones.

## Uso

1. Ejecuta el script proporcionando el directorio donde se encuentran los archivos CSV como argumento. Si no se proporciona ningún argumento, el script buscará en un directorio llamado `large` por defecto.

```
python degrees.py [directorio_de_datos] 
```

2. Sigue las instrucciones para introducir los nombres de los dos actores entre los que deseas encontrar la conexión.

## Estructura de Archivos
  `data/` Hace referencia al directorio donde se encuentran los .csv con la informacion necesaria. En este repo puede hacer referencia a `large/` o `small/`
- `data/people.csv`: Contiene información sobre personas como su ID, nombre y fecha de nacimiento.
- `data/movies.csv`: Contiene detalles de las películas, incluyendo su ID, título y año de lanzamiento.
- `data/stars.csv`: Relaciona las personas con las películas en las que han participado.

## Funcionalidades

- **`load_data`**: Carga la información de los archivos CSV en la memoria del programa.
- **`shortest_path`**: Encuentra el camino más corto entre dos actores usando películas como conexiones.
- **`person_id_for_name`**: Devuelve el ID IMDB de una persona a partir de su nombre, manejando ambigüedades si existen múltiples coincidencias.
- **`neighbors_for_person`**: Obtiene las películas y actores conectados a una persona dada.

## Archivo `util.py`

El archivo `util.py` contiene clases y métodos utilizados para la gestión de nodos y la implementación de la frontera para el algoritmo de búsqueda.

### Clase `Node`

- **`Node`**: Representa un nodo en el grafo de búsqueda.
  - **`state`**: Estado del nodo, en este caso, el ID de la persona o la película.
  - **`parent`**: Referencia al nodo padre.
  - **`action`**: Acción que lleva del nodo padre al nodo actual.

### Clase `StackFrontier` y `QueueFrontier`

- **`StackFrontier`**: Implementa una pila para la frontera de búsqueda.
  - **`add`**: Agrega un nodo a la pila.
  - **`contains_state`**: Verifica si la pila contiene un estado dado.
  - **`empty`**: Comprueba si la pila está vacía.
  - **`remove`**: Elimina y devuelve un nodo de la pila.

- **`QueueFrontier`**: Implementa una cola para la frontera de búsqueda, heredando de `StackFrontier`.
  - **`remove`**: Elimina y devuelve un nodo de la cola (siguiendo la lógica FIFO).

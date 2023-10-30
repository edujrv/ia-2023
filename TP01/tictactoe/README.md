# Juego del Ta-Te-Ti (Tic Tac Toe) con Pygame

Este es un juego del Ta-Te-Ti (Tic Tac Toe) interactivo implementado en Python con la biblioteca Pygame. El proyecto consta de varios archivos que trabajan conjuntamente para permitir a los jugadores competir entre sí o contra una inteligencia artificial (IA) que emplea el algoritmo Minimax para tomar decisiones.

## Requisitos

- Python 3.x
- Pygame (se instala con `pip install pygame`)

## Ejecución del Juego

Para iniciar el juego, ejecuta el archivo `runner.py`. Se abrirá una ventana que permite elegir jugar como 'X' o como 'O', y luego mostrará el tablero del juego. El usuario puede hacer clic en las celdas vacías para realizar sus movimientos.
Esto se puede realizar con:
``` bash
python3 runner.py
```
### Archivos del Proyecto

1. **`tictactoe.py`: Lógica del Juego y Algoritmo Minimax**

   - **Descripción**: Contiene la lógica del juego del Ta-Te-Ti, incluyendo las reglas del juego y el algoritmo Minimax para la IA.
  
   - **Funciones Destacadas**:
     - `initial_state()`: Retorna el estado inicial del tablero.
     - `player(board)`: Determina el jugador con el próximo turno.
     - `actions(board)`: Devuelve un conjunto de todas las acciones posibles en el tablero.
     - `result(board, action)`: Genera el tablero resultante después de un movimiento.
     - `winner(board)`: Determina si hay un ganador en el tablero.
     - `terminal(board)`: Verifica si el juego ha terminado.
     - `utility(board)`: Devuelve la utilidad (puntaje) del tablero.
     - `minimax(board)`: Implementa el algoritmo Minimax para seleccionar la mejor jugada posible.
     - `minimax_score(board)`: Función auxiliar para el algoritmo Minimax.

2. **`util.py`: Estructuras de Datos y Funciones Auxiliares**

   - **Descripción**: Define estructuras de datos y funciones auxiliares utilizadas en el algoritmo Minimax.
  
   - **Clases Destacadas**:
     - `Node`: Representa un nodo en un árbol de búsqueda con atributos como estado, padre y acción.
     - `StackFrontier` y `QueueFrontier`: Estructuras de datos utilizadas para gestionar la frontera en la búsqueda.

3. **`runner.py`: Interfaz Gráfica y Lógica del Juego**

   - **Descripción**: Es el archivo principal que ejecuta el juego con la interfaz gráfica de Pygame.
  
   - **Aspectos Destacados**:
     - Interfaz gráfica: Presenta la ventana del juego y maneja la interacción con el usuario.
     - Turnos de jugador: Alterna entre turnos de usuario y de la IA (si está involucrada).
     - Ciclo de juego: Verifica clics, realiza movimientos y muestra el resultado al final del juego.

## Inteligencia Artificial (IA) - Algoritmo Minimax

El archivo `tictactoe.py` es fundamental para la implementación de la inteligencia artificial en el juego del Ta-Te-Ti. El algoritmo Minimax permite a la IA seleccionar la mejor jugada posible, considerando todos los posibles movimientos del juego. La función `minimax(board)` evalúa recursivamente las jugadas para maximizar las probabilidades de ganar o minimizar las pérdidas, asumiendo que el oponente también juega de manera óptima.

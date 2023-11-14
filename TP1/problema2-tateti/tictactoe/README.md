# Resolución de Problemas - Tic Tac Toe

## Descripción del Proyecto

Este proyecto implementa el juego del "Tic Tac Toe" (tres en línea) en Python utilizando la biblioteca Pygame. Está compuesto por dos archivos:

### `tictactoe.py`

- Define las reglas del juego del "Tic Tac Toe".
- Gestiona la lógica del juego, incluyendo la creación del tablero, turnos de jugadores, movimientos válidos, determinación de ganadores y algoritmo de inteligencia artificial (IA) para tomar decisiones.
- Contiene funciones clave como `initial_state`, `player`, `actions`, `result`, `winner`, `terminal`, `utility` y `minimax` para controlar el flujo del juego y determinar el mejor movimiento posible para la IA.

### `runner.py`

- Utiliza la biblioteca Pygame para renderizar la interfaz gráfica del juego.
- Permite al usuario jugar contra la IA (inteligencia artificial) o entre dos jugadores humanos.
- Gestiona la visualización del tablero, turnos, detección de clics del mouse y manejo del estado del juego.

## Resolución de Problemas

El proyecto aborda varios problemas de programación, incluyendo:

1. **Lógica del Juego**: Implementa reglas y condiciones para determinar el estado del juego, movimientos válidos, ganadores y finalización del juego.
2. **Algoritmo Minimax**: Utiliza el algoritmo Minimax para que la IA tome decisiones óptimas al seleccionar su próximo movimiento en base al estado actual del tablero.
3. **Interfaz Gráfica**: Desarrolla una interfaz de usuario utilizando Pygame para proporcionar una experiencia interactiva al usuario.

## Partes Importantes del Código

### `tictactoe.py`

- **`initial_state()`**: Retorna el estado inicial del tablero.
- **`player(board)`**: Determina el jugador que tiene el próximo turno.
- **`actions(board)`**: Retorna las acciones posibles en el tablero actual.
- **`result(board, action)`**: Retorna el tablero resultante después de realizar una acción.
- **`winner(board)`**: Determina el ganador del juego, si lo hay.
- **`terminal(board)`**: Verifica si el juego ha terminado.
- **`utility(board)`**: Asigna un valor al estado del tablero para el jugador X, O o empate.
- **`minimax(board)`**: Calcula el mejor movimiento posible para la IA usando el algoritmo Minimax.

### `runner.py`

- **Interfaz Gráfica**: Implementa la visualización del juego, manejo de eventos del usuario y lógica para interactuar con el tablero y la IA.

Este proyecto muestra cómo abordar problemas de lógica, algoritmos y diseño de interfaz para desarrollar un juego funcional de Tic Tac Toe en Python.

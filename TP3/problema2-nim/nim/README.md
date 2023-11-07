# Aprendizaje por Refuerzo - TP3 Nim

Este proyecto presenta una implementación del algoritmo de aprendizaje por refuerzo Q-Learning para jugar al juego del Nim. En este juego, los jugadores toman turnos para quitar elementos de pilas específicas. El objetivo es dejar al oponente con la última pila. La inteligencia artificial (IA) aprende a jugar al Nim mediante el aprendizaje por refuerzo para tomar decisiones óptimas.

## Contenido del Repositorio

- **`play.py`**: Este archivo contiene el código principal para entrenar la IA y jugar contra ella. `train()` entrena la IA mediante Q-Learning y `play()` permite a un jugador humano enfrentarse a la IA.

- **`nim.py`**: Contiene la implementación del juego del Nim (`Nim` class) y la IA (`NimAI` class) que utiliza Q-Learning para aprender a jugar.

## Partes Importantes del Código

### `Nim` Class

- **`__init__(self, initial=[1, 3, 5, 7])`**: Inicializa el estado del juego con las pilas iniciales.

- **`available_actions(cls, piles)`**: Retorna todas las acciones posibles en un estado dado.

- **`move(self, action)`**: Realiza un movimiento en el juego.

### `NimAI` Class

- **`__init__(self, alpha=0.5, epsilon=0.1)`**: Inicializa la IA con los valores de alfa y épsilon para el aprendizaje por refuerzo.

- **`update(self, old_state, action, new_state, reward)`**: Actualiza los valores Q después de cada movimiento.

- **`best_future_reward(self, state)`**: Retorna la mejor recompensa futura posible para un estado dado.

- **`choose_action(self, state, epsilon=True)`**: Decide la siguiente acción a tomar, considerando la exploración y la explotación.

### `train(n)` Function

- **`train(n)`**: Entrena la IA jugando `n` juegos contra sí misma. Utiliza Q-Learning para actualizar los valores Q durante el entrenamiento.

### `play(ai, human_player=None)` Function

- **`play(ai, human_player=None)`**: Permite a un jugador humano jugar contra la IA entrenada. La IA utiliza sus valores Q aprendidos para tomar decisiones durante el juego.

## Cómo Usar

1. Ejecutar `python play.py` para entrenar la IA y jugar contra ella.

2. Durante el juego, ingresar las pilas y la cantidad de elementos a remover siguiendo las indicaciones.

## Requisitos

- Python 3.x
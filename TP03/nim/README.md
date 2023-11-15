# Proyecto de Implementación de IA para Juego Nim

Este proyecto es una implementación del juego Nim en Python, donde se ha desarrollado una inteligencia artificial (IA) para jugar contra un jugador humano o por sí misma.

## Descripción

El juego Nim es un juego matemático con pilas de elementos donde los jugadores retiran elementos por turnos. El objetivo es dejar al oponente sin movimientos posibles, tomando la última pieza.

En esta implementación, se ha creado una IA basada en el algoritmo de aprendizaje por refuerzo Q-learning para jugar de manera estratégica y eficiente al Nim.

## Estructura del Proyecto

El proyecto consta de dos archivos principales:

- **`nim.py`**: Contiene la implementación del juego Nim y la clase `NimAI` que representa la inteligencia artificial para jugar al Nim.
- **`play.py`**: Script que entrena la IA mediante juegos repetidos y permite a un jugador humano enfrentarse a la IA.

## Clase `NimAI`

La clase `NimAI` es responsable de la toma de decisiones de la IA. Algunos métodos importantes incluyen:

- `update`: Actualiza el modelo Q-learning basado en el estado anterior, la acción tomada y el nuevo estado resultante.
- `choose_action`: Decide la mejor acción a tomar en un estado dado, considerando la exploración.

## Entrenamiento de la IA

El script `play.py` entrena la IA jugando múltiples juegos contra sí misma. La IA actualiza sus estrategias a medida que aprende de los resultados de cada juego.

## Juego contra la IA

El mismo script `play.py` permite a un jugador humano enfrentarse a la IA. El jugador puede decidir si quiere jugar como primer o segundo jugador.

## Uso

Para jugar contra la IA, ejecuta el script `play.py` y sigue las instrucciones que se muestran en la consola.

```bash
python play.py
```

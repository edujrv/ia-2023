# Proyecto de Lógica y Razonamiento

## Descripción

Este proyecto se centra en resolver una serie de puzzles lógicos utilizando programación en Python. Los puzzles están basados en declaraciones de personajes que pueden ser Caballeros (Knights) o Embusteros (Knaves). Mediante el razonamiento lógico, se intenta determinar la verdadera naturaleza de cada personaje.

## Archivos

### `logic.py`

El archivo `logic.py` contiene la implementación de clases y métodos que representan elementos lógicos y operaciones. Las clases principales incluyen:

- **Sentence**: Una clase base que define métodos genéricos para evaluación, fórmulas y símbolos.
- **Symbol**: Representa un símbolo lógico.
- **Not**, **And**, **Or**, **Implication**, **Biconditional**: Clases para los operadores lógicos que heredan de la clase `Sentence`.

Estas clases permiten crear y manipular expresiones lógicas, evaluar su veracidad, generar fórmulas y obtener los símbolos involucrados en cada expresión.

### `puzzle.py`

En el archivo `puzzle.py`, se presentan varios enigmas lógicos, cada uno definido con una serie de declaraciones hechas por los personajes. Se utilizan las clases y métodos definidos en `logic.py` para establecer las reglas lógicas de cada enigma y resolverlos.

Cada puzzle se construye mediante la creación de instancias de símbolos (`Symbol`) y utilizando los operadores lógicos para modelar las declaraciones de los personajes.

## Solución de los puzzles

El archivo `puzzle.py` contiene la resolución de los puzzles definidos a través de las declaraciones de los personajes. Utiliza las clases y métodos de `logic.py` para modelar las declaraciones y emplea la función `model_check` para evaluar qué personajes son Caballeros y cuáles son Embusteros en cada escenario.

### Inteligencia Artificial y Lógica

Aunque este proyecto no emplea técnicas de aprendizaje automático ni algoritmos de inteligencia artificial convencionales, representa un aspecto importante de la inteligencia computacional. La lógica y el razonamiento deductivo utilizados para resolver estos enigmas reflejan un tipo de inteligencia computacional que se basa en reglas predefinidas y la inferencia lógica.

La resolución de los enigmas se lleva a cabo mediante el uso de reglas lógicas y el razonamiento para inferir la verdadera naturaleza de cada personaje a partir de las declaraciones hechas por ellos.

## Ejecución

Para resolver los puzzles, simplemente ejecuta el archivo `puzzle.py`. Los resultados se mostrarán en la consola, indicando qué personajes son Caballeros y cuáles son Embusteros en cada uno de los enigmas.

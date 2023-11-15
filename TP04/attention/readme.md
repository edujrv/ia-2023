# Modelo de Lenguaje BERT con Máscara y Visualización de Atención

Este script en Python utiliza la biblioteca `transformers` de Hugging Face para realizar modelado de lenguaje con máscara utilizando BERT (Bidirectional Encoder Representations from Transformers). Además, genera diagramas de atención para visualizar los puntajes de autoatención para diferentes capas y cabezas del modelo.

## Requisitos

Asegúrate de tener las bibliotecas necesarias instaladas ejecutando:

```bash
pip install tensorflow transformers pillow
```

## Uso

1. Ejecuta el script:

```bash
python mask.py
```

3. Ingresa un texto que contenga un token enmascarado cuando se te solicite. El script generará predicciones para el token enmascarado y visualizará los puntajes de atención.

## Configuración

- `MODEL`: Modelo de lenguaje preentrenado con máscara, el valor predeterminado es "bert-base-uncased".
- `K`: Número de predicciones a generar, el valor predeterminado es 3.
- `FONT`: Ruta al archivo de fuente TrueType para la visualización.
- `GRID_SIZE`: Tamaño de la cuadrícula para la visualización de la atención.
- `PIXELS_PER_WORD`: Tamaño de píxeles por palabra en la visualización de la atención.

## Visualización

El script genera diagramas de atención para una capa y cabeza específicas. Los diagramas se guardan como archivos PNG con nombres que indican la capa y la cabeza.
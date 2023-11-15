# Clasificación de Señales de Tráfico usando una Red Neuronal Convolucional (CNN)

Este script en Python utiliza TensorFlow y OpenCV para crear y entrenar una Red Neuronal Convolucional (CNN) para clasificar señales de tráfico. El script puede cargar un conjunto de datos de imágenes de señales de tráfico, dividirlo en conjuntos de entrenamiento y prueba, entrenar la CNN, evaluar su rendimiento y guardar el modelo entrenado si así se desea.

## Prerrequisitos

Asegúrate de tener las bibliotecas necesarias instaladas. Puedes instalarlas utilizando:

```bash
pip install numpy opencv-python tensorflow scikit-learn
```

## Uso

```bash
python traffic.py directorio_de_datos [modelo.h5]
```

- `directorio_de_datos`: Ruta al directorio que contiene subdirectorios para cada categoría de señal de tráfico, donde cada subdirectorio contiene imágenes de la señal de tráfico correspondiente.
- `modelo.h5` (opcional): Si se proporciona, el modelo entrenado se guardará en este archivo.

## Parámetros

Puedes personalizar los siguientes parámetros en el script:

- `EPOCHS`: Número de épocas de entrenamiento.
- `IMG_WIDTH` y `IMG_HEIGHT`: Ancho y alto a los cuales se redimensionan las imágenes de entrada.
- `NUM_CATEGORIES`: Número de categorías de señales de tráfico. Cambia a 3 para un conjunto de datos pequeño.
- `TEST_SIZE`: La proporción del conjunto de datos que se incluirá en la división de prueba.

## Cómo funciona

1. **Carga de Datos**: El script lee imágenes y sus etiquetas correspondientes desde el directorio especificado en `directorio_de_datos`.

2. **Preprocesamiento de Datos**: Las imágenes se redimensionan y las etiquetas se convierten al formato categórico.

3. **División de Datos**: El conjunto de datos se divide en conjuntos de entrenamiento y prueba.

4. **Construcción del Modelo CNN**: Se crea un modelo CNN simple utilizando la API Keras de TensorFlow.

5. **Entrenamiento del Modelo**: El modelo se entrena en el conjunto de entrenamiento.

6. **Evaluación**: Se evalúa el rendimiento del modelo entrenado en el conjunto de prueba.

7. **Guardado del Modelo**: Si se proporciona un nombre de archivo para el modelo, este se guarda en un archivo.

## Ejemplo

```bash
python traffic.py ruta/a/dataset_de_senales_de_trafico modelo.h5
```

Esto entrenará el modelo en las imágenes en `ruta/a/dataset_de_senales_de_trafico` y guardará el modelo entrenado en `modelo.h5`. Ajusta los parámetros según sea necesario para tu conjunto de datos y preferencias.
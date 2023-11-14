# Descripción del Proyecto

## Clasificación de Señales de Tráfico usando Redes Neuronales Convolucionales (CNN)

Este proyecto implementa una red neuronal convolucional (CNN) para clasificar señales de tráfico a partir de un conjunto de datos proporcionado. Se utiliza TensorFlow y OpenCV en Python para cargar, procesar y entrenar el modelo.

## Estructura de Carpetas y Archivos

- **`traffic.py`**: Contiene el código principal para cargar los datos, entrenar el modelo y guardar el modelo entrenado si es necesario.
- **`gtsrb`**: Carpeta que contiene 47 subcarpetas numeradas del 0 al 46, cada una representando una categoría de señal de tráfico. Cada subcarpeta contiene imágenes en formato .ppm de las señales de tráfico correspondientes.

## Requisitos

- Python 3.x
- Bibliotecas:
  - TensorFlow
  - OpenCV (cv2)
  - NumPy
  - scikit-learn

## Uso

```bash
python traffic.py data_directory [model.h5]
```

### Funcionalidad del Código

#### `main()` - Función Principal
- Verifica los argumentos de línea de comandos.
- Carga las imágenes y etiquetas del directorio de datos.
- Divide los datos en conjuntos de entrenamiento y prueba.
- Obtiene un modelo de red neuronal convolucional.
- Entrena el modelo y evalúa su rendimiento.
- Guarda el modelo entrenado si se proporciona un nombre de archivo.

#### `load_data(data_dir)` - Carga de Datos
- Carga las imágenes y sus etiquetas desde el directorio especificado.
- Lee las imágenes en formato .ppm y las redimensiona a las dimensiones requeridas.

#### `get_model()` - Obtención del Modelo CNN
- Crea un modelo secuencial de red neuronal convolucional.
- Utiliza capas convolucionales, de agrupación y completamente conectadas.
- Compila el modelo con el optimizador Adam y la función de pérdida de entropía cruzada categórica.

### Parámetros de Configuración
- `EPOCHS`: Número de épocas para entrenar el modelo.
- `IMG_WIDTH` y `IMG_HEIGHT`: Dimensiones de las imágenes de entrada.
- `NUM_CATEGORIES`: Número total de categorías de señales de tráfico.
- `TEST_SIZE`: Proporción de datos a utilizar como conjunto de prueba.

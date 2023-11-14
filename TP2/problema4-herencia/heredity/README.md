# Conocimiento y Razonamiento: Herencia

Este programa en Python aborda el cálculo de probabilidades relacionadas con la herencia genética y rasgos heredados. Utiliza datos sobre genes, rasgos y relaciones familiares para calcular las probabilidades conjuntas de ciertos eventos genéticos y de rasgos.

## Estructura del Archivo heredity.py

El archivo `heredity.py` se estructura de la siguiente manera:

### Definición de Probabilidades

El programa define las probabilidades relacionadas con la presencia de genes (`gene`), los rasgos (`trait`) y la probabilidad de mutación (`mutation`) en el diccionario `PROBS`.

### Función Principal `main()`

- Carga los datos desde un archivo CSV proporcionado como argumento en la línea de comandos.
- Calcula las probabilidades de genes y rasgos para cada persona en función de la información proporcionada y las relaciones familiares.
- Utiliza las probabilidades conjuntas para calcular y actualizar las probabilidades de gene y trait para cada persona.
- Normaliza las probabilidades para que sumen 1 y reflejen proporciones relativas.

### Funciones Importantes

- `load_data(filename)`: Carga los datos desde un archivo CSV que contiene información sobre genes, rasgos y relaciones familiares.
- `powerset(s)`: Retorna todos los subconjuntos posibles de un conjunto dado.
- `joint_probability(people, one_gene, two_genes, have_trait)`: Calcula la probabilidad conjunta de ciertos eventos genéticos y de rasgos para un conjunto de personas.
- `update(probabilities, one_gene, two_genes, have_trait, p)`: Actualiza las distribuciones de probabilidad de gene y trait para cada persona dada una probabilidad conjunta `p`.
- `normalize(probabilities)`: Normaliza las distribuciones de probabilidad para que sumen 1 y reflejen proporciones relativas.

## Uso

El programa se ejecuta desde la línea de comandos con el siguiente formato:

```bash
python heredity.py data.csv
```

## Notas

Este programa utiliza la lógica de probabilidad y relaciones familiares para calcular y predecir la probabilidad de genes y rasgos en individuos, proporcionando una base para comprender conceptos de herencia y genética.

---

¡Explora y comprende las probabilidades de herencia genética con este programa!
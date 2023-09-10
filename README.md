# IA_framework

# DIEGO EMILIO BARRERA HDZ

# A01366802

## Descripción

Este es mi proyecto de uso de un framework que utiliza la regresión logística para llevar a cabo la clasificación de datos. El conjunto de datos utilizado se denomina "Raisin_Dataset.csv". 
Lo que se busca es predesir la clase de los datos segun su MajorAxisLength y su MinorAxisLength.
A continuación, se detallan las principales funcionalidades y pasos que se realizaron.

## Funcionalidades y secciones del código

### 1. Imports

En este bloque inicial, importamos varias bibliotecas necesarias para realizar diferentes tareas en el código

- `pandas` para la manipulación y análisis de datos.
- `numpy` para operaciones matemáticas y numéricas.
- `matplotlib` y `seaborn` para la visualización de datos.
- `sklearn` para las herramientas de aprendizaje automático, específicamente la regresión logística.

### 2. Lectura de los dato

Este paso se encarga de leer y limpiar el conjunto de datos.

- Leer el conjunto de datos y definirlos en `df`
- Entender la estructura de las columnas

### 3. Manejo de nuestros datos

En esta sección, se realiza el siguiente preprocesamiento de datos:

- Mapear las categorías en la columna "Class" a valores numéricos, es decir, asignar 0 a "Kecimen" y 1 a "Besni", de esta manera es más sencillo el manejo de los datos
- Definir las características de entrada `x` como un subconjunto de columnas que incluyen "MajorAxisLength" y "MinorAxisLength"
- Establecer la variable objetivo `y` como la columna "Class"
- Dividir los datos en conjuntos de entrenamiento y prueba utilizando la función `train_test_split` de scikit-learn

### 4. Modelo de Regresión Logística

En esta sección, se crea el modelo de regresión logística

- Crear un modelo de regresión logística con el fit
- Ajustar el modelo a los datos de entrenamiento utilizando `model.fit(x_train, y_train)`.

### 5. Evaluación del Modelo (TRAIN)

Aquí se evalúa el rendimiento del modelo en el conjunto de entrenamiento

- Predecir los valores objetivo en el conjunto de entrenamient
- Calcular la precisión y el coeficiente Rsquere

### 6. Evaluación del Modelo (TEST)

Aquí se evalúa el rendimiento del modelo en el conjunto de pruebas

- Predecir los valores objetivo en el conjunto de pruebas
- Calcular la precisión y el coeficiente Rsquere

### 7. Cross validation

Aquí se aplica Cross validation para evaluar la capacidad del modelo

- Calcular los puntajes R cuadrado para el modelo utilizando la validación cruzada
- Calcular la media de los puntajes R cuadrado obtenidos en la validación cruzada

### 8. Mean squere Error

Se calcula el EMean Squere Error (MSE) entre las predicciones del modelo y los valores reales en el conjunto de prueba. Este valor proporciona una medida de la calidad de las predicciones

### 9. Visualización de Datos

En esta sección, se realizan varias visualizaciones para comprender mejor los datos y las predicciones del modelo

- Una matriz de correlación entre las características "MajorAxisLength" y "MinorAxisLength" y la variable objetivo "Class".
- Un diagrama de dispersión que compara los valores reales y predichos en el conjunto de prueba.

## CONSIDERACIONES PARA CORRER EL CÓDIGO
Para poder ver ambas graficas es importante cerrar la primera y de inmediato aparecerá la segunda c:

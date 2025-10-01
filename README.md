# Challenge-Prediccion-de-Veracidad-de-Declaraciones-con-IA
Modelo de IA simple para la predicción de la veracidad de las declaraciones

Este proyecto implementa un modelo de inteligencia artificial para la predicción de la veracidad de declaraciones públicas, clasificándolas como verdaderas o falsas (fake news). El enfoque se centra en la aplicación de un modelo de Machine Learning entrenado para identificar patrones y correlaciones entre los datos históricos y contextuales asociadas a una declaración y su clasificación final.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

"GIF"

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 1. Preprocesamiento de datos
   La fase inicial se dedica a la limpieza, organización y preparación del conjunto de datos para optimizar el rendimiento del modelo.

### Proceso de Limpieza y Organización:

Inspección Inicial: Se realiza una visualización de la estructura tabular de los datos para comprender su conformación.

Mapeo de Variables Categóricas: Las columnas con valores de texto se mapean a representaciones numéricas, facilitando su posterior procesamiento por el algoritmo de Machine Learning.

Gestión de Datos Nulos: Se emplea la función .info() para identificar la cantidad de valores nulos. Con base en este análisis y la relevancia percibida, las columnas "Cargo del orador" y "Contexto" son eliminadas debido a su alta tasa de datos faltantes y su baja relevancia para el objetivo predictivo.

Análisis de Correlación: Se utiliza un mapa de calor para evaluar visualmente la relación estadística de cada variable con la columna dependiente, "Etiqueta".

   ### Mapa de calor:

   <img width="513" height="432" alt="image" src="https://github.com/user-attachments/assets/6d30b123-c892-4ddd-9c84-fc84a7c88ce8" />

   
## 2. Desarrollo del modelo

   Tras el análisis de correlación del mapa de calor, se seleccionan las variables que demuestran el mayor índice de concordancia con la variable objetivo "Etiqueta". Aunque los coeficientes de correlación son moderados, estas variables se consideran las más relevantes para el entrenamiento del modelo de clasificación.

### Variables Independientes Utilizadas

Cantidad verdadera: Número de declaraciones previas del orador clasificadas como verdaderas.

Afiliación Política: Partido o tendencia política del orador.

Estado: Estado o región asociada al orador o a la declaración.

El proceso prosigue con el entrenamiento del modelo de clasificación utilizando exclusivamente el dataset preprocesado y las variables independientes seleccionadas.


## 3. Evaluación y predicción

   La eficiencia del modelo se evalúa mediante un conjunto de datos de prueba externo (df_test_sin_etiqueta.csv) que carece de la variable objetivo.

### Proceso de Validación:

Generación de Predicciones: El modelo entrenado se aplica al archivo de prueba para generar y asignar los valores predictivos a la columna "Etiqueta".

Exportación y Validación Externa: El archivo con las etiquetas predichas se exporta y se somete a una plataforma de comprobación externa, la cual valida la eficiencia y la precisión del modelo frente a los valores reales.

## Resultados
   El modelo tiene un porcentaje de aprobación de alrededor del 60% porciento.
   
<img width="447" height="222" alt="Captura de pantalla 2025-10-01 090610" src="https://github.com/user-attachments/assets/c835e0de-fe77-4b2f-b2a5-0344e03f42f7" />

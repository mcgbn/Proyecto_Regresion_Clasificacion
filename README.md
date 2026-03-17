# Informe del proyecto Machine Learning: Regresión y Clasificacion

Ejercicio de creación de modelos de regresión lineal y de clasificación para documentos relacionados con el desempeño de estudiantes.

- Modelo de regresión para la variable objetivo *nota_final*
- Modelo de clasificación para la variable objetivo *aprobado*

Antes de realizar este modelo, se hace un **análisis exploratorio** del dato inicial, para entender el documento bruto obtenido (*notebooks/01_análisis_exploratorio*):  

- Detección de nulos, duplicados, tipo de datos y posibles errores.  
- Creación y visualización de la matriz de correlación  
- Exploración del comportamiento de estas variables en relación con la nota final vía gráficos  
- Análisis de inconsistencias en la tabla  

**Limpieza y procesado de los datos** a partir de lo detectado en el análisis exploratorio inicial (*notebooks/02_limpieza_previa*):  

- Gestion de nulos y outliers  
- Codificación y escalado de medidas, preparándolas para ambos modelos y guardándolo en distintos documentos limpios (en carpeta limpios)  

**Generación de modelos de regresión y clasificación:** 

**Regresión lineal** (*notebooks/03_regresion*):  

- Separacion en parte de entreno y test  
- Utilizacion del modelo de regresión lineal  
- Validación y residuos  
- Análisis de características  
- Evaluamos el modelo con las distintas métricas  
  - En la primera iteración, el modelo nos da una R2 alrededor del 0,5.
  - Para intentar mejorar el sistema de correlaciones, 1) se modifica la codificación en el notebook de limpieza previa   2) se escoge solo las variables con más correlación con la variable objetivo (*notebooks/03_regresion_optimizacion_modelo*). Este resultado era incluso más bajo en R2, por lo que se decide utilizar el inicial al tener mayor ajuste.  
  - En métricas, observamos que el test no se diferencia tanto de entreno, por lo que el modelo es consistente y no sufre de overfitting.  
- Entrenamiento final y regularización  

**Clasificación** (*notebooks/04_clasificacion*): 

- Separación en parte de entreno y test  
- Utilización del modelo de clasificación  
- Validación  
- Evaluación el modelo con las distintas métricas  
- Métricas balanceadas  
- Importancia de las características  
- Entrenamiento final  

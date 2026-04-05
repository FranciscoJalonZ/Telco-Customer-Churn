El proyecto utiliza el dataset *Telco Customer Churn* para identificar patrones de comportamiento en clientes de servicios de telefonía e internet. Se implementó un flujo de trabajo que abarca desde la limpieza de datos "crudos" hasta la evaluación de un modelo predictivo, asegurando la integridad de la información mediante el uso de Pipelines.

Tecnologías Utilizadas

* Lenguaje: Python 3.x
* Librerías principales:
    * Scikit-Learn: Para el preprocesamiento y modelado.
    * Pandas: Para la manipulación y análisis de datos.
    * NumPy: Para operaciones numéricas.
    * Matplotlib / Seaborn: Para visualización de datos (opcional).

Metodología Aplicada

Preparación de Datos
* División del Dataset: Se aplicó una división de 80% para entrenamiento y 20% para pruebas.
* Estratificación: Se utilizó el parámetro `stratify` para mantener la proporción de la variable objetivo en ambos conjuntos, crucial en problemas de clasificación.

Preprocesamiento (Pipeline de Datos)
Se implementó un `ColumnTransformer` para aplicar transformaciones específicas según el tipo de variable:
* Variables Numéricas:
    * Imputación: Llenado de valores faltantes mediante la *mediana*.
    * Escalamiento: Uso de `StandardScaler` para normalizar los rangos de las variables.
* Variables Categóricas:
    * Imputación: Uso de la *moda* (valor más frecuente).
    * Codificación: Implementación de `OneHotEncoder` para convertir categorías en vectores binarios procesables por el algoritmo.

Modelo de Machine Learning
Se seleccionó el algoritmo *Random Forest Classifier* debido a su robustez frente al sobreajuste (overfitting) y su capacidad para manejar múltiples variables de entrada.



Resultados

El modelo final alcanzó una métrica de desempeño sólida:
* Precisión (Accuracy):0.777 (78%)

Este resultado demuestra la efectividad de las técnicas de preprocesamiento aplicadas, permitiendo que el modelo generalice correctamente sobre datos no vistos previamente.

Estructura del Repositorio

* Telco-custom-churm.ipynb: Notebook principal con el código documentado.
* reporte_actividad.pdf: Informe detallado con análisis técnico y capturas de resultados.
* README.md: Descripción general del proyecto.

Cómo ejecutar el proyecto

Clona el repositorio:
   bash
   git clone (https://github.com/FranciscoJalonZ/Telco-Customer-Churn/blob/main/Telco-Customer-Churn.ipynb)

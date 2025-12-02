# Modelos Supervisados - DataAnalyst

## Proyecto Grupal

Detección de Enfermedades Cardiovasculares con Modelos de Machine Learning
Descripción del Proyecto
Este proyecto se enfoca en el desarrollo y evaluación de diversos modelos de Machine Learning para predecir la presencia de enfermedades cardiovasculares. Utilizando un dataset específico de condiciones cardíacas, se implementan y comparan algoritmos supervisados con el objetivo de identificar el modelo más eficiente en términos de precisión y tiempo de predicción.

Objetivo
El objetivo principal es construir y comparar modelos predictivos que puedan clasificar con alta precisión si un paciente tiene probabilidades de sufrir inconvenientes cardíacos, basándose en un conjunto de características clínicas. Además, se busca analizar el impacto de la selección de características en el rendimiento del modelo, evaluando tanto un conjunto completo de características como un subconjunto reducido.

Metodología
El proceso de análisis y modelado se estructura en las siguientes fases:

Carga y Exploración de Datos: Se carga el dataset de enfermedades cardiovasculares y se realizan análisis exploratorios básicos para entender la distribución y características de los datos.
Preprocesamiento de Datos: Se prepara el dataset para el entrenamiento de los modelos, incluyendo la división en conjuntos de entrenamiento y prueba.
Implementación y Evaluación de Modelos: Se implementan y entrenan los siguientes algoritmos de clasificación:
Árbol de Decisión (Decision Tree)
Naive Bayes (MultinomialNB y GaussianNB)
Máquinas de Soporte Vectorial (SVM)
K-Nearest Neighbors (KNN)
Perceptrón (Perceptron)
Optimización y Comparación: Para cada modelo, se evalúa su rendimiento utilizando métricas como la precisión (accuracy) y el tiempo de predicción. Se exploran diferentes configuraciones (por ejemplo, número de vecinos en KNN, diferentes random_states) y se compara el rendimiento de los modelos con el conjunto completo de características y con un subconjunto de 5 características clave (slope, chestpain, restingBP, restingrelectro, noofmajorvessels).
Formularios Interactivos: Se desarrollan formularios en el cuaderno para permitir la predicción interactiva de nuevos pacientes utilizando los modelos entrenados.
Resultados Clave
La tabla de resumen a continuación muestra una comparación de la precisión y el tiempo de predicción de los modelos evaluados, destacando el impacto de la selección de características:

Modelo	Columnas Usadas	Precisión (%)	Tiempo de Predicción (s)
Árbol de Decisión	5 columnas	95.0	0.003667
Árbol de Decisión	Todas	94.5	0.002380
Naive Bayesian	5 columnas	99.0	0.000933
Naive Bayesian	Todas	98.5	0.001837
SVM	5 columnas	92.0	0.003016
SVM	Todas	96.5	0.017086
KNN	5 columnas	96.50	0.004219
KNN	Todas	87.0	0.003346
Perceptrón	5 columnas	90.50	0.001384
Perceptrón	Todas	78.5	0.003867
Observaciones:
El modelo Naive Bayesian con 5 columnas demostró la mayor precisión (99.0%) y un excelente tiempo de predicción.
En general, el uso de un subconjunto de 5 columnas (slope, chestpain, restingBP, restingrelectro, noofmajorvessels) resultó en modelos más rápidos y, en muchos casos, con mayor o similar precisión que los modelos entrenados con todas las columnas. Esto sugiere que estas 5 características son altamente predictivas y que un modelo más simple puede ser más eficiente.
Conclusión
Este proyecto demuestra la efectividad de los modelos de Machine Learning en la predicción de enfermedades cardiovasculares. El análisis comparativo resalta la importancia de la selección de características, donde un conjunto reducido de atributos clave puede llevar a modelos más eficientes y precisos. El modelo Naive Bayesian, en particular, se destaca como una opción prometedora para esta tarea.

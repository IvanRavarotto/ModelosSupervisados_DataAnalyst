# Análisis y Predicción de Enfermedades Cardiovasculares mediante Clasificación Supervisada (DecisionTreeClassifier, Naive Bayesian, Support Vector Machines, K-Nearest Neighbor y Perceptron)

Este proyecto de Google Colab explora la aplicación de diversas técnicas de clasificación supervisada para analizar y predecir el riesgo de enfermedades cardiovasculares. El objetivo principal es construir modelos predictivos que puedan clasificar a los pacientes en categorías de 'Sano' o 'Enfermo' basándose en características médicas, utilizando etiquetas predefinidas en el entrenamiento.

## 📊 Dataset
El análisis se basa en el dataset de Enfermedades Cardiovasculares (`Cardiovascular_Disease_Dataset.csv`), cargado directamente desde un repositorio de GitHub. Este dataset contiene diversas métricas de salud de pacientes, incluyendo:

*   `age`: Edad
*   `gender`: Género (0: Femenino, 1: Masculino)
*   `chestpain`: Tipo de dolor de pecho
*   `restingBP`: Presión arterial en reposo
*   `serumcholestrol`: Colesterol sérico
*   `fastingbloodsugar`: Azúcar en sangre en ayunas
*   `restingrelectro`: Resultados electrocardiográficos en reposo
*   `maxheartrate`: Frecuencia cardíaca máxima alcanzada
*   `exerciseangia`: Angina inducida por ejercicio
*   `oldpeak`: Depresión del ST inducida por el ejercicio
*   `slope`: La pendiente del segmento ST pico del ejercicio
*   `noofmajorvessels`: Número de vasos principales coloreados por fluoroscopia
*   `target`: Variable objetivo (0: Sano, 1: Enfermo) - **Utilizada solo para evaluación, no para el entrenamiento de los modelos no supervisados**.


## 🚀 Metodología
### 1. Preprocesamiento de Datos
Antes de aplicar los algoritmos de clasificación, los datos fueron preprocesados y divididos en conjuntos de entrenamiento y prueba (80% y 20% respectivamente).

### 2. Modelos de Clasificación Supervisada
Se implementaron y evaluaron los siguientes algoritmos de clasificación:

*  **Decision Tree Classifier (Árbol de Decisión):** Un modelo intuitivo que toma decisiones de manera jerárquica. 
*  **Naive Bayesian (Clasificador Bayesiano Ingenuo):** Basado en el teorema de Bayes, asumiendo independencia entre las características. 
Se exploraron MultinomialNB (para el dataset completo) y GaussianNB (con un subconjunto de 5 características clave).
*  **Support Vector Machines (SVM):** Busca el hiperplano óptimo para separar las clases.
*  **K-Nearest Neighbor (KNN):** Clasifica un punto de datos basándose en la mayoría de las clases de sus 'K' vecinos más cercanos.
*  **Perceptron:** Un algoritmo de aprendizaje supervisado para clasificación binaria, que simula el funcionamiento básico de una neurona.
### 3. Evaluación de Modelos
Cada modelo fue evaluado utilizando métricas clave como:

Precisión (Accuracy Score): El porcentaje de predicciones correctas.
Matriz de Confusión: Para visualizar el rendimiento del clasificador (verdaderos positivos, verdaderos negativos, falsos positivos y falsos negativos).
Tiempo de Entrenamiento y Predicción: Para comparar la eficiencia computacional de cada algoritmo.
### 4. Predicción de Nuevos Pacientes
Se incluyó una funcionalidad para ingresar datos de un nuevo paciente y obtener una predicción de riesgo cardiovascular con cada uno de los modelos entrenados.

### 5. Conclusión
Este proyecto evaluó diversos modelos de clasificación supervisada (Decision Tree, Naive Bayesian, Support Vector Machines, K-Nearest Neighbor y Perceptron) para el diagnóstico de enfermedades cardiovasculares.
El modelo Gaussian Naive Bayesian se destacó como la opción más eficiente y precisa. Utilizando un conjunto reducido de solo 5 características ('slope', 'chestpain', 'restingBP', 'restingrelectro', 'noofmajorvessels'), este modelo alcanzó una precisión impresionante del 97.00% con un tiempo de predicción extremadamente rápido, ideal para aplicaciones en tiempo real.
Otros modelos como Support Vector Machine (SVM) sobre el dataset completo y K-Nearest Neighbor (KNN) con características reducidas también mostraron un rendimiento competitivo, ambos con una precisión del 96.5%.
En resumen, el Gaussian Naive Bayesian con el conjunto de características optimizado es el modelo recomendado para el diagnóstico de enfermedades cardiovasculares en este contexto, debido a su combinación superior de alta precisión y eficiencia computacional.

# Modelos Basados en Árboles - Parte 11: Clasificación 1
# Introducción

En esta parte del laboratorio, exploraremos la clasificación binaria utilizando un árbol de decisión para predecir eventos de muerte en pacientes con enfermedad cardíaca. Se analizará la distribución de clases, se partirá el conjunto de datos en entrenamiento y prueba de manera estratificada, se ajustará un árbol de decisión y se optimizarán sus hiperparámetros utilizando GridSearchCV. Finalmente, se evaluará la precisión del modelo optimizado.

# Análisis de la Distribución de Clases

Se observó que el conjunto de datos tiene una ligera inclinación hacia la clase "No" (eventos de muerte sin ocurrir), representando el 72.5% del total. Sin embargo, esta distribución no es tan desequilibrada como para afectar significativamente el rendimiento del modelo.

# Partición del Conjunto de Datos

Se realizó una partición estratificada del conjunto de datos en entrenamiento y prueba, utilizando la función train_test_split de scikit-learn. Se estableció un tamaño de conjunto de prueba del 20% y se preservó la distribución de clases en ambos conjuntos.

# Ajuste Inicial del Árbol de Decisión

Se entrenó un árbol de decisión inicial y se evaluó su precisión en el conjunto de prueba. Se obtuvo una precisión inicial del 78%, lo que indica un buen rendimiento inicial del modelo.

# Optimización de Hiperparámetros con GridSearchCV

Se utilizó GridSearchCV para optimizar los hiperparámetros del árbol de decisión: max_depth, min_samples_split y min_samples_leaf. Se exploraron diferentes valores para cada hiperparámetro y se seleccionó la combinación que maximizaba la precisión en la validación cruzada.

# Resultados de la Optimización

La búsqueda de GridSearchCV encontró la siguiente combinación de hiperparámetros como la mejor:

max_depth: 3
min_samples_leaf: 1
min_samples_split: 2
# Precisión Optimizada

Se entrenó un nuevo árbol de decisión con los hiperparámetros optimizados y se evaluó su precisión en el conjunto de prueba. Se obtuvo una precisión optimizada del 84%, lo que representa una mejora significativa del 6% en comparación con el modelo inicial.

# Conclusión

En este laboratorio, se demostró la efectividad de la optimización de hiperparámetros para mejorar el rendimiento de un modelo de clasificación. Mediante el uso de GridSearchCV, se logró identificar una configuración de hiperparámetros que optimizó la precisión del árbol de decisión en la predicción de eventos de muerte en pacientes con enfermedad cardíaca.

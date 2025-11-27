🦓 Proyecto Zoo – Clasificación de Animales con Machine Learning
📝 **Descripción**

Este proyecto clasifica animales según sus características físicas y de comportamiento usando Machine Learning.
Se trabajó con un dataset limpio de animales que incluye atributos como pelo, plumas, alas, patas, dieta, hábitat, entre otros, para predecir su tipo:
Mamífero 🐶, Ave 🐦, Reptil 🐍, Anfibio 🐸, Pez 🐟 o Insecto 🐜.

Incluye:

Limpieza y preparación de datos

Exploración de correlaciones

Entrenamiento de modelos

Optimización con Grid Search y Random Search

🎯 **Objetivo**

Entrenar un modelo de clasificación capaz de predecir el tipo de animal.

Analizar qué características son más relevantes para la predicción.

Comparar distintos modelos y elegir el más efectivo.

📊 **Dataset**

250 animales con 16 características principales.

Variables numéricas y categóricas transformadas para ML.

Target: type (tipo de animal).

Agrupación de clases minoritarias para reducir desbalance:

Reptiles + Anfibios → Reptiles_Amphibians

Insectos + Invertebrados → Invertebrados

⚙️ **Preparación de Datos**

Escalado de características numéricas con StandardScaler.

Codificación de variables categóricas.

Eliminación de valores innecesarios y duplicados.

Análisis de distribución de clases y correlaciones entre features.

🤖 **Modelos de Machine Learning**
Modelo	Accuracy
Gradient Boosting 🌟	76%
Regresión Logística	61%
Random Forest	70%
KNN	65%

Optimización de los dos mejores modelos con Grid Search y Random Search.

Gradient Boosting elegido como modelo final.

📈 **Evaluación**

Matriz de confusión para revisar aciertos y errores por clase.

Métricas: precisión, recall y F1-score por tipo de animal.

Visualización de la distribución de clases y correlación de características.

🐾 **Predicción Individual**

Ejemplo de cómo predecir el tipo de animal:

nuevo = [[1,0,0,1,0,0,1,1,1,1,0,0,1,0,1,4]]  # Nueva entrada con las mismas columnas que X
nuevo_scaled = scaler.transform(nuevo)
pred = final_model.predict(nuevo_scaled)
print("Predicción tipo de animal:", pred[0])

💻 **Requisitos**

Python 3.8+

Pandas

Scikit-learn

Matplotlib / Seaborn (opcional para gráficas)

✅ **Conclusión**

Este proyecto demuestra el flujo completo de Machine Learning:

Limpieza y preparación de datos

Selección de características

Entrenamiento y optimización de modelos

Evaluación y visualización de resultados

Permite clasificar animales de forma efectiva y entender qué atributos influyen más en la predicción.

👩‍💻 **Autora**

Nerea Gomez

Estudiante de Ironhack, 2025

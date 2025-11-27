# 🦓 Proyecto Zoo – Clasificación de Animales con Machine Learning

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python) 
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-0.24+-orange?logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-1.3+-lightgrey?logo=pandas)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📝 Descripción
Este proyecto clasifica animales según sus características físicas y de comportamiento usando **Machine Learning**.  
Se trabajó con un dataset limpio de animales que incluye atributos como **pelo, plumas, alas, patas, dieta, hábitat**, entre otros, para predecir su tipo:  

- Mamífero 🐶  
- Ave 🐦  
- Reptil 🐍  
- Anfibio 🐸  
- Pez 🐟  
- Insecto 🐜  

El proyecto incluye:  
- Limpieza y preparación de datos  
- Exploración de correlaciones  
- Entrenamiento de modelos  
- Optimización con Grid Search y Random Search  

---

## 🎯 Objetivo
<details>
<summary>Click para ver detalles</summary>

- Entrenar un modelo de clasificación capaz de predecir el **tipo de animal**.  
- Analizar qué características son más relevantes para la predicción.  
- Comparar distintos modelos y elegir el más efectivo.  

</details>

---

## 📊 Dataset
<details>
<summary>Click para ver detalles</summary>

- **101 animales** con **16 características principales**.  
- Variables numéricas y categóricas transformadas para Machine Learning.  
- **Target:** `type` (tipo de animal).  

**Agrupación de clases minoritarias:**  
- Reptiles + Anfibios → `Reptiles_Amphibians`  
- Insectos + Invertebrados → `Invertebrados`  

</details>

---

## ⚙️ Preparación de Datos
<details>
<summary>Click para ver detalles</summary>

- Escalado de características numéricas con **StandardScaler**.  
- Codificación de variables categóricas.  
- Eliminación de valores innecesarios y duplicados.  
- Análisis de distribución de clases y correlaciones entre features.  

</details>

---

## 🤖 Modelos de Machine Learning

| Modelo | Accuracy |
|--------|---------|
| Gradient Boosting 🌟 | 76% |
| Regresión Logística | 61% |
| Random Forest | 70% |
| KNN | 65% |

<details>
<summary>Optimización</summary>

- Optimización de los dos mejores modelos con **Grid Search** y **Random Search**.  
- **Gradient Boosting** elegido como modelo final.  

</details>

---

## 📈 Evaluación
<details>
<summary>Click para ver detalles</summary>

- **Matriz de confusión** para revisar aciertos y errores por clase.  
- Métricas: **precisión, recall y F1-score** por tipo de animal.  
- Visualización de la **distribución de clases** y **correlación de características**.  

</details>

---

## 🐾 Predicción Individual
```python
nuevo = [[1,0,0,1,0,0,1,1,1,1,0,0,1,0,1,4]]  # Nueva entrada con las mismas columnas que X
nuevo_scaled = scaler.transform(nuevo)
pred = final_model.predict(nuevo_scaled)
print("Predicción tipo de animal:", pred[0])
```

---

## 💻 Requisitos

- Python 3.8+

- Pandas

- Scikit-learn

- Matplotlib / Seaborn (opcional)

## ✅ Conclusión

Este proyecto demuestra el flujo completo de Machine Learning:

- Limpieza y preparación de datos

- Selección de características

- Entrenamiento y optimización de modelos

- Evaluación y visualización de resultados

Permite clasificar animales de forma efectiva y entender qué atributos influyen más en la predicción.
El Gradient Boosting se confirmó como el modelo más eficiente para este dataset.
Además, se evidenció que características como patas, tipo de alimentación y hábitat son determinantes para predecir correctamente el tipo de animal.

## 👩‍💻 Autora

Nerea Gomez
Estudiante de Ironhack, 2025

# 📈 Telecom X - Parte 2: Predicción de Cancelación (Churn)

## 📖 Descripción del Proyecto
Este repositorio contiene la segunda fase del proyecto "Telecom X". Tras realizar el Análisis Exploratorio de Datos (EDA) inicial, esta etapa se centra en el desarrollo de un pipeline de **Machine Learning** capaz de predecir qué clientes tienen mayor probabilidad de cancelar sus servicios (Churn). 

El objetivo es proporcionar al equipo de negocio herramientas predictivas robustas y recomendaciones estratégicas respaldadas por datos para anticiparse a la pérdida de clientes.

## 🎯 Objetivos y Alcance
* **Preprocesamiento:** Limpieza final, eliminación de variables irrelevantes (ej. `customerID`), y transformación de variables categóricas mediante One-Hot Encoding.
* **Balanceo de Clases:** Aplicación de la técnica **SMOTE** (Synthetic Minority Over-sampling Technique) para manejar el desbalance natural de la variable objetivo en los datos de entrenamiento.
* **Selección de Variables:** Análisis de correlación evitando problemas de multicolinealidad perfecta (ej. descartando variables redundantes como costos diarios frente a costos mensuales).
* **Modelado:** Entrenamiento y comparación de dos algoritmos: **Regresión Logística** (con datos normalizados mediante `StandardScaler`) y **Random Forest**.
* **Evaluación:** Medición del rendimiento mediante Exactitud, Precisión, Recall, F1-Score y Matrices de Confusión.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 3.x
* **Entorno:** Jupyter Notebook (`.ipynb`)
* **Manipulación de Datos:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (`LogisticRegression`, `RandomForestClassifier`, `StandardScaler`, métricas)
* **Manejo de Desbalanceo:** Imbalanced-learn (`SMOTE`)
* **Visualización:** Matplotlib, Seaborn

## 💡 Resultados Clave
Tras corregir sesgos y balancear los datos, los modelos arrojaron los siguientes insights:
* **Desempeño:** La **Regresión Logística** demostró ser el modelo más estable y efectivo para este problema de negocio, logrando un **Recall del 63%** en la predicción de cancelaciones, superando al Random Forest (58%) que presentó ligeros indicios de sobreajuste (overfitting).
* **Factores de Riesgo:** Los clientes con contratos **"Mes a Mes"** y aquellos suscritos al servicio de **Fibra Óptica** presentan la mayor probabilidad de fuga.
* **Retención Natural:** La antigüedad del cliente (`tenure`) es el principal factor protector; los primeros meses de servicio son la ventana crítica de riesgo.

## 🚀 Instalación y Uso

1. Clona este repositorio en tu máquina local:
   ```bash
   git clone [https://github.com/JordanValenzuela22/TelecomX_parte2_Latam.git](https://github.com/JordanValenzuela22/TelecomX_parte2_Latam.git)

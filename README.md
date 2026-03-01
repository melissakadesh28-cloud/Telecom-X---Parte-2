

# 📊 Telecom X - Parte 2: Análisis Predictivo para Churn


![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat-square&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data-150458?style=flat-square&logo=pandas&logoColor=white)
![Estado](https://img.shields.io/badge/Estado-Finalizado-brightgreen?style=flat-square)

---

## 📖 Índice
1. [Resumen Ejecutivo](#-resumen-ejecutivo)
2. [Estructura del Proyecto](#-estructura-del-proyecto)
3. [Procesamiento de Datos](#-procesamiento-de-datos)
4. [Análisis de Desempeño por Modelo](#-análisis-de-desempeño-por-modelo)
5. [Hallazgos de Negocio (Insights)](#-hallazgos-de-negocio-insights)
6. [Instrucciones de Despliegue](#-instrucciones-de-despliegue)
7. [Licencia](#-licencia)
8. [Autora](#-autora)

---

## 🎯 Resumen 
Este proyecto desarrolla un modelo de clasificación para predecir la deserción de clientes (Churn) en una compañía de telecomunicaciones. El enfoque principal fue identificar patrones de comportamiento que permitan a la empresa ejecutar campañas de retención más efectivas y dirigidas.

## **1. Introducción al Modelado**
En esta fase del proyecto, el objetivo principal es desarrollar un modelo de clasificación capaz de predecir qué clientes tienen una alta probabilidad de abandonar los servicios de la compañía. Se prioriza la métrica de **Recall** para asegurar la detección de la mayor cantidad de desertores potenciales.

---

## 📂 Estructura del Proyecto
* **Cuaderno de Análisis**: Documento principal con el código, visualizaciones y entrenamiento del modelo.
* **Dataset Procesado**: Archivo CSV con los datos limpios y transformados listos para el modelado.

---

## 🛠️ Procesamiento de Datos
En esta etapa, se realizó un tratamiento exhaustivo de la información para asegurar la calidad de las predicciones. Se eliminaron datos irrelevantes como los IDs de cliente, se transformaron las categorías de texto en valores numéricos y se estandarizaron las escalas de los cargos mensuales. Además, se aplicó la técnica **SMOTE** para equilibrar los datos, permitiendo que el modelo aprenda a identificar con precisión a los clientes que realmente cancelan el servicio.



---

## 📈 Análisis de Desempeño por Modelo

### Modelo de Regresión Logística (Seleccionado)
Este modelo fue elegido como la solución definitiva debido a su excelente capacidad de detección. Logró un **Recall del 81%**, lo que garantiza que la gran mayoría de los clientes en riesgo sean identificados correctamente. Con una precisión equilibrada y un F1-Score de 0.63, es la herramienta ideal para minimizar los falsos negativos en el negocio.

### Modelo de Random Forest (Optimizado)
Se entrenó un Bosque Aleatorio con una profundidad máxima de 10 niveles, alcanzando una exactitud general del 77%. Sin embargo, su capacidad de detección (**Recall**) se limitó al 70%, lo que significa que omitiría a un 30% de los clientes en riesgo de fuga. A pesar de ser un modelo potente y estable, su menor sensibilidad lo hizo menos apto para este caso de uso donde la detección proactiva es prioritaria.

---

## 🚩 Hallazgos de Negocio (Insights)
* **Vulnerabilidad Contractual**: Los clientes con contratos mensuales tienen una probabilidad de fuga significativamente mayor que aquellos con planes a largo plazo.
* **Período Crítico**: Los primeros 12 meses de antigüedad son determinantes; es donde se concentra el mayor riesgo de abandono.
* **Cargos Mensuales**: Existe una relación directa entre cargos elevados y la probabilidad de churn, indicando que el precio es un factor decisivo si no hay servicios de valor percibido.

---

## 🚀 Instrucciones de Despliegue
1. Abrir el archivo `.ipynb` en **Google Colab** o entorno local.
2. Asegurarse de instalar la librería necesaria: `!pip install -U imbalanced-learn`.
3. Cargar el dataset en formato `.csv` y ejecutar las celdas de forma secuencial.

---

## 📄 Licencia
Este proyecto se distribuye bajo la **Licencia MIT**.

---

## ✍️ Autora
**Melissa Rodríguez** *Científica de Datos en Formación*



# 📊 Telecom X - Parte 2: Análisis Predictivo para Churn

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat-square&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data-150458?style=flat-square&logo=pandas&logoColor=white)
![Estado](https://img.shields.io/badge/Estado-Finalizado-brightgreen?style=flat-square)

---

## 🎯 Resumen Ejecutivo
Este proyecto desarrolla un modelo de clasificación para predecir la deserción de clientes (Churn) en una compañía de telecomunicaciones. El enfoque principal fue identificar patrones de comportamiento que permitan a la empresa ejecutar campañas de retención más efectivas y dirigidas.

---

## 🛠️ Ingeniería de Características
El proceso de preparación de datos incluyó una limpieza profunda para eliminar ruidos y variables irrelevantes. Se aplicó **One-Hot Encoding** para las variables categóricas y se normalizaron los datos numéricos. Finalmente, se utilizó la técnica **SMOTE** para balancear las clases, asegurando que el modelo aprendiera correctamente a identificar la clase minoritaria (los clientes que se van).

---

## 📈 Análisis de Desempeño por Modelo

### Modelo de Regresión Logística (Seleccionado)
Este modelo fue elegido como la solución definitiva debido a su excelente capacidad de detección. Logró un **Recall del 81%**, lo que garantiza que la gran mayoría de los clientes en riesgo sean identificados correctamente. Con una precisión equilibrada, es la herramienta ideal para minimizar los falsos negativos en el negocio.

### Modelo de Random Forest (Optimizado)
Se entrenó un Bosque Aleatorio con una profundidad máxima de 10 niveles, alcanzando una exactitud del 77%. Sin embargo, su **Recall fue del 70%**, lo que significa que omitiría a un 30% de los clientes en riesgo de fuga. A pesar de ser un modelo potente, su menor sensibilidad lo hizo menos apto para este caso de uso específico donde la detección es prioritaria.

---

## 🚩 Hallazgos de Negocio (Insights)
* **Vulnerabilidad Contractual**: Los clientes con contratos mensuales tienen una probabilidad de fuga significativamente mayor que aquellos con planes anuales.
* **Período Crítico**: Los primeros 12 meses de antigüedad son determinantes; es donde se concentra el mayor volumen de cancelaciones.
* **Impacto Económico**: Existe una relación directa entre los cargos mensuales elevados y el abandono del servicio, especialmente si el cliente no cuenta con servicios adicionales de valor.

---

## 🚀 Instrucciones de Despliegue
1. Abrir el archivo `.ipynb` en **Google Colab**.
2. Asegurarse de tener instalado `imbalanced-learn` para el balanceo de datos.
3. Cargar el dataset en formato `.csv` y ejecutar las celdas en orden.

---

## 📄 Licencia
Este proyecto se distribuye bajo la **Licencia MIT**.

---

## ✍️ Autora
**Melissa Rodríguez** *Científica de Datos en Formación*

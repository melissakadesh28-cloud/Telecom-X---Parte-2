
# 📊 Telecom X - Parte 2: Análisis Predictivo de Churn

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat-square&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data-150458?style=flat-square&logo=pandas&logoColor=white)

---

## 📑 Índice
1. [Propósito del Análisis](#-propósito-del-análisis)
2. [Estructura del Proyecto](#-estructura-del-proyecto-y-organización)
3. [Preparación de Datos](#️-descripción-del-proceso-de-preparación-de-datos)
4. [Modelización y Justificación](#-modelización-y-justificación-de-decisiones)
5. [Insights (EDA)](#-hallazgos-e-insights-eda)
6. [Instrucciones de Ejecución](#-instrucciones-para-ejecutar-el-cuaderno)
7. [Licencia](#-licencia)
8. [Autora](#️-autora)

---

## 🎯 Propósito del Análisis
El objetivo principal de este proyecto es **predecir la deserción de clientes (Churn)** en la compañía Telecom X. A través de este análisis, identificamos proactivamente a los usuarios con mayor probabilidad de cancelar su servicio basándonos en variables críticas, permitiendo ejecutar estrategias de retención oportunas antes de la pérdida del cliente.

---

## 📂 Estructura del Proyecto y Organización
El repositorio está organizado con los siguientes archivos esenciales:

* **`ML_TELECOMX_2.ipynb`**: Cuaderno principal con el flujo de trabajo: carga, EDA, preprocesamiento y modelos.
* **`datos_tratados_limpio.csv`**: Dataset procesado, codificado y normalizado.
* **`README.md`**: Documentación detallada del proyecto.
* **`LICENSE`**: Archivo con los términos legales (Licencia MIT).

---

## 🛠️ Descripción del Proceso de Preparación de Datos
Se aplicó un pipeline de ingeniería de características detallado:

1. **Clasificación de Variables**: Se categorizaron en **numéricas** (`MonthlyCharges`, `tenure`) y **categóricas** (`Contract`, `InternetService`).
2. **Normalización y Codificación**: 
   * **One-Hot Encoding** para variables categóricas.
   * **Escalado** de variables numéricas para evitar sesgos por magnitud.
3. **Balanceo de Clases**: Uso de **SMOTE** para mejorar la detección de la clase minoritaria (Churn).
4. **Separación de Datos**: División en **80% entrenamiento** y **20% prueba**.

---

## 📈 Modelización y Justificación de Decisiones
Evaluamos algoritmos priorizando el impacto para el negocio:

* **Regresión Logística (Seleccionado)**: Alcanzó un **Recall del 81%**.
* **Random Forest**: Logró buena exactitud, pero un Recall inferior (70%).

**Justificación**: Es preferible contactar a un cliente que quizás no se iba (Falso Positivo) que perder a uno real por falta de detección (Falso Negativo). Por ello, se eligió la Regresión Logística por su alto **Recall**.

---

## 🚩 Hallazgos e Insights (EDA)
* **Contratos**: Los contratos "mes a mes" tienen la tasa de abandono más alta.
* **Cargos**: Los cargos elevados en fibra óptica están correlacionados con la cancelación.

---

## 🚀 Instrucciones para Ejecutar el Cuaderno
1. **Instalación**: `pip install pandas scikit-learn imbalanced-learn matplotlib seaborn`.
2. **Carga**: Asegúrate de que `datos_tratados_limpio.csv` esté en el mismo directorio.
3. **Ejecución**: Ejecuta las celdas de `ML_TELECOMX_2.ipynb` secuencialmente.

---

## 📄 Licencia
Este proyecto está bajo la **Licencia MIT**. El texto legal completo se encuentra en el archivo **LICENSE** incluido en este repositorio.

---

## ✍️ Autora
**Melissa Rodríguez** *Científica de Datos en Formación*



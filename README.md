
# **📊 Telecom X - Parte 2: Análisis Predictivo para Churn**

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat-square&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Estado](https://img.shields.io/badge/Estado-Finalizado-brightgreen?style=flat-square)

---

## **📖 Índice**
1. [Resumen Ejecutivo](#1-resumen-ejecutivo)
2. [Introducción al Modelado](#2-introducción-al-modelado)
3. [Preparación y Procesamiento de Datos](#3-preparación-y-procesamiento-de-datos)
4. [Análisis Exploratorio (EDA) e Insights](#4-análisis-exploratorio-eda-e-insights)
5. [Análisis de Desempeño y Matriz de Confusión](#5-análisis-de-desempeño-y-matriz-de-confusión)
6. [Principales Factores que afectan la Cancelación](#6-principales-factores-que-afectan-la-cancelación)
7. [Estrategias de Retención Propuestas](#7-estrategias-de-retención-propuestas)
8. [Conclusión Crítica](#8-conclusión-crítica)

---

## **1. Resumen Ejecutivo**
Este proyecto desarrolla un modelo de clasificación para predecir la deserción de clientes (**Churn**) en una compañía de telecomunicaciones. El enfoque principal fue identificar patrones de comportamiento que permitan a la empresa ejecutar campañas de retención más efectivas y dirigidas.

---

## **2. Introducción al Modelado**
En esta fase del proyecto, el objetivo principal es desarrollar un modelo de clasificación capaz de predecir qué clientes tienen una alta probabilidad de abandonar los servicios de la compañía. Se prioriza la métrica de **Recall** para asegurar la detección de la mayor cantidad de desertores potenciales.

---

## **3. Preparación y Procesamiento de Datos**
Para garantizar la calidad de las predicciones, se realizó un flujo técnico estructurado:
* **Clasificación de Variables:** Identificación y separación de variables en **categóricas** y **numéricas**.
* **Codificación y Normalización:** Etapas de One-Hot Encoding para categorías y escalado de datos mediante `StandardScaler`.
* **División de Datos:** Separación de los datos en conjuntos de **entrenamiento y prueba** (80/20).
* **Balanceo (SMOTE):** Aplicación de remuestreo sintético (SMOTE) para corregir el desbalance de clases y mejorar la sensibilidad del modelo.

---

## **4. Análisis Exploratorio (EDA) e Insights**
Basado en el análisis previo a la modelización, se obtuvieron los siguientes hallazgos:
* **Gráficos de Antigüedad:** Muestran que la volatilidad es crítica durante el primer año (especialmente los primeros 6 meses).
* **Relación de Cargos:** El análisis detecta una correlación directa entre facturas elevadas y deserción.

---

## **5. Análisis de Desempeño y Matriz de Confusión**

El uso de la **Matriz de Confusión** fue la herramienta clave para validar que la Regresión Logística es el mejor "radar" de detección temprana:

### **Modelo Seleccionado: Regresión Logística**
* **Recall (81%):** Identifica correctamente a 8 de cada 10 clientes en riesgo de fuga. Supera por un 11% al Random Forest optimizado (70%).
* **F1-Score (0.63):** Mantiene el equilibrio más sólido entre detección y precisión, superando el 0.61 logrado por el Random Forest.
* **Robustez:** A diferencia de los modelos basados en árboles, la Regresión Logística ofrece una mayor estabilidad y generalización en este conjunto de datos.

### **Modelo Comparativo: Random Forest Optimizado**
Se configuró con límites para evitar **Overfitting** (`max_depth=10`). Aunque es un modelo potente, su menor capacidad de captura lo sitúa por debajo de los objetivos de esta misión.

---

## **6. Principales Factores que afectan la Cancelación**
El análisis de los coeficientes nos permite identificar los "disparadores" de fuga:

* **Tipo de Contrato (El mayor riesgo):** El contrato "Mes a mes" es el predictor más fuerte de cancelación. La ausencia de un compromiso a largo plazo facilita la migración hacia la competencia.
* **Antigüedad del Cliente (Tenure):** Existe una relación inversamente proporcional; superada la fase inicial de 12 meses, la probabilidad de abandono disminuye drásticamente.
* **Sensibilidad al Precio (Cargos Mensuales):** Clientes con cargos altos sin servicios de valor agregado percibido son los más propensos a buscar alternativas económicas.

---

## **7. Estrategias de Retención Propuestas**
* **Plan de Migración a la Lealtad:** Incentivar el paso de contratos mensuales a anuales mediante descuentos progresivos.
* **Programa de "Bienvenida Crítica":** Establecer un protocolo de seguimiento intensivo durante los primeros 12 meses del cliente.
* **Optimización de la Percepción de Valor:** Implementar "Bundles" (paquetes) con servicios adicionales (ej. Streaming o soporte premium) sin elevar el costo nominal.

---

## **8. Conclusión Crítica**
La elección de la Regresión Logística sobre el Random Forest se justifica por la prioridad de la misión: minimizar la pérdida de clientes. Aunque el Random Forest es ligeramente más preciso evitando falsas alarmas, la Regresión Logística rescata a un 11% más de desertores reales. En un mercado de alta competencia, el beneficio económico de prevenir esta fuga supera significativamente el costo operativo de las campañas de retención.

---
**Autora:** Melissa Rodríguez


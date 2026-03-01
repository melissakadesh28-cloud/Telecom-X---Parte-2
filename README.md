# 📊 Telecom X - Parte 2: Análisis Predictivo de Churn

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat-square&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data-150458?style=flat-square&logo=pandas&logoColor=white)

---

## 🎯 Propósito del Análisis
El objetivo principal es **predecir la deserción de clientes (Churn)** en Telecom X. Identificamos usuarios en riesgo mediante variables relevantes para ejecutar estrategias de retención proactivas antes de que cancelen el servicio.

---

## 📂 Estructura del Proyecto
* **`ML_TELECOMX_2.ipynb`**: Cuaderno principal con el flujo completo de limpieza, análisis y modelado.
* **`datos_tratados_limpio.csv`**: Dataset procesado y normalizado listo para el entrenamiento.
* **`LICENSE`**: Términos de uso del proyecto.

---

## 🛠️ Preparación de los Datos
Se aplicó un pipeline riguroso para asegurar la precisión del modelo:

1. **Clasificación**: Identificamos variables **categóricas** (tipo de contrato) y **numéricas** (cargos mensuales).
2. **Transformación**: Aplicamos codificación para textos y normalización para que los valores numéricos tengan la misma escala.
3. **División**: Los datos se separaron en **80% Entrenamiento** y **20% Prueba** para validar el rendimiento real.

---

## 📈 Modelización y Justificación
Evaluamos varios modelos, tomando decisiones basadas en el impacto de negocio:

* **Regresión Logística (Elegido)**: Logró un **81% de Recall**. 
* **Justificación**: En el Churn, preferimos un "Falso Positivo" (contactar a alguien que no se iba a ir) que un "Falso Negativo" (perder a un cliente por no detectarlo). Este modelo es el más eficiente para esta estrategia.

---

## 🚩 Insights y Gráficos (EDA)
El Análisis Exploratorio reveló que:
* Los clientes con **contratos mes a mes** tienen la tasa de abandono más alta.
* El uso de **fibra óptica** está correlacionado con mayores costos y mayor probabilidad de churn.



---

## 🚀 Instrucciones de Ejecución
1. Asegúrate de tener instalado: `pandas`, `scikit-learn`, `matplotlib` y `seaborn`.
2. Mantén el archivo **`datos_tratados_limpio.csv`** en la misma carpeta que el cuaderno.
3. Ejecuta las celdas de **`ML_TELECOMX_2.ipynb`** de forma secuencial.

---
**Autora:** Tu Nombre | Científica de Datos


# Telecom-X---Parte-2
Analizar el churn (cancelación) de clientes de una empresa de telecomunicaciones
![Python 3.10](https://img.shields.io/badge/Python-3.10-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas Data Analysis](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=flat-square&logo=pandas&logoColor=white)
![Seaborn Visualization](https://img.shields.io/badge/Seaborn-Visualization-444444?style=flat-square)
![Scikit-Learn ML](https://img.shields.io/badge/Scikit--Learn-Machine_Learning-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google_Colab-Notebook-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)
![Estado Finalizado](https://img.shields.io/badge/Estado-Finalizado-brightgreen?style=flat-square)

📖 Índice
Propósito del Proyecto

Estructura del Proyecto

Tecnologías Utilizadas

Preparación de los Datos

Demostración de Resultados

Factores de Riesgo

Instrucciones de Ejecución

Licencia

Autora

🎯 Propósito del Proyecto
El objetivo es predecir el churn (cancelación) de clientes mediante modelos de clasificación. Esto permite identificar proactivamente a los usuarios en riesgo y diseñar estrategias de retención basadas en datos reales de comportamiento y servicio.

📂 Estructura del Proyecto
TU_CUADERNO.ipynb: Cuaderno con el proceso completo de limpieza, EDA y modelado.

TU_DATASET.csv: Base de datos procesada utilizada para el entrenamiento.

🛠️ Tecnologías Utilizadas
Python 3.10: Lenguaje base.

Pandas: Manipulación de estructuras de datos.

Seaborn & Matplotlib: Generación de visualizaciones estadísticas.

Scikit-Learn: Implementación de modelos (Regresión Logística, Random Forest).

Imbalanced-Learn: Balanceo de datos con SMOTE.

🛠️ Preparación de los Datos
Limpieza: Eliminación de identificadores irrelevantes (customerID).

Transformación: Codificación de variables categóricas y normalización con StandardScaler.

División: Repartición de datos en 80% entrenamiento y 20% prueba.

Balanceo: Aplicación de SMOTE para corregir el desbalance de la clase "Churn".

📈 Demostración de Resultados
## 📈 Análisis de Desempeño por Modelo

### Modelo de Regresión Logística (Seleccionado)
Este modelo demostró ser la solución más robusta para los objetivos del negocio. Logró un **Recall del 81%**, lo que significa que es capaz de detectar a 8 de cada 10 clientes que realmente tienen la intención de cancelar. Con una exactitud del 75% y un F1-Score de 0.63, ofrece el mejor equilibrio para una estrategia de retención proactiva.

### Modelo de Random Forest (Optimizado)
El modelo de bosque aleatorio, tras un ajuste de hiperparámetros (`max_depth=10`), alcanzó una exactitud superior del 77%. Sin embargo, su capacidad de detección (**Recall**) se limitó al 70%, lo que implica que dejaría pasar a un 30% de clientes en riesgo. Aunque es un modelo muy estable, se descartó como opción principal debido a que en el contexto de Churn, el costo de omitir un desertor es más crítico que la precisión general.

Conclusión: Se seleccionó la Regresión Logística por su capacidad de detectar al 81% de los clientes que realmente cancelarán, maximizando el impacto de las campañas de retención.

🚩 Factores de Riesgo
Contratos "Month-to-month": Mayor volatilidad de permanencia.

Tenure (Antigüedad): El riesgo disminuye significativamente después del primer año.

Cargos Mensuales: Los costos elevados sin soporte técnico asociado incrementan la fuga.

🚀 Instrucciones de Ejecución
Abrir en Google Colab.

Instalar dependencias: !pip install -U imbalanced-learn.

Cargar el dataset .csv en la sesión y ejecutar secuencialmente.

📄 Licencia
Este proyecto cuenta con la Licencia MIT.

✍️ Autora
Lic. Melissa Rodríguez
Científica de Datos en Formación


# Alura-Telecom-2
Telecom X — Parte 2: Modelado Predictivo de Churn

Segunda parte del proyecto de análisis de evasión de clientes. A partir del dataset limpio de la Parte 1, se desarrollan modelos de machine learning para predecir qué clientes tienen mayor probabilidad de cancelar el servicio.

Objetivo
Construir modelos de clasificación que permitan identificar clientes en riesgo de churn, evaluar su desempeño y analizar los factores más influyentes en la cancelación.

Flujo de trabajo
- Preparación de datos
Se elimina customerID, se codifican variables binarias como 0/1 y se aplica one-hot encoding a las variables categóricas. El dataset final contiene 32 variables.

- Desbalance de clases
La proporción de churn es aproximadamente 74% clientes que permanecen y 26% clientes que cancelan. Se utiliza class_weight='balanced' para compensar este desbalance.

- División del dataset
Se divide el dataset en 80% entrenamiento y 20% prueba utilizando estratificación.

- Normalización
Se aplica StandardScaler para la Regresión Logística. Random Forest no requiere normalización.

Modelos entrenados
- Regresión Logística
- Random Forest

Evaluación
Se utilizan las métricas:
- Accuracy
- Precision
- Recall
- F1 Score

Matrices de confusión
Resultados
La Regresión Logística presenta un mayor recall, lo que permite detectar más clientes que realmente cancelan el servicio. Random Forest logra una mayor precisión general, pero pierde más casos reales de churn.

Debido a su mejor capacidad para identificar clientes en riesgo, la Regresión Logística puede ser más útil como sistema de alerta temprana para estrategias de retención.
Variables más relevantes

Los factores con mayor influencia en la predicción de churn incluyen:
tenure
- Monthly Charges
- contrato Month-to-month
- servicio Fiber optic
- método de pago Electronic check

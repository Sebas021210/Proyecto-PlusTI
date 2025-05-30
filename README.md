# 🕵️‍♂️ Detección de Fraude en Comercios Nuevos con LightGBM

Este proyecto tiene como objetivo construir un modelo de clasificación binaria que permita detectar transacciones fraudulentas, con especial enfoque en comercios recién afiliados.

## 📌 Descripción del problema

Detectar fraudes en comercios nuevos es un desafío por varias razones:
- Son comercios sin historial, por lo que los patrones normales aún no están bien definidos.
- Muchos fraudes ocurren durante los primeros días de operación.

En este contexto, se diseñaron métricas personalizadas y un enfoque de evaluación específico para priorizar la detección de fraudes en este subconjunto de datos.

## 🧠 Modelo

- Algoritmo: LightGBM
- Datos: Dataset tabular con información de transacciones, usuarios, fechas y comercios.
- División de datos: Train/Validation con enfoque estratificado.
- Comercios nuevos: Se consideran aquellos cuyo primer mes de operación (first_transaction_date).

## 🧪 Métricas de evaluación

Se implementaron métricas personalizadas para evaluar el modelo exclusivamente sobre comercios nuevos:
- Recall en nuevos comercios: qué tan bien detecta fraudes reales.
- Precision en nuevos comercios: qué tan confiables son las alertas.
- F1 Score en nuevos comercios: equilibrio entre precision y recall.

### 📈 Resultados obtenidos (en el subconjunto de comercios nuevos):

| Métrica   | Valor  |
| --------- | ------ |
| Recall    | 0.7071 |
| Precision | 0.9722 |
| F1 Score  | 0.8187 |

## ⚙️ Tecnologías utilizadas

- Python
- LightGBM
- Pandas / NumPy / Scikit-learn

## 📌 Notas
Este README es una introducción breve. El análisis completo, decisiones de diseño y validación se incluirán en el reporte formal del proyecto.

# Detección de Fraude en Transacciones con Tarjeta de Crédito

## Descripción del proyecto y objetivos

Este proyecto aborda el análisis y detección de transacciones fraudulentas en tarjetas de crédito utilizando técnicas de Machine Learning. El objetivo principal es identificar patrones que permitan distinguir entre transacciones legítimas y fraudulentas, contribuyendo así a la prevención de fraudes financieros.

---

## Dataset utilizado y justificación de selección

El dataset utilizado es el **Credit Card Fraud Detection** de [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). Contiene 284,807 transacciones realizadas en septiembre de 2013 por titulares europeos de tarjetas, de las cuales solo 492 son fraudes. Este dataset es ampliamente utilizado por la comunidad científica debido a su realismo, tamaño y la presencia de un fuerte desbalance de clases, lo que lo convierte en un excelente caso de estudio para problemas reales de detección de fraude.

---

## Problema de negocio abordado

La detección temprana y precisa de fraudes en transacciones con tarjetas de crédito es fundamental para evitar pérdidas económicas y proteger a los clientes. El principal desafío es identificar la mayor cantidad de fraudes posible, minimizando tanto los falsos negativos (fraudes no detectados) como los falsos positivos (transacciones legítimas marcadas como fraude).

---

## Metodología aplicada paso a paso

1. **Carga y exploración de los datos**: Inspección inicial, análisis de estructura y desbalance de clases.
2. **Análisis exploratorio de datos (EDA)**: Visualización de variables clave, identificación de patrones, outliers y correlaciones.
3. **Preprocesamiento**: Escalado de la variable `Amount`, separación de conjuntos de entrenamiento y prueba, revisión de valores nulos.
4. **Modelado**: Entrenamiento de dos modelos de clasificación (Logistic Regression y Random Forest).
5. **Evaluación**: Comparación de desempeño mediante métricas como accuracy, precision, recall, F1-score y matriz de confusión.
6. **Conclusiones y recomendaciones**: Análisis de resultados, identificación de limitaciones y propuestas de mejora.

---

## Algoritmos de ML utilizados y justificación

- **Logistic Regression:**  
  Elegido por su simplicidad, interpretabilidad y utilidad como modelo base para comparar con otros algoritmos más complejos.
- **Random Forest:**  
  Seleccionado por su capacidad para manejar datos desbalanceados, capturar relaciones no lineales y ofrecer una mejor identificación de fraudes a través de un mayor recall.

---

## Principales hallazgos y patrones identificados

- El dataset está altamente desbalanceado: menos del 0.2% de las transacciones son fraudes.
- La mayoría de los montos de transacción son bajos, pero existen valores atípicos significativos.
- Random Forest supera a Logistic Regression en la detección de fraudes (mayor recall), aunque a costa de más falsos positivos.
- No se detectaron valores nulos y la mayoría de variables están transformadas para proteger la confidencialidad.

---

## Enlaces al notebook en Google Colab

- [Haz clic aquí para ver y ejecutar el notebook en Google Colab](ENLACE_PUBLICO_COLAB_AQUI)

---

## Instrucciones para reproducir el análisis

1. Descarga el dataset desde [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) y súbelo a tu Google Drive, siguiendo la estructura indicada en el notebook.
2. Abre el notebook en Google Colab desde el enlace proporcionado.
3. Modifica la ruta del archivo en la celda de carga de datos si es necesario.
4. Ejecuta todas las celdas secuencialmente.
5. Se recomienda tener conocimientos básicos de Python y librerías como pandas, scikit-learn, matplotlib y seaborn.

---

## Conclusiones principales y recomendaciones

- El modelo Random Forest es más efectivo para identificar fraudes, pero el tratamiento del desbalance de clases sigue siendo un reto importante.
- Se recomienda experimentar con técnicas como sobremuestreo (SMOTE), submuestreo o ajuste de pesos de clase para mejorar los resultados.
- Es fundamental priorizar el recall para minimizar fraudes no detectados, aunque esto pueda aumentar los falsos positivos.
- La metodología utilizada puede adaptarse y escalarse para otros problemas de clasificación desbalanceada en el sector financiero.

---

## Limitaciones identificadas del análisis

- El dataset es anónimo y real, pero carece de variables categóricas que podrían aportar contexto adicional.
- No se aplicaron técnicas avanzadas de balanceo de clases ni optimización de hiperparámetros.
- El análisis está limitado a dos modelos clásicos; podrían explorarse modelos más avanzados como XGBoost o redes neuronales.
- El performance real en producción puede variar si los datos futuros difieren del patrón histórico analizado.

---

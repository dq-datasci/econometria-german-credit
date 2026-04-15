# Análisis Econométrico: German Credit Scoring 💳🏛️

Este proyecto desarrolla un sistema de **Credit Scoring** aplicando un rigor econométrico progresivo sobre el *German Credit Dataset*. A diferencia de un enfoque de "caja negra", este análisis se centra en la **inferencia causal** y en la justificación teórica de los modelos de elección discreta para la toma de decisiones financieras.

## 🎯 Objetivo del Proyecto
Evaluar los determinantes socioeconómicos que influyen en la probabilidad de que un cliente caiga en impago (*default*), comparando las limitaciones del Modelo de Probabilidad Lineal (MPL) frente a la robustez de los modelos **Logit** y **Probit**.

## 🧠 Marco Teórico: Las 5 C's del Crédito
La selección de variables se fundamentó en los pilares financieros del riesgo:
* **Capacidad de pago**: Monto, Plazo y Carga de la cuota.
* **Carácter (Historial)**: Antecedentes críticos y experiencia crediticia.
* **Capital y Colateral**: Reservas de ahorro y propiedad de bienes raíces.

## 📈 Hallazgos Clave e Insights de Negocio
* **La Paradoja del Historial Crítico**: Se descubrió que en el contexto alemán, los clientes con historial "Crítico" tienen una tasa de impago del **17.1%**, notablemente inferior al **35.4%** de aquellos con historial "Sano". Esto sugiere que la experiencia crediticia previa es un mitigante de riesgo superior a la incertidumbre de un cliente sin antecedentes.
* **Falla Estructural del MPL**: Mediante una "prueba de estrés", se demostró que el modelo lineal genera probabilidades imposibles (de **-22%** y **110%**), lo que justifica el uso de estimaciones por Máxima Verosimilitud.
* **Efectos Marginales (AME)**: Tener la cuenta corriente en negativo es el factor de riesgo más potente, incrementando la probabilidad de default en un **18.43%** en promedio para toda la población estudiada.

## 🛠️ Stack Tecnológico y Reproducibilidad
Este proyecto utiliza **R** y **RStudio** bajo un esquema de entorno aislado (`renv`) para garantizar la reproducibilidad.

**Librerías principales:**
* `dplyr` & `tidyr`: Manipulación y limpieza.
* `ggplot2` & `corrplot`: Análisis visual.
* `stargazer`: Reporte de tablas con formato académico.
* `margins`: Cálculo de Efectos Marginales Promedio (AME).
* `car` & `lmtest`: Diagnósticos de multicolinealidad y heterocedasticidad.

### Instrucciones para Reproducir
1. Clonar el repositorio.
2. Abrir el archivo `econometria-german-credit.Rproj`.
3. Ejecutar `renv::restore()` para instalar las librerías necesarias.
4. Ejecutar **Knit** en el archivo `.Rmd` para generar el reporte final.

---
**Autor:** [dqdatasci](https://github.com/dqdatasci)
# Turismo Inteligente: Modelos de IA para Análisis y Visualización

Este repositorio contiene el código fuente, los notebooks de trabajo y modelado y los recursos del **Trabajo Final de Grado (TFG)** del Grado en Ciencia de Datos Aplicada de la **Universitat Oberta de Catalunya (UOC)**.

**Autor:** Daniel Oñoro Segura  
**Convocatoria:** Enero 2026  
**Universitat Oberta de Catalunya (UOC)**

---

## Descripción del Proyecto

El objetivo de este proyecto es desarrollar y evaluar un sistema de análisis y visualización basado en técnicas de ciencia de datos que permita caracterizar perfiles de turistas y realizar predicciones de flujos turísticos por comunidad autónoma de destino y país de residencia, integrando los resultados en un dashboard interactivo en Power BI para apoyar la toma de decisiones en el ámbito del turismo inteligente.

El sistema implementa un flujo *End-to-End*:
1.  **Ingeniería de Datos:** Procesamiento de ficheros de gran volumen (>30GB) utilizando **DuckDB** para superar las limitaciones de memoria local.
2.  **Machine Learning:**
    * **Clustering:** Estudio de segmentación de perfiles turísticos mediante modelos **K-Means**, **HDBSCAN** y **GMM**, con sus respectivas métricas de evaluación.
    * **Forecasting:** Estudio de predicción de demanda turística comparando modelos **ARIMA**, **Prophet**, **LSTM** y **Baseline Estacional** con sus respectivas métricas de evaluación..
3.  **Visualización:** Integración de resultados en un Dashboard interactivo de **Power BI**.

---

## Tecnologías y Metodología

1. Procesamiento de Big Data (DuckDB)
Se optó por la librería DuckDB en Python para ingerir, transformar y filtrar el dataset de 239 millones de registros del INE, realizando agregaciones y limpiezas estructurales previas al modelado en Python.

2. Clustering (Segmentación)
Se identificaron 12 perfiles de comportamiento turístico.

* Técnica: Reducción de dimensionalidad mediante PCA (10 componentes) para capturar la estructura latente y mitigar el ruido de variables categóricas, seguido de GMM (Gaussian Mixture Models).
* Validación: Métricas de silueta, criterio BIC e interpretabilidad de negocio.

3. Forecasting (Predicción)
Debido a la ruptura estructural del COVID-19, se entrenaron modelos con series cortas (2022-2024).

* Modelos: ARIMA vs. Baseline Naïve en función de la ruta.
* Validación: RSME, MAPE y visual.

## Visualización (Power BI)
[El resultado final alimenta un cuadro de mando que permite filtrar predicciones y cruzar perfiles de viajeros accesible clicando este hipervínculo](https://app.powerbi.com/view?r=eyJrIjoiYTgwZDY2YWEtMzI4NC00YzUyLWFkMzctN2Y1OWI4ODM4ODdiIiwidCI6ImFlYzc2MmU0LTNkNTQtNDk1ZS1hOGZlLTQyODdkY2U2ZmU2OSIsImMiOjh9).

---

Instalación y Reproducibilidad

Debido al tamaño de los datos originales del INE (33GB), el fichero original no se incluyen en este repositorio, sino la version de 48 MB tratada mediante el notebook (comprimida en .rar).

Para reproducir, descargar los notebooks y los datos en una misma carpeta y ejecutar los notebooks por el orden numérico.

---

Contacto: Daniel Oñoro Segura - www.linkedin.com/in/daniel-oñoro-segura-9143b42a0

# Miami-Housing-ML-Prediction

# Proyecto: Predicción de Precios Inmobiliarios en Miami

### 1. Introducción y Objetivos
El mercado inmobiliario de Miami se caracteriza por una alta complejidad, donde factores como la ubicación geográfica (distancia al océano, subcentros) y la calidad estructural interactúan de forma no lineal para definir el valor de una propiedad.

El objetivo principal de este proyecto es desarrollar un sistema de **Machine Learning** capaz de predecir con precisión el precio de venta (`SALE_PRC`). Más allá de minimizar el error, buscamos interpretar *qué* hace valiosa a una vivienda, comparando la eficacia de modelos econométricos clásicos frente a algoritmos avanzados de Inteligencia Artificial.

### 2. Hoja de Ruta del Proyecto (Workflow)
A lo largo de este estudio, implementaremos un flujo de trabajo riguroso de Ciencia de Datos dividido en cuatro fases:

1.  **Exploración y Preprocesamiento:**
    * **Análisis del Target:** Detección de asimetría en el precio y aplicación de transformación logarítmica ($log(1+y)$).
    * **Estructura Latente:** Uso de PCA y t-SNE para visualizar la separabilidad de los datos.
    * **Limpieza:** Escalado de variables (`StandardScaler`) y codificación (`One-Hot Encoding`).

2.  **Fase 1: Línea Base (Modelos Lineales y Basados en Instancias):**
    * Evaluación de **Regresión Lineal (OLS)** y **LASSO** para establecer un *baseline*.
    * Implementación de **K-Nearest Neighbors (KNN)** para comprobar si la "similitud local" supera a la linealidad.

3.  **Fase 2: Modelos No Lineales Avanzados:**
    * **Ensemble Learning:** Entrenamiento de **Random Forest** (Bagging) y **Gradient Boosting** (Boosting) para capturar patrones complejos y reducir el error.
    * **Deep Learning:** Prueba de concepto con una Red Neuronal (**MLP Regressor**) para datos tabulares.
    * **Optimización:** Ajuste de hiperparámetros mediante `RandomizedSearchCV` con validación cruzada ($k=5$).

4.  **Evaluación e Interpretación:**
    * Comparativa final usando métricas robustas: **RMSE** (error en dólares) y **$R^2$** (varianza explicada).
    * Análisis de **Importancia de Variables** para entender los drivers del mercado.

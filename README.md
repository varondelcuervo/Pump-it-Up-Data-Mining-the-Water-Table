# Pump-it-Up-Data-Mining-the-Water-Table

## Predicción del Estado de Pozos de Agua — Proyecto de Machine Learning

### Descripción del Proyecto

Este proyecto tiene como objetivo predecir el **estado operativo de los pozos de agua** (funcional, no funcional o en reparación) a partir de variables demográficas, geográficas y técnicas.

A través de un proceso completo de **preprocesamiento, modelado y evaluación**, se implementaron distintas técnicas de Machine Learning para comparar el rendimiento de varios algoritmos y determinar el modelo más eficiente.

---

### Tecnologías y Librerías Utilizadas

* **Python 3.x**
* **pandas**, **numpy** — Manipulación y análisis de datos
* **scikit-learn** — Modelos de machine learning, pipelines, métricas y GridSearchCV
* **matplotlib**, **seaborn** — Visualización de datos
* **imblearn** — Aplicación de SMOTE para balanceo de clases

---

### Flujo del Proyecto

1. **Carga y exploración de datos**

   * Revisión de variables numéricas y categóricas
   * Identificación de valores nulos y desbalance de clases

2. **Preprocesamiento**

   * Imputación de valores faltantes (media para numéricas, moda para categóricas)
   * Estandarización con `StandardScaler`
   * Codificación de variables categóricas con `OneHotEncoder`
   * Integración mediante `ColumnTransformer` y `Pipeline`
   * Aplicación de **SMOTE** para balancear las clases minoritarias

3. **Entrenamiento de modelos**

   * **DecisionTreeClassifier**
   * **RandomForestClassifier**
   * **GaussianNB**
   * **GradientBoostingClassifier**

4. **Optimización de hiperparámetros**

   * Uso de `GridSearchCV` con validación cruzada
   * Métrica de optimización: **recall**, priorizando la correcta identificación de pozos no funcionales

5. **Evaluación y resultados**

   * Cálculo de **recall**, **precision**, **f1-score** y **accuracy**
   * Análisis de la matriz de confusión
   * Comparación entre modelos para identificar el de mejor desempeño

---

### Resultados Principales

* Los modelos **Random Forest** y **Gradient Boosting** obtuvieron los mejores resultados en recall y F1-score.

---

### Conclusiones

* El **pipeline de preprocesamiento y balanceo** fue clave para mejorar la calidad del entrenamiento.
* **SMOTE** ayudó a mitigar el sesgo hacia las clases mayoritarias.
* Los modelos basados en árboles (RandomForest y GradientBoosting) mostraron mejor desempeño que modelos probabilísticos como Naive Bayes.
* El modelo final puede servir como base para un sistema de monitoreo y priorización de mantenimiento de pozos.

---

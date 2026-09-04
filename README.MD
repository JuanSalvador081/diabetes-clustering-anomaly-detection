# Diabetes Clustering & Anomaly Detection

Análisis no supervisado sobre datos de salud pública para identificar segmentos de pacientes y detectar comportamientos atípicos (outliers) en indicadores clínicos, usando el dataset [BRFSS 2021 Diabetes Health Indicators](https://raw.githubusercontent.com/Zephyrodes/Datasets/main/diabetes_binary_5050split_health_indicators_BRFSS2021.csv).

## Qué hace este proyecto

- **Segmentación de pacientes** mediante K-Means y clustering jerárquico, evaluando el número óptimo de clústeres con Silhouette Score.
- **Detección de anomalías/outliers** con DBSCAN, identificando registros que no encajan en ningún patrón de comportamiento esperado.
- **Reducción de dimensionalidad** con PCA y t-SNE para visualizar los clústeres en 2D y validar su separación.
- **Validación cruzada de clústeres** contra la variable objetivo (`Diabetes_binary`) para interpretar qué combinaciones de indicadores caracterizan a cada grupo.

## Técnicas y herramientas

- **Clustering:** K-Means, Clustering Jerárquico (linkage/dendrograma), DBSCAN
- **Reducción de dimensionalidad:** PCA, t-SNE
- **Validación:** Silhouette Score, Índice de Dunn
- **Librerías:** Scikit-learn, SciPy, Pandas, NumPy, Matplotlib, Seaborn

## Por qué DBSCAN

A diferencia de K-Means, DBSCAN no asume clústeres de forma esférica ni un número fijo de grupos: identifica automáticamente registros que se alejan de la densidad general de los datos. Esto lo hace especialmente útil para **detección de patrones anómalos** en escenarios donde no se conoce de antemano qué comportamientos son atípicos — un enfoque directamente aplicable a la identificación de anomalías fuera del dominio de salud, como en análisis de fraude.

## Autor

Juan Salvador Londoño Cortés — [github.com/JuanSalvador081](https://github.com/JuanSalvador081)
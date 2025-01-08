# Water Quality and Potability

### Descripción del proyecto

El objetivo de este proyecto es evaluar y predecir la potabilidad del agua en función de los atributos de calidad del agua. Puede utilizarse para evaluar la seguridad y la idoneidad de las fuentes de agua para el consumo humano, tomar decisiones informadas sobre el tratamiento del agua y garantizar el cumplimiento de los estándares de calidad del agua. Este conjunto de datos es valioso para la evaluación de la calidad del agua, la planificación del tratamiento del agua y para garantizar la seguridad del suministro de agua potable. Puede ser utilizado por plantas de tratamiento de agua, agencias ambientales e investigadores para tomar decisiones basadas en datos sobre la calidad y potabilidad del agua.

### Fuentes de dato

La base de datos utilizada para este proyecto se encuentra en el archivo "water_potability.csv", conteniendo registros de muestras de agua.

### Herramientas

- Python - EDA y modelamiento

### Limpieza / preparación de datos

En la fase inicial de preparación de datos, se hizo lo siguiente:
1. Carga de data e inspección.
2. Verificación del balance de datos de variable objetivo.
3. Validación de datos duplicados.
4. Validación de datos nulos e imputación con Iterative Imputer.
5. Tratamiento de outliers con método Isolation Forest.
6. Análisis de correlación de variables.
7. Se hizo un oversampling de la variable objetivo con el método SMOTE.

### Modelamiento de datos

Se probaron diversos escaladores y modelos de Machine Learning para validar el mejor rendimiento para el proyecto.

- Escaladores: Standard Scaler, Min Max Scaler, Robust Scaler, Quantile Transformer y Power Transformer.
- Modelos: Regresión Logística, , SVM, XGBoost, Random Forest y KNN.

### Resultados

Los resultados de este proyecto son:
1. El modelo con mejor rendimiento fue utilizando un escalador Power Transformer y luego un modelo de Random Forest.
2. Para este proyecto la métrica de mayor relevancia es el recall para 'no potable', ya que es crucial poder verdaderamente predecir estos casos.
3. Se optimizaron los hiperparámetros del modelo con los valores: {'max_depth': None, 'min_samples_leaf': 1, 'min_samples_split': 2, 'n_estimators': 200}.
4. Se obtuvo un recall = 0.69.
5. Se obtuvo una precisión = 0.70.

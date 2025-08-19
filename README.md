# Desafío Telecom X Latam Parte 2: Modelado Predictivo de Evasión de Clientes (Churn)

¡Bienvenido al repositorio de la Parte 2 del Desafío Telecom X! Este proyecto forma parte del curso de Data Science de Alura Latam y se centra en la aplicación de conceptos de estadística, regresión lineal y machine learning para construir un modelo predictivo de evasión de clientes (churn) en una empresa de telecomunicaciones.

## 🎯 Propósito del Análisis y Modelado

El objetivo principal de esta segunda parte es continuar el trabajo de la Parte 1 (ETL y EDA) para:

* **Preparar y separar los datos** adecuadamente para el modelado predictivo.
* **Construir un modelo de Machine Learning** capaz de predecir la probabilidad de que un cliente cancele su servicio.
* **Evaluar el rendimiento del modelo** utilizando métricas clave.
* **Derivar conclusiones estratégicas** a partir del modelo para ayudar a Telecom X a anticipar y mitigar la pérdida de clientes.

Este proyecto busca proporcionar a Telecom X una herramienta para identificar clientes en riesgo y desarrollar estrategias de retención proactivas y dirigidas.

## 📁 Estructura del Proyecto y Organización de Archivos

Este repositorio contiene:

* `Desafío_Telecom_X_Análisis_de_Evasión_de_Clientes.ipynb` (o el nombre que le hayas dado a tu cuaderno de la Parte 2): El cuaderno Jupyter/Colab principal donde se realiza la preparación de datos, el modelado predictivo y la evaluación.
* **Datos Originales:** Los datos se obtienen de la misma API utilizada en la Parte 1, y se procesan internamente en el cuaderno para asegurar la continuidad. No se incluyen archivos de datos CSV directamente en este repositorio.

La estructura del código dentro del cuaderno está organizada en las siguientes secciones:

1.  **📌 Carga de Datos Pre-procesados:** Simulación de la carga de los datos limpios de la Parte 1, con el re-procesamiento inicial para asegurar la consistencia.
2.  **🔧 Preparación de Datos para Modelado:**
    * Eliminación de columnas irrelevantes.
    * Definición de la variable objetivo (churn) y las características (features).
    * Identificación de columnas numéricas y categóricas.
    * Verificación de la proporción de clases (balance de churn).
    * Configuración del `ColumnTransformer` para el escalado numérico (`StandardScaler`) y codificación One-Hot (`OneHotEncoder`) de variables categóricas.
3.  **📊 Separación de Datos (Train/Test Split):** División del dataset en conjuntos de entrenamiento y prueba, asegurando la estratificación de la variable objetivo.
4.  **⚙️ Construcción y Evaluación del Modelo:**
    * Creación de un `Pipeline` de Machine Learning (preprocesamiento + `LogisticRegression`).
    * Entrenamiento del modelo con los datos de entrenamiento.
    * Realización de predicciones en el conjunto de prueba.
    * Evaluación del modelo mediante `classification_report`, `confusion_matrix` y la curva ROC (`roc_curve`, `auc`).
5.  **📄 Conclusiones Estratégicas:** Un informe detallado con el rendimiento del modelo, los factores clave identificados y las implicaciones estratégicas para Telecom X.

## 📈 Ejemplos de Gráficos e Insights Obtenidos

El modelado predictivo y su evaluación proporcionan insights cruciales:

* **Matriz de Confusión:** Muestra cuántas predicciones fueron correctas e incorrectas para cada clase (clientes que cancelan vs. no cancelan), ayudando a entender los errores del modelo (Falsos Positivos y Falsos Negativos).
    * ![Matriz de Confusión](https://placehold.co/300x200/007bff/ffffff?text=Matriz+de+Confusión)
    * *Insight Clave:* Identificación de la capacidad del modelo para detectar correctamente a los clientes que realmente cancelarán (Recall para Churn).

* **Curva ROC (Receiver Operating Characteristic):** Visualiza la capacidad del modelo para distinguir entre las clases, y el área bajo la curva (AUC-ROC) cuantifica el rendimiento general.
    * ![Curva ROC](https://placehold.co/300x200/28a745/ffffff?text=Curva+ROC)
    * *Insight Clave:* Un AUC-ROC cercano a 1 indica un excelente rendimiento del modelo.

* **Reporte de Clasificación:** Proporciona métricas como Precisión, Recall y F1-Score para cada clase, ofreciendo una visión detallada del rendimiento del modelo.

Las conclusiones estratégicas detalladas en el notebook final resaltan la importancia de factores como la antigüedad del cliente, el tipo de contrato mensual, la falta de servicios adicionales y el método de pago electrónico como los principales impulsores del churn.

## 🚀 Instrucciones para Ejecutar el Notebook

Para replicar y explorar este análisis de modelado predictivo en tu propio entorno:

1.  **Accede a Google Colab:**
    * Abre tu navegador y ve a [Google Colab](https://colab.research.google.com/).
2.  **Abrir el Cuaderno:**
    * Haz clic en `Archivo` (File) -> `Abrir cuaderno` (Open notebook).
    * En la ventana emergente, selecciona la pestaña `GitHub`.
    * Pega la URL de este repositorio. **Importante:** Asegúrate de reemplazar `https://github.com/tu-usuario/Desafio-TelecomX-Latam-Parte2` con la URL real de **tu propio repositorio** en GitHub para acceder al cuaderno.
    * Selecciona el archivo `Desafío_Telecom_X_Análisis_de_Evasión_de_Clientes.ipynb` (o el nombre que le hayas dado) y haz clic en `Abrir`.
3.  **Ejecutar las Celdas:**
    * Una vez que el cuaderno esté abierto en Colab, puedes ejecutar cada celda de forma secuencial haciendo clic en el botón de "Play" al lado de cada celda, o puedes ejecutar todas las celdas yendo a `Entorno de ejecución` (Runtime) -> `Ejecutar todas` (Run all).

**¡Esperamos que este modelo predictivo sea una herramienta valiosa para que Telecom X reduzca la evasión de clientes y mejore la lealtad!**


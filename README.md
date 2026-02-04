# Predicción de Precios de Coches Usados
Desarrollo de un modelo de Machine Learning para la tasación automática de vehículos de segunda mano.

📝 1. Introducción y Contexto
La estimación del precio de un coche de segunda mano es un reto complejo debido a la alta variabilidad de factores involucrados. Elementos como la marca, el modelo, el kilometraje, el tipo de combustible y la antigüedad interactúan de forma no lineal para determinar el valor de mercado de un vehículo.

Este proyecto nace de la necesidad de automatizar este proceso. Mediante el análisis de datos históricos de ventas, buscamos transformar información bruta en una herramienta inteligente capaz de sugerir precios competitivos en portales de compraventa o realizar tasaciones instantáneas con base científica.

🎯 2. Objetivos del Proyecto
El objetivo principal es desarrollar e implementar un modelo de aprendizaje supervisado robusto y preciso.

Meta Técnica: Lograr un Error Absoluto Medio (MAE) inferior a 3,000 € en el conjunto de validación.

Meta de Negocio: Generar predicciones fiables que puedan integrarse en sistemas de tasación automática o recomendaciones de precios en tiempo real para usuarios finales.

📊 3. Alcance y Limitaciones
Alcance
Procesamiento de un dataset con 4,960 registros de entrenamiento y 2,672 de prueba.

Análisis de 11 variables clave, incluyendo datos técnicos (consumo, tipo de motor, tasa) y comerciales (marca, modelo, año).

Evaluación de múltiples algoritmos de regresión para identificar el de mejor desempeño.

Limitaciones
El modelo se basa en datos históricos; factores externos repentinos (cambios legislativos, crisis económicas) podrían no estar reflejados.

Modelos de coches catalogados como "poco frecuentes" podrían tener una precisión menor debido a la falta de representatividad en los datos de entrenamiento.

⚙️ 4. Metodología
El proyecto sigue un flujo de trabajo estándar de Ciencia de Datos:

Exploración de Datos (EDA): Identificación de valores nulos (especialmente en tipo_cambio y consumo) y análisis de distribuciones sesgadas.

Preprocesamiento:

Imputación: Manejo de datos faltantes detectados en las fases iniciales.

Codificación: Transformación de variables categóricas (como marca y modelo) mediante técnicas como OneHotEncoding.

Escalado: Normalización de variables numéricas para optimizar el entrenamiento.

Modelado: Se evalúan diversos algoritmos disponibles en la librería Scikit-learn, tales como:

Regresión Lineal.

Bosques Aleatorios (Random Forest).

Gradient Boosting.

Redes Neuronales (MLPRegressor).

Validación: Uso de métricas de error (MAE, RMSE, R²) para asegurar que se cumple el umbral de calidad establecido.

🏆 5. Resultados Esperados
Modelo de Alta Precisión: Una herramienta capaz de predecir el precio con un margen de error controlado (MAE < 3,000 €).

Pipeline de Datos: Un sistema de procesamiento que permite transformar datos de un coche nuevo en un vector de entrada para el modelo.

Insights del Mercado: Identificación de cuáles son las variables que más impactan en la depreciación de un vehículo.
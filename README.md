# parcial

Este proyecto consiste en el desarrollo completo (full stack) de una aplicación móvil Android para predecir el clima (temperatura promedio del día siguiente) en Bucaramanga. Se basa en datos meteorológicos reales obtenidos desde la API gratuita de Open-Meteo.

Fases del Proyecto:

Recolección de Datos (Google Colab)

Fuente: Open-Meteo API (https://open-meteo.com/)

Datos descargados: temperatura máxima, mínima, precipitación diaria, velocidad del viento.

Periodo: 2019-2024.

Ubicación: Bucaramanga (lat: 7.1254, lon: -73.1198)

Exploración y Preprocesamiento

Limpieza de datos: manejo de valores nulos.

Creación de nuevas variables: 2025, 05, temperatura media.

Definición de variable objetivo: temperatura media del día siguiente.

Entrenamiento del Modelo (Machine Learning)

Modelo: RandomForestRegressor (scikit-learn)

Variables de entrada: temperatura_max, temperatura_min, precipitación, viento, mes, día.

Métricas de evaluación: RMSE, MAE, R².

Guardado del modelo entrenado: modelo_clima.pkl + features_clima.pkl (usado en backend).

Backend (API REST con Flask)

El backend (Flask) cargará el modelo entrenado.

Expondrá un endpoint POST /predict que recibirá parámetros climáticos y devolverá la predicción.

La app móvil consumirá esta API.

App Android (Android Studio)

Interfaz para ingresar datos meteorológicos.

Envío de solicitud POST a la API Flask.

Muestra de la predicción del clima en pantalla.

Archivos clave del proyecto:

clima_bucaramanga.csv: dataset original obtenido desde Open-Meteo

modelo_clima.pkl: modelo de predicción guardado (RandomForest)

features_clima.pkl: lista de columnas usadas para el modelo

app.py: archivo Flask para servir el modelo como API REST

Requisitos Python (Colab / Backend):

pandas

numpy

scikit-learn

joblib

flask (para backend)

requests (para Open-Meteo API)

Este proyecto combina machine learning, backend API y desarrollo móvil como un caso práctico de aplicación de inteligencia artificial en análisis de datos meteorológicos.

Autor: [Jaime Rueda, Andres Muñoz]
Fecha: Mayo 2025

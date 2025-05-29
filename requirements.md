📁 ESTRUCTURA DE CARPETAS DEL PROYECTO CLIMA APP

ClimaApp/
├── backend/
│ ├── app.py ← API Flask para predicción
│ ├── modelo_clima.pkl ← Modelo entrenado
│ ├── features_clima.pkl ← Lista de variables (features)
│ ├── requirements.txt ← Dependencias para backend
│
├── data/
│ ├── clima_bucaramanga.csv ← Dataset con datos reales
│
├── notebooks/
│ ├── entrenamiento_modelo.ipynb ← Cuaderno Colab para EDA + modelado
│
├── android_app/
│ ├── (Archivos del proyecto en Android Studio)
│
├── README_ClimaApp.txt ← Documentación del proyecto (descripción general)

—

📦 requirements.txt (para backend)

Este archivo permite instalar las dependencias con pip:

Flask
scikit-learn
pandas
numpy
joblib

Contenido del archivo requirements.txt:

Flask==2.2.5
scikit-learn==1.3.0
pandas==2.0.3
numpy==1.24.4
joblib==1.3.2

(Usa pip install -r requirements.txt para instalar todo en tu entorno virtual)

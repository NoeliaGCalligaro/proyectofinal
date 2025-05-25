# Proyecto Final - Soy Henry - Data Analytics

Este proyecto corresponde al trabajo final del bootcamp de Data Analytics de Soy Henry. El objetivo es realizar un análisis de datos de compras y ventas del año 2016, aplicando técnicas de exploración, limpieza y modelado con Python.

## 📁 Estructura del proyecto

- `proyecto_final.ipynb`: Notebook principal con el análisis completo.
- `*.csv`: Archivos con los datos utilizados para el análisis.
- `.gitignore`: Configurado para excluir archivos innecesarios del repositorio.
- `requirements.txt`: Lista de bibliotecas necesarias para ejecutar el proyecto.
- `nanclajecloud` Archivo relacionado con la configuración o integración en entorno cloud



> ⚠️ **Recomendación:** Mover los archivos `.csv` a una carpeta `data/` y excluir esa carpeta del repositorio para mantenerlo liviano.

## 📊 Datos utilizados

- `2017PurchasePricesDec.csv`
- `BegInvFINAL12312016.csv`
- `EndInvFINAL12312016.csv`
- `InvoicePurchases12312016.csv`
- `PurchasesFINAL12312016.csv`
- `SalesFINAL12312016.csv`
- `data_final2.xlsx`

## 🧪 Tecnologías y librerías utilizadas

- Python 3.13 (o compatible)
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Category Encoders

## ▶️ Cómo ejecutar el proyecto

1. Clonar este repositorio:
   ```bash
   git clone https://github.com/NoeliaGCalligaro/proyectofinal.git
   cd proyecto final 

2. Crear y activar un entorno virtual:
   python -m venv venv
   # Activar en Windows
   .\venv\Scripts\activate
   # Activar en Mac/Linux
   source venv/bin/activate



3. Instalar las dependencias:

    pip install -r requirements.txt


📈 Contenido del análisis
1. EDA Inicial
Exploración preliminar de los datos para comprender su estructura, tipos, y calidad.

Análisis de valores faltantes, estadísticas descriptivas de variables numéricas y categóricas.

Visualizaciones básicas (boxplots, histogramas, gráficos de dispersión) para detectar outliers y distribuciones.

Identificación inicial de variables relevantes para el análisis posterior.

2. ETL (Extracción, Transformación y Carga)
Integración y unión de los diferentes datasets para formar una base unificada.

Limpieza avanzada: tratamiento de valores faltantes con técnicas de imputación y modelos predictivos (Random Forest con encoding mixto).

Normalización y codificación de variables categóricas, incluyendo Target Encoding para variables de alta cardinalidad y OneHot Encoding para variables con pocas categorías.

Generación de nuevas variables derivadas para enriquecer el análisis.

Preparación final del dataset listo para análisis profundos y modelado.

3. EDA Final
Análisis más detallado y segmentado basado en el dataset limpio y completo.

Visualizaciones avanzadas para evaluar desempeño y comportamiento de compras y ventas por proveedor, tienda y otras dimensiones.

Gráficos de tendencias temporales para identificar patrones estacionales o cambios relevantes durante el año.

Evaluación y validación de los resultados de la imputación y modelado, con métricas y gráficos que confirman la calidad del procesamiento.
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



📈 Contenido de Anclaje_cloud.ipynb
☁️ ANCLAJE CLOUD - CARGA Y CONFIRMACIÓN DE DATOS EN BIGQUERY

👉 1. IMPORTACIÓN DE LIBRERÍAS
📌 Se importa pandas como librería base.

👉 2. DEFINICIÓN DE NUEVOS DATOS A CARGAR
📌 Se generan listas con datos simulados o nuevos para cargar en la base de datos.
  Ejemplos:
  - datos_new_data1 → Producto
  - datos_new_data2 → Inventario inicial
  - datos_new_data3 → Inventario final
  - datos_new_data4 → Compras
  - datos_new_data5 → Detalle de compras
  - datos_new_data6 → Ventas

👉 3. CARGA DE DATOS A BIGQUERY
📌 Se utiliza la función cargar_datos_una_tabla para insertar datos en tablas específicas dentro del proyecto y dataset:
  - Proyecto: soy-henry-459003
  - Dataset: andes_insight
  Tablas afectadas:
  - Productos
  - Inventario_inicial
  - Inventario_final
  - Compras
  - Detalle_compras
  - Ventas

👉 4. CONFIRMACIÓN DE DATOS CARGADOS
📌 Se usa la función confirmar_nuevos_datos_cargados para verificar que los datos se hayan insertado correctamente en cada tabla

👉 5. ELIMINACIÓN DE DATOS CARGADOS
📌 Se eliminan los datos previamente insertados en cada tabla utilizando la función eliminar_datos_cargados_por_columna.
  Tablas afectadas:
  - Productos
  - Inventario_inicial
  - Inventario_final
  - Compras
  - Detalle_compras
  - Ventas

👉 6. CONFIRMACIÓN DE ELIMINACIÓN DE DATOS
📌 Validación con confirmar_nuevos_datos_cargados para asegurar que los registros eliminados ya no se encuentren en las tablas.

📈 Contenido de proyecto_final.ipynb
📥 FUENTE DE DATOS
Antes del proceso de ETL, se toman los datos directamente desde la base de datos andes_insight, donde se encuentra el dataset previamente cargado y listo para trabajar.

📈 ANALISIS GENERAL DEL DATASET
      👉 1. IMPORTAMOS LIBRERIAS
      👉 2. ABRIMOS DATASET
      👉 3. EDA - ANALISIS EXPLORATORIO DE DATOS EDA - INCIAL
           📌 A. Análisis Integral EDA  (dimension, columnas, tipo de columnas, nulos, estadísticas variables numericas, detalle de categóricas) 
           📌 B. Análisis de Columnas con alta variabilidad
           📌 C. Análisis de Columnas con valores númericos ceros
      👉 4. ETL - PROCESO DE EXTRACCION, TRANSFORMACION Y LIMPIEZA DE DATOS
           📌 A. Remplazamos valores nulos
           📌 B. Remplazamos valores equivalente a cero en columnas númericas, cuando es necesario
           📌 C. Cambiamos tipo de datos en variables catégoricas que se encuentran como númericas (Brand, Store,VendorNumber)
      👉 5. DETERMINAR STOCK OPTIMO
           📌 A. Definimos funcion de stock óptimo (Stock óptimo = Demanda diaria promedio × Tiempo de reposición promedio + Stock de seguridad) 
           📌 B. Determinamos tiempo de reposión, y determinar media y desviacion std del tiempo de reposición medio para cada IventoryID 
           📌 C. Determinamos demanda diaria, y determinar media y desviacion std de la demanda diaria para cada IventoryID
           📌 D. Unimos en una tabla Inventario Incial, Inventario Final, Tiempo de Reposición y Demanda Diaria
           📌 E. Estimamos tiempo de reposición para productos que no han sido comprados, y Estimar demanda diaria para productos que no han sido                         vendidos. La estimación la haremos con técnicas de Maching Learning (Random Forest).
           📌 F. Determinamos Demanda diaria media. Analizar si se utiliza la demanda diaria media obtenida con Maching Learning, o la función de                        demanda diaria media obtenida con la funcion: Demada Estimada =Inventario Inicial + Compras - Inventario Final
           📌 G  Determimos Stock Optimo y Demanda Estimada
           📌 H. Exportamos nueva tabla Stock Óptimo
      👉 6. EDA - ANALISIS EXPLORATORIO DE DATOS EDA - FINAL


## Autores
- **Amalia Granata** 
- **Jenny Ortiz** 
- **Luis Ladino** 
- **Noelia Calligaro** 

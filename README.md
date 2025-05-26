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


# 🧠 Proyecto Final - Optimización de Stock con Análisis de Datos en BigQuery y Python

Este repositorio contiene dos notebooks principales que conforman el proceso completo del proyecto:

- **📥 `Anclaje_cloud.ipynb`**: Encargado de la **carga, confirmación y eliminación de datos** en BigQuery.
- **📈 `proyecto_final.ipynb`**: Realiza el **análisis exploratorio, ETL y cálculo del stock óptimo**.

---

## ☁️ Anclaje en la Nube - `Anclaje_cloud.ipynb`

Este notebook se encarga de simular y cargar datos nuevos en BigQuery, así como su verificación y limpieza.

### 🔹 1. Importación de librerías
- Se importa `pandas` como librería base.

### 🔹 2. Definición de nuevos datos a cargar
- Generación de listas de datos simulados:
  - `datos_new_data1` → Producto
  - `datos_new_data2` → Inventario inicial
  - `datos_new_data3` → Inventario final
  - `datos_new_data4` → Compras
  - `datos_new_data5` → Detalle de compras
  - `datos_new_data6` → Ventas

### 🔹 3. Carga de datos en BigQuery
- Uso de `cargar_datos_una_tabla` para insertar datos en las tablas del dataset `andes_insight` del proyecto `soy-henry-459003`:
  - `Productos`
  - `Inventario_inicial`
  - `Inventario_final`
  - `Compras`
  - `Detalle_compras`
  - `Ventas`

### 🔹 4. Confirmación de datos cargados
- Verificación de los datos insertados con `confirmar_nuevos_datos_cargados`.

### 🔹 5. Eliminación de datos cargados
- Uso de `eliminar_datos_cargados_por_columna` para limpiar las tablas anteriores.

### 🔹 6. Confirmación de eliminación de datos
- Validación final para asegurar que los datos fueron correctamente eliminados.

---

## 📊 Análisis y Optimización de Stock - `proyecto_final.ipynb`

Este notebook toma los datos desde BigQuery y realiza todo el análisis para determinar el stock óptimo de productos.

### 🔹 0. Fuente de datos
- Conexión directa a la base de datos `andes_insight` luego del EDA.

### 🔹 1. Importación de librerías

### 🔹 2. Carga del dataset

### 🔹 3. EDA Inicial (Análisis Exploratorio de Datos)
- A. Análisis integral: dimensiones, tipos, nulos, estadísticas numéricas, categóricas.
- B. Columnas con alta variabilidad.
- C. Columnas con valores numéricos en cero.

### 🔹 4. ETL - Extracción, Transformación y Limpieza
- A. Reemplazo de valores nulos.
- B. Reemplazo de ceros en columnas numéricas, si corresponde.
- C. Conversión de tipos en variables categóricas (Brand, Store, VendorNumber).

### 🔹 5. Determinación de Stock Óptimo
- A. Fórmula: `Stock óptimo = Demanda diaria promedio × Tiempo de reposición promedio + Stock de seguridad`.
- B. Cálculo del tiempo de reposición y su desviación estándar por `InventoryID`.
- C. Cálculo de demanda diaria y su desviación estándar por `InventoryID`.
- D. Unión de tablas: Inventario Inicial, Final, Tiempo de Reposición y Demanda Diaria.
- E. Estimación con Machine Learning (Random Forest) para productos sin historial.
- F. Comparación entre demanda estimada por ML vs. fórmula tradicional.
- G. Determinación final de stock óptimo.
- H. Exportación de tabla `stock_óptimo`.

### 🔹 6. EDA Final
- Revisión final del estado del dataset después del procesamiento.

---



## Autores
- **Amalia Granata** 
- **Jenny Ortiz** 
- **Luis Ladino** 
- **Noelia Calligaro** 

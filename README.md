# Análisis del Comportamiento de Clientes - ConnectaTel

## 📊 Objetivo del Proyecto
Este proyecto tiene como objetivo principal evaluar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones en Latinoamérica. A través de la exploración, limpieza y análisis de datos, se busca construir un perfil estadístico de los clientes, detectar comportamientos atípicos, crear segmentos de clientes, identificar patrones de consumo, diseñar estrategias de retención y sugerir mejoras en los planes ofrecidos por la empresa. El análisis se centra en información registrada hasta el año 2024.

## 💾 Datasets Utilizados
Se utilizaron tres datasets principales para este análisis:
- **`plans.csv`**: Contiene información detallada sobre los planes actuales de ConnectaTel (precio, minutos incluidos, GB incluidos, costo por extra).
- **`users_latam.csv`**: Incluye datos de los clientes, como edad, ciudad, fecha de registro, plan contratado y estado de churn.
- **`usage.csv`**: Proporciona el detalle del uso real de los servicios por parte de los clientes (llamadas y mensajes).

## 📈 Etapas del Análisis Realizadas
El análisis se estructuró en las siguientes etapas clave:
1.  **Carga y Exploración de Datos**: Familiarización con la estructura de los datasets, carga correcta de archivos, revisión de columnas y tipos de datos, y detección de inconsistencias preliminares.
2.  **Identificación de Problemas de Calidad de Datos**: Revisión de valores nulos, detección de valores inválidos (sentinels) y estandarización de fechas para asegurar la coherencia y calidad de los datos.
3.  **Limpieza Básica de Datos**: Corrección de sentinels en variables numéricas y categóricas, así como manejo de fechas fuera de rango y justificación de decisiones sobre valores nulos.
4.  **Summary Statistics de Uso por Usuario**: Agregación de datos de uso por `user_id` para crear métricas clave de comportamiento (número total de mensajes, llamadas, minutos), y resumen estadístico de perfiles de usuario.
5.  **Visualización de Distribuciones y Outliers**: Creación de histogramas y boxplots para entender visualmente las distribuciones de variables clave (`age`, `cant_mensajes`, `cant_llamadas`, `total_minutos_llamada`) e identificación de outliers.
6.  **Segmentación de Clientes**: Clasificación de usuarios en grupos basados en su nivel de uso (`Bajo uso`, `Uso medio`, `Alto uso`) y edad (`Joven`, `Adulto`, `Adulto Mayor`), seguida de visualización de estas segmentaciones.
7.  **Insight Ejecutivo para Stakeholders**: Conclusiones accionables basadas en los hallazgos, abordando problemas de datos, segmentos valiosos, patrones de uso extremo y recomendaciones para mejorar la oferta de planes.

## 🚀 Cómo Ejecutar el Notebook
Para ejecutar este análisis, sigue estos pasos:
1.  **Si usas Google Colab:**
    - Abre el notebook en Google Colab.
    - Asegúrate de que los archivos `plans.csv`, `users_latam.csv`, y `usage.csv` estén accesibles en el entorno de Colab, preferiblemente en un directorio `/datasets/` o actualiza las rutas de archivo en la celda de carga de datos.
    - Ejecuta las celdas de código secuencialmente para replicar el análisis.
2.  **Si usas Jupyter Notebook (local):**
    - Clona o descarga este repositorio a tu máquina local.
    - Navega al directorio donde guardaste el notebook y los archivos de datos (`plans.csv`, `users_latam.csv`, `usage.csv`).
    - Abre una terminal en ese directorio y ejecuta `jupyter notebook`.
    - Abre el archivo `.ipynb` en tu navegador.
    - Asegúrate de que los archivos CSV estén en el mismo directorio que el notebook o actualiza las rutas de archivo en la celda de carga de datos.
    - Ejecuta las celdas de código secuencialmente.
  
## 📝 Guía de Reproducción
- **Entorno**: Google Colab o Jupyter Notebook (Python 3.x)
- **Librerías**: `pandas`, `seaborn`, `matplotlib.pyplot`, `numpy`.
    - **Para Jupyter Notebook (instalación local):** Si no las tienes, puedes instalarlas usando `pip install pandas seaborn matplotlib numpy`.
- **Datos**: Los archivos CSV (`plans.csv`, `users_latam.csv`, `usage.csv`) deben estar en el mismo directorio que el notebook o en la ruta especificada en el código (ej. `/datasets/` si se usa Colab o una ruta relativa para Jupyter).

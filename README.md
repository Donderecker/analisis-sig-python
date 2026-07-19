# Análisis Geoespacial y Estadístico con Python

Este repositorio contiene el desarrollo y los resultados de un flujo de trabajo técnico enfocado en el procesamiento de datos raster multiespectrales y el análisisPipe de datos estadísticos descriptivos. El código fuente interactivo se encuentra disponible en el archivo Jupyter Notebook adjunto.

---

## 1. Procesamiento y Visualización de Imágenes Satelitales (Sentinel-2)

En este apartado se detalla el tratamiento de datos raster provenientes del sensor Sentinel-2. Utilizando la librería `rasterio`, se realizó la manipulación de bandas espaciales para generar combinaciones espectrales y el cálculo automatizado de índices ambientales clave:

* **Combinación de Color Real:** Visualización estándar en el espectro visible (Bandas 4, 3, 2).
* **Combinación Infrarrojo Cercano:** Resalte de cobertura vegetal activa (Bandas 8, 4, 3).
* **Índice de Vegetación de Diferencia Normalizada (NDVI):** Cuantificación de la densidad de la vegetación.
* **Índice de Agua de Diferencia Normalizada (NDWI):** Monitoreo de cuerpos de agua y humedad.

### Visualización de Resultados Ráster | *Sentinel-2 Spectral Bands and Environmental Indices*

![Sentinel-2 Spectral Bands and Environmental Indices](Sentinel-2%20Spectral%20Bands%20and%20Environmental%20Indices.jpg)

---

## 2. Análisis Estadístico Comparativo de Sensores Térmicos

Evaluación del rendimiento, consistencia y correlación entre dos tecnologías de medición térmica con distintas arquitecturas de costos: sensores de bajo costo (Arduino) y sensores de estándar comercial de alta gama (Hobo), registrados simultáneamente en un entorno controlado.

### A. Evolución Temporal de las Mediciones | *Thermal Sensor Time Series*
Registro continuo minuto a minuto que permite contrastar directamente el comportamiento de las curvas térmicas capturadas por los cuatro sensores.

![Thermal Sensor Time Series](Thermal%20Sensor%20Time%20Series.png)

### B. Distribución de Frecuencia (Sensor Arduino 1) | *Temperature Frequency Distribution*
Histograma detallado para evaluar la densidad, el rango de variación térmica y la concentración de lecturas específicas en el dispositivo.

![Temperature Frequency Distribution](Temperature%20Frequency%20Distribution.png)

### C. Dispersión General y Análisis de Cuartiles | *Temperature Distribution Boxplot*
Gráfico de cajas (Boxplot) para comparar estadísticamente la mediana, los límites y la presencia de asimetrías de todos los dispositivos de manera simultánea.

![Temperature Distribution Boxplot](Temperature%20Distribution%20Boxplot.png)

---

## Conclusiones del Análisis

A través de las representaciones gráficas y métricas de dispersión se identifican las siguientes dinámicas de comportamiento:

* **Dispersión en Sensores de Bajo Costo (Arduino):** Muestran variaciones y oscilaciones internas considerables entre sí. Esto evidencia una mayor sensibilidad al ruido instrumental o menor calibración de fábrica, traduciéndose en una disparidad notable en los datos registrados bajo las mismas condiciones.
* **Consistencia en Sensores Comerciales (Hobo):** Reflejan una alta reproducibilidad de datos, manteniendo curvas y valores altamente homogéneos entre sí, validando su estabilidad operativa para registros de alta precisión.

---

## Tecnologías Utilizadas
* Python 3
* Rasterio & NumPy (Procesamiento numérico y geoespacial)
* Pandas (Gestión de bases de datos)
* Matplotlib & Seaborn (Visualización estadística de datos)

---
*Nota académica: Este proyecto fue desarrollado individualmente a partir de las metodologías abordadas en el marco de la formación en Sistemas de Información Geográfica de la Universidad Austral de Chile.*

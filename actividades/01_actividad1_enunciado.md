<h1 align="center">INF-497 — Análisis de Datos Espaciales</h1>
<h2 align="center">Actividad 1</h2>
<p align="center">
<strong>Universidad Técnica Federico Santa María</strong><br>
<strong>Departamento de Informática</strong><br>
<strong>Daniela Opitz</strong><br>
<strong>2026</strong>
</p>

## Contexto

En esta actividad vamos a trabajar con datos de la **Región Metropolitana de Santiago, Chile**. Usaremos los datos del Censo 2017 (comunas) y un Modelo de Elevación Digital (DEM) descargado de Copernicus GLO-30.



## Datos Proporcionados

- **Shapefile de comunas:** `datos/external/censo2017/R13/COMUNA_C17.shp` (polígonos de las comunas de la Región Metropolitana, Censo 2017).
- **DEM Copernicus GLO-30:** se descargará usando la librería `dem_stitcher` a partir del bounding box de las comunas.

---

## Preámbulo: Descarga del DEM

A continuación se entrega el código para descargar el DEM una vez que tengas el bounding box calculado. Este bloque utiliza la función `stitch_dem` de la librería `dem_stitcher`, que descarga automáticamente el modelo de elevación Copernicus GLO-30. El resultado se guarda como un archivo GeoTIFF comprimido con LZW.

**Tu tarea es obtener la variable `BOUNDS` antes de ejecutar este código** (ver Paso 1).

```python
from dem_stitcher import stitch_dem
import numpy as np
import rasterio

# Bounding box: [lon_min, lat_min, lon_max, lat_max]
OUTPUT_FILE = "datos/external/nasadem/nasadem_santiago.tif"

print("Descargando DEM Copernicus 30m para Santiago...")
arr, profile = stitch_dem(
    BOUNDS,
    dem_name='glo_30',          # Copernicus GLO-30: global, sin login
    dst_ellipsoidal_height=False,
    dst_area_or_point='Point'
)

# Guardar como GeoTIFF
profile.update(dtype='float32', compress='lzw')
with rasterio.open(OUTPUT_FILE, 'w', **profile) as dst:
    dst.write(arr.astype('float32'), 1)

print(f"Archivo guardado: {OUTPUT_FILE}")
```

**¿Qué hace cada línea?**

- `stitch_dem(BOUNDS, ...)` descarga las tiles del DEM que cubren el bounding box indicado y las une en un solo arreglo NumPy (`arr`). También devuelve `profile`, un diccionario con los metadatos del raster (CRS, resolución, dimensiones, etc.).
- `profile.update(dtype='float32', compress='lzw')` actualiza los metadatos para guardar los valores como punto flotante de 32 bits y aplicar compresión LZW (reduce el tamaño del archivo sin perder información).
- `rasterio.open(OUTPUT_FILE, 'w', **profile)` crea un nuevo archivo GeoTIFF de escritura con los metadatos del profile.
- `dst.write(arr.astype('float32'), 1)` escribe el arreglo de elevaciones en la banda 1 del archivo.

---

## Instrucciones

Desarrolla los siguientes pasos en un notebook de Jupyter:

### Paso 1: Definir el área de estudio

1. Carga el shapefile de comunas de la Región Metropolitana usando GeoPandas.
2. Reproyecta las geometrías al sistema de coordenadas WGS84 (`EPSG:4326`).
3. Extrae el bounding box (`lon_min`, `lat_min`, `lon_max`, `lat_max`) del área completa de las comunas y almacénalo en una variable llamada `BOUNDS`. Este será el insumo para la descarga del DEM.

> **Pista:** revisa el atributo `.total_bounds` de un GeoDataFrame.

### Paso 2: Descargar el Modelo de Elevación Digital

1. Ejecuta el código del preámbulo para descargar el DEM usando el `BOUNDS` que calculaste.
2. Verifica que el archivo `nasadem_santiago.tif` se haya guardado correctamente.

### Paso 3: Verificar y explorar el raster

1. Abre el archivo GeoTIFF con `rasterio`.
2. Imprime la información básica del raster: CRS, resolución aproximada en metros, dimensiones (ancho × alto) y límites geográficos.
3. Calcula e imprime la elevación mínima y máxima del área.

### Paso 4: Visualizar el DEM y las comunas

1. Genera un mapa del DEM filtrando los valores de elevación mayores a 0 (sobre el nivel del mar).
2. Genera un mapa de las comunas de la Región Metropolitana e indica cuántas comunas contiene el dataset.

### Paso 5: Calcular estadísticas zonales de elevación

1. Usa la función `zonal_stats` de la librería `rasterstats` para calcular estadísticas de elevación (media, mínima, máxima) para cada comuna. 
2. Convierte los resultados a un DataFrame de pandas y muéstralo.
3. ¿Cuáles son las 5 comunas con mayor elevación promedio y las 5 con menor?
4. ¿Cuál es la comuna con mayor rango de elevación (diferencia entre máxima y mínima)? 

### Paso 6: Visualización comparativa

Genera una figura con 3 paneles (subplots) lado a lado:

1. **Panel 1:** DEM original (superficie de elevación).
2. **Panel 2:** Mapa de las comunas de la Región Metropolitana.
3. **Panel 3:** Mapa coroplético de la elevación promedio por comuna.

---

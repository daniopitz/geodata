<h1 align="center">INF-497 — Análisis de Datos Espaciales</h1>
<p align="center">
<strong>Universidad Técnica Federico Santa María</strong><br>
<strong>Departamento de Informática</strong><br>
<strong>Docente: Daniela Opitz</strong><br>
<strong>Miércoles · 2 bloques · 4 marzo — 1 julio 2026</strong>
</p>

---

## Calendario de clases

| Sem | Fecha | Tipo | Contenido | Clase Teórica | Jupyter | Evaluación |
|-----|-------|------|-----------|---------------|---------|------------|
| 1 | 4 mar | Teórica | Introducción: datos espaciales, tipos (vector), sistemas de referencia, tablas y geopandas. Fuentes de datos para el proyecto. | [00_introduccion.pdf](https://github.com/daniopitz/geodata/tree/main/00_introduccion.pdf) | [00_introduccion.ipynb](https://github.com/daniopitz/geodata/tree/main/00_introduccion.ipynb) | |
| 2 | 11 mar | Teórica + Práctica | Datos raster + matrices de pesos espaciales + práctica en Python | [01_datos_espaciales.pdf](https://github.com/daniopitz/geodata/tree/main/01_datos_espaciales.pdf) | [01_datos_espaciales.ipynb](https://github.com/daniopitz/geodata/tree/main/01_datos_espaciales.ipynb) | P |
| 3 | 18 mar | — | **Sin clases — Semana Mechona** | — | — | |
| 4 | 25 mar | Teórica + Práctica | Pesos Espaciales|[02_pesos_espaciales.pdf](https://github.com/daniopitz/geodata/tree/main/02_pesos_espaciales.pdf)| [02_pesos_espaciales.ipynb](https://github.com/daniopitz/geodata/tree/main/02_pesos_espaciales.ipynb) | P |
| 5 | 1 abr | Teórica + Práctica | Visualización I: Mapas Coropleticos| [03_visualizacion.pdf](https://github.com/daniopitz/geodata/tree/main/03_visualizacion.pdf) | [03_visualizacion_parte1.ipynb](https://github.com/daniopitz/geodata/tree/main/03_visualizacion_parte1.ipynb) | P |
| 6 | 8 abr | Presentación| Presentación avance proyecto  | Presentación avance proyecto| Presentación avance proyecto|**H1 entrega**  |
| 7 | 15 abr | Teórica + Práctica  |  Autocorrelacion Global y Local| [04_autocorrelacion_global.pdf](https://github.com/daniopitz/geodata/tree/main/04_autocorrelacion_global.pdf)| [04_autocorrelacion_global.ipynb](https://github.com/daniopitz/geodata/tree/main/04_autocorrelacion_global.ipynb) | P |
| 8 | 22 abr | Teórica + Práctica  | Autocorrelación espacial local: I de Moran local, Gi y Gi* de Getis-Ord, hot spots y outliers (LISA) | [05_autocorrelacion_local.pdf](https://github.com/daniopitz/geodata/tree/main/05_autocorrelacion_local.pdf) | [05_autocorrelacion_local.ipynb](https://github.com/daniopitz/geodata/tree/main/05_autocorrelacion_local.ipynb) | P |
| 9 | 29 abr | Teórica + Práctica | Desigualdad espacial: Gini, Theil, Lorenz, Moran y descomposiciones espaciales en Python | [06_desigualdad_espacial.pdf](https://github.com/daniopitz/geodata/tree/main/06_desigualdad_espacial.pdf) | [06_desigualdad_espacial.ipynb](https://github.com/daniopitz/geodata/tree/main/06_desigualdad_espacial.ipynb) | P |
| 10 | 6 may | Teórica + Práctica | Clustering y regionalización: K-Means, AHC y AHC con restricción espacial (Queen, KNN) | [07_regionalizacion.pdf](https://github.com/daniopitz/geodata/tree/main/07_regionalizacion.pdf) | [07_regionalizacion.ipynb](https://github.com/daniopitz/geodata/tree/main/07_regionalizacion.ipynb) | P |
| 11 | 13 may | Teórica + Práctica | Regresión espacial (Parte 1): OLS, diagnóstico de residuos y SLX | [08_regresion_espacial.pdf](https://github.com/daniopitz/geodata/tree/main/08_regresion_espacial.pdf) | [08_regresion_espacial.ipynb](https://github.com/daniopitz/geodata/tree/main/08_regresion_espacial.ipynb) | P |
| 12 | 20 may |  — | **Sin Clases Vacaciones**|  — | — |
| 13 | 27 may | Teórica + Práctica | Regresión espacial (Parte 2): SEM, SAR y heterogeneidad espacial. *2do bloque: trabajo en T1.* | `09_regresion_espacial_parte2.pdf` | `09_regresion_espacial_parte2.ipynb` | |
| 14 | 3 jun | Teórica + Práctica | Spatial Feature Engineering (Parte 1): Map Matching — POIs cercanos, joins punto/polígono, tesselación H3 (Uber). *2do bloque: trabajo en T1.* | `10_feature_engineering_parte1.pdf` | `10_feature_engineering_parte1.ipynb` | |
| 15 | 10 jun | Teórica + Práctica | Spatial Feature Engineering (Parte 2): Map Synthesis — ring buffers, clustering (HDBSCAN) como feature. *2do bloque: trabajo en T1.* | `10_feature_engineering_parte2.pdf` | `10_feature_engineering_parte2.ipynb` | **H2 entrega** |
| 16 | 17 jun | Teórica + Práctica | GWR (tema extra, fuera del libro base) + integración de contenidos. *2do bloque: trabajo en T1.* | `11_GWR.pdf` | `11_GWR.ipynb` | |
| 17 | 24 jun | — | Integración y preparación de presentaciones | — | — | **T1 entrega** |
| 18 | 1 jul | Evaluación | Presentaciones orales + entrega informe final | — | — | **H3 entrega final** · T2 (voluntaria) |

---

## Resumen de evaluaciones

| Evaluación | Fecha Tentativa | Peso |
|---|---|---|
| H1 Proyecto | 8 abril | 15% del PF |
| H2 Proyecto | 10 junio | 25% del PF |
| T1 Tarea | 24 junio | 50% de T |
| T2 Tarea (voluntaria) | 1 julio | 50% de T |
| H3 + Informe final | 1 julio | 60% del PF |
| Participación (P) | Semanas 2, 4, 5, 7, 8, 9, 10, 11 (actividades 01–08) | mejores 5 de 8 |

---



## Sesiones prácticas (Participación)

Se evaluarán **8 sesiones prácticas** a lo largo del semestre. El objetivo es evaluar la realización de las actividades en clase.  Se consideran las **mejores 5** para el cálculo de la nota P.  

---

## Fórmula nota final

```
Nota Final = 0.5 × PF + 0.4 × T + 0.1 × P

PF = 0.15 × H1 + 0.25 × H2 + 0.60 × H3
T  = max(T1, T2)   # T2 es voluntaria; reemplaza a T1 si es mayor
P  = mejores 5 sesiones prácticas de 8
```


---

## Instalación del entorno

Este proyecto usa [uv](https://docs.astral.sh/uv/) para gestionar paquetes y dependencias. Para instalar el entorno local, ejecuta:

```bash
uv sync
```

Esto creará un entorno virtual e instalará todas las dependencias especificadas en `pyproject.toml`.

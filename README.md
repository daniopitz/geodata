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
| 4 | 25 mar | Teórica + Práctica | Visualización I: mapas coropléticos y símbolos proporcionales + práctica | `03_visualizacion_I.pdf` | `03_visualizacion_I.ipynb` | P |
| 5 | 1 abr | Teórica + Práctica | Visualización II: densidad kernel + práctica en Python | `04_visualizacion_II.pdf` | `04_visualizacion_II.ipynb` | P |
| 6 | 8 abr | Teórica | Autocorrelación espacial global y local | `05_autocorrelacion.pdf` | — | **H1 entrega** |
| 7 | 15 abr | Práctica | Cálculo e interpretación de índices de Moran y LISA | — | `05_autocorrelacion.ipynb` | P |
| 8 | 22 abr | Teórica | Análisis de patrones de puntos | `06_patrones_puntos.pdf` | — | |
| 9 | 29 abr | Práctica | Análisis de patrones de puntos en Python | — | `06_patrones_puntos.ipynb` |**T1 entrega** |
| 10 | 6 may | Teórica | Desigualdad espacial: Gini, Theil, Lorenz | `07_desigualdad.pdf` | — | P |
| 11 | 13 may | Teórica | Regionalización y construcción de variables derivadas | `08_regionalizacion.pdf` | — |**H2 entrega** |
| 12 | 20 may | Teórica + Práctica | Regionalización y construcción de variables derivadas + práctica en Python | `08_regionalizacion.pdf` | `08_regionalizacion.ipynb` | P |
| 13 | 27 may | Práctica | Índices de desigualdad y regionalización en Python | — | `07_desigualdad.ipynb` | P |
| 14 | 3 jun | Teórica | Modelos de regresión espacial: SAR y SEM | `09_regresion_espacial.pdf` | — | **T2 entrega** |
| 15 | 10 jun | Práctica | Implementación SAR, SEM y GWR en Python | — | `09_regresion_espacial.ipynb` | P |
| 16 | 17 jun | Teórica | GWR + integración de contenidos | `10_GWR.pdf` | — | |
| 17 | 24 jun | Teórica | Preparación presentaciones | — | — | |
| 18 | 1 jul | Evaluación | Presentaciones orales + entrega informe final | — | — | **H3 entrega final** |

---

## Resumen de evaluaciones

| Evaluación | Fecha Tentativa | Peso |
|---|---|---|
| H1 Proyecto | 8 abril | 15% del PF |
| H2 Proyecto | 13 mayo | 25% del PF |
| T1 Tarea | 29 abril | 50% de T |
| T2 Tarea | 3 junio | 50% de T |
| H3 + Informe final | 1 julio | 60% del PF |
| Participación (P) | Semanas 2, 4, 5, 7, 10, 12, 13, 15 | mejores 5 de 8 |

---



## Sesiones prácticas (Participación)

Se evaluarán **8 sesiones prácticas** a lo largo del semestre. El objetivo es evaluar la realización de las actividades en clase.  Se consideran las **mejores 5** para el cálculo de la nota P.  

---

## Fórmula nota final

```
Nota Final = 0.5 × PF + 0.4 × T + 0.1 × P

PF = 0.15 × H1 + 0.25 × H2 + 0.60 × H3
T  = (T1 + T2) / 2
P  = mejores 5 sesiones prácticas de 8
```


---

## Instalación del entorno

Este proyecto usa [uv](https://docs.astral.sh/uv/) para gestionar paquetes y dependencias. Para instalar el entorno local, ejecuta:

```bash
uv sync
```

Esto creará un entorno virtual e instalará todas las dependencias especificadas en `pyproject.toml`.

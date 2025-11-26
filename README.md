# 💥 Análisis de Accidentes de Tránsito en Bucaramanga (2012-2023)

[cite_start]Este proyecto es una **aplicación web interactiva** que permite la visualización y el análisis profundo de los datos de accidentes de tránsito registrados en la ciudad de Bucaramanga entre los años 2012 y 2023[cite: 3, 5, 7]. [cite_start]Utiliza una API para exponer los resultados del análisis exploratorio de datos (EDA) y la aplicación de modelos de **Machine Learning** con el objetivo de clasificar la gravedad de los siniestros[cite: 6, 83].

---

### 💡 Características Principales

* [cite_start]**Análisis Exploratorio de Datos (EDA):** Visualización de tendencias anuales de accidentes (2012-2023) [cite: 16][cite_start], y los barrios con la mayor cantidad de accidentes[cite: 14].
* [cite_start]**Barrios Críticos:** Los barrios con la mayor cantidad de accidentes son: **Centro** (3861) [cite: 15][cite_start], **Cabecera Del Llano** (2360) [cite: 15][cite_start], y **San Francisco** (1974)[cite: 15].
* **Patrones Temporales y Vehiculares Clave:**
    * [cite_start]**Hora Pico:** 12 horas[cite: 103].
    * [cite_start]**Día más Crítico:** Día 6 (Sábado, considerando 1=Lunes, 7=Domingo)[cite: 103].
    * [cite_start]**Mes más Crítico:** Mes 3 (Marzo)[cite: 103].
    * [cite_start]**Vehículos Más Involucrados:** Automóvil (30620), Moto (24559), y Peatón (4136)[cite: 103].
* **Análisis de Gravedad:** La mayoría de los accidentes registrados son **Solo daños** (19602) o **Con heridos** (18982). [cite_start]Los accidentes **Con Muertos** representan la menor cantidad (609)[cite: 100].
* [cite_start]**Modelado de Machine Learning:** Aplicación de modelos para clasificar la gravedad del accidente: K-Nearest Neighbors, Árbol de Decisión y Naive Bayes[cite: 83].

---

### 📊 Datos y Metodología

#### 💾 Datos Base

* [cite_start]**Periodo:** Años 2012-2023[cite: 5, 7].
* [cite_start]**Total de Registros Usados:** 39,193[cite: 9].

#### 🛠️ Modelos de Clasificación

[cite_start]El objetivo de los modelos es clasificar la variable objetivo **Gravedad del Accidente** (Con Muertos | Con heridos | Solo daños)[cite: 88].

| Modelo | Accuracy | Precision (Macro Avg) | Recall (Macro Avg) |
| :--- | :--- | :--- | :--- |
| **Árbol de Decisión** | [cite_start]**83.20%** [cite: 107] | [cite_start]0.562 [cite: 123] | [cite_start]0.564 [cite: 124] |
| **K-Nearest Neighbors (KNN)** | [cite_start]80.00% [cite: 105] | [cite_start]0.559 [cite: 105] | [cite_start]0.545 [cite: 105] |
| **Naive Bayes** | [cite_start]67.55% [cite: 114] | [cite_start]0.542 [cite: 119] | [cite_start]0.463 [cite: 119] |

[cite_start]**Características (Features) utilizadas para ML:** `HORA_INT`, `MES_NUM`, `DIA_NUM`, `AÑO`, `PEATON`, `AUTOMOVIL`, `MOTO`, `BICICLETA`, `DIURNIO_NOCTURNO_ENC`[cite: 86, 87].

---

### 🚧 Estructura del Proyecto

El proyecto está dividido en dos componentes principales:

1.  **API/Backend (Análisis y ML):** Contiene la lógica para el procesamiento de datos, la implementación de los modelos de Machine Learning, y la exposición de los resultados.
2.  **Frontend (Visualización Web):** La interfaz de la página web que consume la API para renderizar los gráficos y tablas.



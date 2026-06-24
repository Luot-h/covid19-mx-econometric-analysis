# Análisis Econométrico Integral de la Evolución, Mortalidad y Hospitalización por COVID-19 en México

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Framework](https://img.shields.io/badge/Statsmodels-Econometrics-green.svg)](https://www.statsmodels.org/)
[![Institution](https://img.shields.io/badge/IPN-ESCOM-midnightblue.svg)](https://www.escom.ipn.mx/)

Este repositorio contiene el desarrollo del **Proyecto Final** para la asignatura de **Modelos Econométricos** del semestre **2026-2** en la **Escuela Superior de Cómputo del Instituto Politécnico Nacional**.

El objetivo primordial es aplicar un marco metodológico riguroso para modelar y entender los determinantes de la hospitalización, los factores críticos de mortalidad y la dinámica temporal/espacial de la pandemia de COVID-19 en el contexto mexicano.

---

## 📊 Estructura del Proyecto

El análisis se ejecuta de manera secuencial a través de un único entorno de trabajo estructurado en las siguientes etapas fundamentales:

### Fase Inicial y Descriptiva
1. **Configuración del entorno:** Inicialización de librerías y control de versiones del software.
2. **Carga y limpieza de datos:** Preprocesamiento de la base masiva, manejo de valores faltantes y codificación de variables estructurales.
3. **Etapa 1 — Estadística descriptiva:** Análisis de frecuencias, medidas de tendencia central y dispersión de las variables demográficas y clínicas.

### Modelado Clásico y de Respuesta Cualitativa
4. **Etapa 2 — Regresión lineal simple:** Análisis inicial de correlaciones lineales base.
5. **Etapa 3 — Regresión lineal múltiple:** Incorporación de variables de control macro y microclínicas.
6. **Etapa 4 — Variables *dummy*:** Modelado de efectos estructurales por género, sector de atención y condiciones geográficas.
7. **Etapa 5 — Modelos Logit y Probit:** Estimación de las probabilidades de riesgo de deceso y hospitalización mediante máxima verosimilitud (ML).

### Pruebas de Diagnóstico y Validación
8. **Etapa 6 — Multicolinealidad:** Diagnóstico mediante el Factor de Inflación de la Varianza (VIF).
9. **Etapa 7 — Heterocedasticidad:** Pruebas estadísticas robustas (White / Breusch-Pagan) y correcciones.
10. **Etapa 8 — Autocorrelación:** Verificación de independencia en los residuos.
11. **Etapa 9 — Normalidad:** Evaluación de la distribución de las perturbaciones.

### Análisis Dinámico y Series de Tiempo
12. **Construcción de la serie de tiempo:** Agregación de datos a frecuencias diarias/semanales nacionales y estatales.
13. **Etapa 10 — Rezagos distribuidos:** Evaluación del impacto temporal diferido de las políticas de movilidad y contagios.
14. **Etapa 11 — Modelo de ajuste parcial:** Modelado de la velocidad de ajuste institucional ante picos de demanda hospitalaria.
15. **Etapa 12 — Expectativas adaptativas:** Análisis del comportamiento social e institucional basado en la evolución epidemiológica previa.
16. **Etapa 13 — Series de tiempo avanzadas:** Análisis de estacionariedad (Prueba Dickey-Fuller Aumentada - ADF), identificación y calibración de estructuras AR/MA/ARMA/ARIMA y proyección de escenarios de hospitalización.

### Interpretación y Extensiones Avanzadas
17. **Visualizaciones obligatorias + *dashboard* resumen:** Dashboard integrado para la exploración dinámica de coeficientes y pronósticos.
18. **Etapa 15 — Interpretación económica:** Discusión de los estimadores bajo la perspectiva del sistema de salud y de la política pública.
19. **🚀 Puntos Extra Implementados:**
    * **Datos de Panel:** Control de heterogeneidad inobservable a través del tiempo y las entidades federativas.
    * **Econometría Espacial:** Identificación de autocorrelación espacial y propagación de contagios inter-estatales mediante matrices de contigüidad.
    * **Comparación de Modelos de Pronóstico:** Evaluación comparativa del rendimiento predictivo de diferentes especificaciones.
    * **Pronósticos por Entidad:** Desagregación analítica personalizada para las 32 regiones del país.
    * **Dashboard Interactivo:** Interfaz visual interactiva avanzada para usuarios no técnicos.

---

## 💾 Fuente de Datos

Los análisis utilizan los microdatos provistos por la **Dirección General de Epidemiología de la Secretaría de Salud (SSA)** de México. 
* **Origen:** [Datos Abiertos COVID-19 en México](https://www.gob.mx/salud/documentos/datos-abiertos-152127)
* *Nota:* La base de datos cruda presenta un volumen de varios gigabytes (GB), por lo cual está excluida del sistema de control de versiones mediante el archivo `.gitignore`.

---

## 👥 Equipo de Desarrolladores

* Escudero Gutierrez Evelyn Abril
* Perez Hurtado Luis Rogelio
* Mendiola Gomez Juan

---

## ⚙️ Instrucciones de Ejecución

### Prerrequisitos
Contar con una distribución activa de Python (versión 3.9 o superior) y el gestor de dependencias `pip`.

### Configuración del Entorno Local

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/Luot-h/covid19-mx-econometric-analysis.git]
   cd covid19-mx-econometric-analysis
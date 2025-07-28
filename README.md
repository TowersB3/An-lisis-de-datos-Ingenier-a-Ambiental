# Análisis de Series de Tiempo: PM2.5 y Ozono en Itagüí

Este repositorio contiene el código y análisis para el estudio de la dinámica temporal y la relación entre las concentraciones de PM2.5 y Ozono en el municipio de Itagüí, Antioquia.

## 1. Contexto y Objetivo del Proyecto

La contaminación del aire por material particulado fino (PM2.5) y ozono (O3) es un desafío significativo en zonas urbano-industriales como el Valle de Aburrá. Este proyecto se centra en analizar datos de alta frecuencia de estos dos contaminantes, recolectados por la estación del SIATA en la I.E. Concejo Municipal de Itagüí.

El objetivo principal es doble:

1. Caracterizar y modelar la dinámica individual de las concentraciones de PM2.5 y O3 para identificar sus patrones temporales (ciclos diarios, estacionalidad, tendencias).

2. Evaluar la relación y correlación que existe entre ambos contaminantes para entender mejor sus interacciones en la atmósfera local

## 2. Metodología y Herramientas

**Metodología**

El flujo de trabajo se estructuró de la siguiente manera:

1. **Procesamiento de Datos:** Carga, limpieza y manejo de datos faltantes mediante interpolación temporal.

2. **Análisis Descriptivo y Visualización:** Cálculo de estadísticas descriptivas y generación de gráficos (series de tiempo, histogramas, diagramas de caja) para explorar el comportamiento de cada variable.

3. **Análisis de Correlación:** Se realizó un análisis de correlación y regresión para cuantificar la naturaleza y fuerza de la relación entre las concentraciones de PM2.5 y Ozono.
  
4. **Modelado Estadístico:** Se ajustó un modelo ARMA(1,1) a las series de tiempo con el objetivo de modelar su comportamiento y dependencia interna.

5. **Análisis de Series de Tiempo:**

- **Autocorrelación:** Se usaron las funciones de autocorrelación (ACF) y autocorrelación parcial (PACF) para identificar la estructura de dependencia temporal.

- **Estacionalidad y Tendencia:** Se aplicaron las pruebas de Dickey-Fuller Aumentada y Mann-Kendall.

- **Análisis Espectral:** Se empleó la Transformada de Fourier para descomponer las series en sus frecuencias constituyentes.

Herramientas

El análisis se implementó en Python dentro de un Jupyter Notebook, utilizando las siguientes librerías:

- **Pandas y NumPy:** Para la manipulación y operación de datos.

- **Matplotlib y Seaborn:** Para toda la visualización gráfica.

- **Statsmodels:** Para el análisis de series de tiempo, incluyendo las funciones ACF/PACF y el ajuste de modelos ARMA.

- **SciPy:** Para pruebas estadísticas y procesamiento de señales (como la Transformada de Fourier).

- **PyMannKendall:** Para la prueba de tendencia de Mann-Kendall


## 3. Hallazgos y Discusión

- **Ciclos Diarios Diferenciados:** Los resultados confirmaron comportamientos diarios distintos para cada contaminante. El PM2.5 presenta dos picos diarios claros, coincidiendo con las horas pico de tráfico vehicular. Por otro lado, el Ozono muestra un único pico pronunciado al mediodía, consistente con su naturaleza fotoquímica, que depende de la radiación solar.

- **No Normalidad de los Datos:** Las pruebas estadísticas (como la de Kolmogorov-Smirnov) confirmaron que las distribuciones de ambos contaminantes no son normales, lo cual es un resultado típico en datos ambientales y condiciona el tipo de modelos que se pueden aplicar.

- **Limitaciones del Modelo ARMA(1,1):** Un hallazgo crucial fue que el modelo ARMA(1,1) resultó ser insuficiente para capturar adecuadamente la fuerte componente estacional presente en las series. Aunque el modelo puede describir la dependencia a corto plazo, falla en representar los patrones cíclicos diarios y semanales.

- **Relación entre Contaminantes:** El análisis de correlación reveló la compleja interacción entre PM2.5 y Ozono. A menudo, sus picos de concentración no son simultáneos, lo que sugiere una relación inversa o desfasada en el ciclo diario, donde los precursores de uno pueden influir en la formación del otro.


## 4. Conclusión Principal del Proyecto

Este proyecto caracteriza los patrones temporales del PM2.5 y el Ozono en Itagüí, y cuantifica la relación existente entre ellos.

La conclusión central es que, si bien existen patrones y dependencias temporales claras en los datos, los modelos simples como el ARMA(1,1) no son adecuados para un pronóstico preciso debido a la fuerte estacionalidad de los fenómenos. Esto subraya la necesidad de utilizar modelos más avanzados que incorporen explícitamente componentes estacionales (como SARIMA o modelos de machine learning) para futuras investigaciones o aplicaciones de pronóstico de la calidad del aire.

## 5. Código Fuente

El código completo de este análisis se encuentra en el archivo [TrabajoFinal_JuanEstebanBolivar.ipynb](./TrabajoFinal_JuanEstebanBolivar.ipynb).


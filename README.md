# Análisis Exploratorio de Contaminantes Atmosféricos (PM2.5 y O₃) en el Valle de Aburrá

Este repositorio contiene el análisis final realizado para el curso de Análisis de Datos, centrado en la relación entre los contaminantes criterio PM2.5 y Ozono, y su interacción con variables meteorológicas en el área metropolitana del Valle de Aburrá.

## 1. Contexto y Objetivo del Proyecto

El Valle de Aburrá presenta desafíos únicos en la gestión de la calidad del aire debido a su densidad poblacional, sus fuentes de emisión y su compleja topografía. El objetivo de este proyecto fue realizar un análisis exploratorio de datos para investigar las relaciones y patrones existentes entre las concentraciones de PM2.5, Ozono (O₃) y variables meteorológicas clave (como temperatura y velocidad del viento), utilizando datos de las estaciones de monitoreo de la red del SIATA.

## 2. Metodología y Herramientas

El análisis se desarrolló íntegramente en **Python** dentro de un entorno de Jupyter Notebook. El flujo de trabajo consistió en:

* **Recopilación y Limpieza de Datos:** Consolidación de bases de datos de múltiples estaciones de monitoreo, tratando valores faltantes y asegurando la consistencia de los datos.
* **Manejo de Series de Tiempo:** Uso de la librería **Pandas** para la manipulación, agregación y análisis de los datos en sus componentes temporales.
* **Análisis Estadístico Descriptivo:** Cálculo de estadísticas fundamentales y matrices de correlación para obtener una primera visión cuantitativa de las relaciones entre las variables.
* **Visualización de Datos:** Creación de gráficos (series de tiempo, diagramas de dispersión, histogramas) con las librerías **Matplotlib** y **Seaborn** para identificar patrones visuales y comunicar los hallazgos.

## 3. Hallazgos y Discusión

El análisis de correlación lineal directa entre las concentraciones de los contaminantes y las variables meteorológicas individuales mostró relaciones más débiles de lo que la teoría podría sugerir.

Este hallazgo es clave, ya que sugiere que la calidad del aire en el Valle de Aburrá es un fenómeno complejo y **altamente no lineal**. Las principales conclusiones de la discusión son:

* **Interacciones Múltiples:** La formación y dispersión de contaminantes no depende de una sola variable, sino de la interacción simultánea de múltiples factores (temperatura, radiación solar, velocidad y dirección del viento, humedad, etc.).
* **Importancia de la Química Atmosférica:** La formación de ozono troposférico es un proceso fotoquímico secundario, por lo que su concentración no puede explicarse adecuadamente mediante correlaciones simples con variables primarias.
* **Efectos Locales y de Transporte:** Cada estación de monitoreo puede estar fuertemente influenciada por fuentes de emisión locales y por la dinámica de transporte de contaminantes a través del valle, lo que añade otra capa de complejidad al análisis.

## 4. Conclusión Principal del Proyecto

La principal conclusión de este análisis no es una fórmula predictiva simple, sino una **comprensión más profunda de la complejidad del sistema**. Se demostró que para modelar o predecir adecuadamente la calidad del aire en este entorno, es necesario recurrir a modelos más avanzados (multivariados, de machine learning o basados en la física y química atmosférica) que puedan capturar estas interacciones no lineales.

Este proyecto fue un excelente ejercicio para aplicar técnicas de análisis de datos a un problema ambiental real, complejo y con datos no ideales, reflejando los desafíos que enfrenta un profesional en el campo.

## 5. Código Fuente

El código completo de este análisis se encuentra en el archivo [TrabajoFinal_JuanEstebanBolivar.ipynb](./TrabajoFinal_JuanEstebanBolivar.ipynb).

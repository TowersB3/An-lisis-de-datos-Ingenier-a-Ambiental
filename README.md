# Análisis Exploratorio de Contaminantes Atmosféricos (PM2.5 y O₃) en el Valle de Aburrá

La contaminación del aire por material particulado fino (PM2.5) y ozono (O₃) es un 
desafío significativo en zonas urbano-industriales como el municipio de Itagüí, Colombia. 
Este estudio tiene como objetivo principal caracterizar y modelar la dinámica de las 
concentraciones de estos dos contaminantes para identificar sus patrones temporales y 
evaluar la relación que existe entre ellos. Se utilizaron datos de alta frecuencia temporal, 
abarcando desde abril de 2023 hasta agosto de 2024, provenientes de la estación de 
monitoreo del SIATA ubicada en la I.E. Concejo Municipal de Itagüí. La metodología 
empleó un análisis de series de tiempo que incluyó estadísticas descriptivas, análisis de 
autocorrelación (ACF/PACF), transformada de Fourier, el ajuste de un modelo
ARMA(1,1) y análisis de correlación y regresión. Los resultados revelaron ciclos diarios 
distintos para cada contaminante: el PM2.5 presenta dos picos diarios asociados a las 
horas de mayor tráfico, mientras que el ozono muestra un único pico al mediodía,
impulsado por la actividad fotoquímica. El modelo ARMA(1,1) ajustado demostró ser 
insuficiente para capturar la fuerte componente estacional de las series, lo que se 
evidenció en la autocorrelación remanente en sus residuales. Adicionalmente, se encontró 
una correlación lineal negativa, estadísticamente significativa pero extremadamente débil 
(coeficiente de -0.0656), entre las dos variables. Los modelos de regresión confirmaron 
esta débil conexión, con un coeficiente de determinación (R²) inferior a 0.01,
demostrando una capacidad predictiva prácticamente nula. Se concluye que, si bien los 
patrones temporales de ambos contaminantes son muy marcados, su interrelación es 
compleja y no puede ser explicada adecuadamente mediante modelos lineales simples o 
modelos ARMA estándar

El código completo de este análisis se encuentra en el archivo [TrabajoFinal_JuanEstebanBolivar.ipynb](./TrabajoFinal_JuanEstebanBolivar.ipynb).

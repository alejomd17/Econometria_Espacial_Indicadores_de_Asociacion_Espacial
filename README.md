# Econometria Espacial
# Análisis Exploratorio de Datos Espaciales
## Indicadores de Asociacion Espacial

### Índice de Moran e Indicadores Locales de Asociaión Espacial

En este notebook se muestra cómo implementar en Python el Índice Global de Moran y los Indicadores Locales de Asociación Espacial (LISA pos sus siglas en Inglés).
Ambas son medidas que caracterizan la distribución espacial de una variable. Sin embargo, el índice de Moran mide el grado dependencia o autocorrelación espacial **promedio**, es decir, responde a la pregunta ¿en general las unidades espaciales vecinas están relacionadas entre sí, o son independientes las unas de las otras, con respecto a la variable analizada? Si las unidades espaciales están relacionadas entre sí, el índice de Moran permite discernir si está asociación es positiva o negativa: ¿En promedio, son las unidades espaciales vecinas similares entre sí (dependencia positiva), son opuestas (depedencia negativa), o no hay relación (distribución aleatoria)?

Los Indicadores Locales de Asociación Espacial, comúnmente llamados (LISA - *Local Indicators of Spatial Association*) no preguntan acerca del patrón general o promedio que prevalece en la muestra, si no que preguntan por el tipo de patrón que se presenta alredador del vecindario de *cada* unidad espacial. Por ejemplo, es posible que aunque a nivel global, el índice de Moran sugiera que existe dependencia espacial positiva, a nivel local pueden exisitir algunos vecindarios de unidades espaciales que escapen a la tendencia, y por tanto exhibir correlación negativa o no exhibir ningún tipo de correlación, o viceversa. 

La implementación de estas medidas de autocorrelación espacial se aplicará a datos referentes al índice de necesadades básicas insatifechas (INBI) de los municipios Colombianos calculado por el DANE según el Censo de Población de 2005.

### Estadístico Bivariado Global de Moran e Indicadores Locales de Asociaión Espacial Bivariado

Después de analizar la distribución espacial de ambas variables, a continuación calcula el estadístico bivariado de Moran. Esto se hace a través de la función Moran_BV. Es necesario tener en cuenta que la primera variable que se provee como argumento a dicha función es la que se rezaga espacialmente. Esto es importante tenerlo presente a la hora de interprertar el estadístico bivariado de Moran.

Se obtiene que el estadístico bivariado Moran es negativo y significativo. Esto significa, en este caso, que en general los municipios con bajo valor agregado per cápita usualmente tienen vecinos con alta incidencia de la pobreza multidimensional rural o, equivalmentente, que los municipios con alto valor agregado per cápita tienen vecinos con un baja incidencia de la pobreza multidimiensional rural.


# Proyecto de Identificación de Patrones de Pobreza Multidimensional en Colombia asociado a las características de las viviendas en los hogares

## Descripción del Proyecto

¡Bienvenidos a nuestro viaje de exploración a través de las complejidades de la pobreza multidimensional en Colombia! En este proyecto, hemos emprendido un recorrido por los datos de vivienda recopilados por el DANE en 2022, con un objetivo en mente: buscar patrones y comprender mejor la realidad de las familias colombianas que enfrentan situaciones de vulnerabilidad desde la perspectiva de la vivienda.

Este proyecto utiliza técnicas de aprendizaje no supervisado y reducción de dimensionalidad en datos de vivienda de la Encuesta Nacional de Calidad de Vida del DANE 2022 para identificar patrones relacionados con la pobreza multidimensional en Colombia. El objetivo es desarrollar políticas públicas dirigidas a reducir la pobreza en poblaciones vulnerables.

## Estructura del Repositorio

El repositorio está organizado de la siguiente manera:

- **Datos**: Esta carpeta contiene los datos de entrada utilizados en el análisis. Incluye la información de la Encuesta Nacional de Calidad de Vida del DANE (2022):
  
  - `Datos de la vivienda.zip`: Archivo comprimido que contiene el CSV de los datos.

- **Código**: Aquí se encuentra el código utilizado en el análisis. El archivo está comentado para facilitar la comprensión:
  
  - `Proyecto Aprendizaje No Supervisado.ipynb`: El código presenta el siguiente proceso
    - Se preparan los datos, incluyendo la eliminación de columnas irrelevantes y la transformación de variables binarias. Se realizan análisis descriptivos de las variables binarias y categóricas numéricas. También se realiza un análisis geoespacial para visualizar la distribución geográfica de las encuestas en Colombia.
    - Se crea un mapa de calor interactivo que muestra la concentración de encuestas en diferentes regiones del país. Se utilizan gráficos dinámicos para comparar la presencia de servicios públicos como el acueducto y el alcantarillado en diferentes regiones. También se analiza la ocurrencia de desastres naturales en las diferentes regiones, lo que proporciona información sobre la vulnerabilidad de cada área.
    - Además se procede a reducir la dimensionalidad de los datos utilizando una matriz truncada a través de la descomposición en valores singulares. Sin embargo, este enfoque no logra obtener un índice unidimensional satisfactorio. Luego, se aplican algoritmos de clustering, incluyendo K-Means, K-Medoids y DBSCAN, para identificar grupos de hogares similares en función de múltiples características.
    - Se analizan las estadísticas y las características de cada cluster. Finalmente, se realiza un análisis de clustering jerárquico para comprender mejor las jerarquías de agrupamiento en los datos y se dividen los datos en 4 clusters.

- **Documento_entrega**: Aquí el documento del proyecto con el siguiente contenido:
  
  - `Introducción`: La pobreza multidimensional afecta a más de 1.2 mil millones de personas en países en desarrollo. En Colombia, se observa una reducción en el índice de pobreza multidimensional en 2023. Entonces se va a analizar datos de vivienda y encontrar relaciones con la pobreza multidimensional.

  - `Materiales y Métodos`: Se explora y preprocesa un conjunto de datos de 93,161 hogares colombianos con 35 variables. Se utilizan varios algoritmos de clustering para el análisis.

  - `Resultados y Discusión`: El análisis revela la importancia de factores ambientales y materiales de construcción en la pobreza multidimensional. Aunque se intenta crear un índice unidimensional, se utiliza una matriz truncada para una mejor interpretabilidad de los datos.

  - `Conclusiones`: Este proyecto sienta las bases para comprender la pobreza multidimensional en Colombia y ofrece perspectivas valiosas para la formulación de políticas públicas efectivas en la lucha contra la pobreza en el país.

- **Video Presentación**: En este link se encuentra el video presenacion del proyecto:
[![Proyecto de Identificación de Patrones de Pobreza Multidimensional en Colombia asociado a las características de las viviendas en los hogares](https://img.youtube.com/vi/ZmPGZZcKcxM/0.jpg)](https://www.youtube.com/watch?v=ZmPGZZcKcxM)

- **README.md**: En este espacio se busca proporcionar una descripción general del proyecto y su estructura.

## Variables disponibles

A continuación se listan las variables disponibles para el análisis:

| Variable                | Descripción                                                                                                            | Tipo de Datos |
|-------------------------|------------------------------------------------------------------------------------------------------------------------|---------------|
| DIRECTORIO              | Número de registro                                                                                                    | int64         |
| SECUENCIA_ENCUESTA      | Consecutivo de la secuencia usada para la encuesta (solo toma el valor de "1")                                      | int64         |
| SECUENCIA_P             | Consecutivo de la secuencia usada para la encuesta (solo toma el valor de "1")                                      | int64         |
| ORDEN                   | Consecutivo de la secuencia usada para la encuesta (solo toma el valor de "1")                                      | int64         |
| REGION                  | Región del país en la cual se tomaron los datos (1 Caribe, 2 Oriental, etc.)                                        | int64         |
| P1_DEPARTAMENTO         | Identificador numérico para cada uno de los departamentos de Colombia                                                | int64         |
| CANT_HOG_COMPLETOS      | Cantidad de hogares completos en una vivienda                                                                         | int64         |
| CANT_HOGARES_VIVIENDA   | Cantidad de hogares en una vivienda                                                                                   | int64         |
| CLASE                   | Clasificación (1 si es cabecera, 2 si son centros poblados, etc.)                                                      | int64         |
| P1070                   | Tipo de vivienda (1 Casa, 2 Apartamento, etc.)                                                                         | int64         |
| P4005                   | Material predominante de las paredes exteriores (1 Bloque, 2 Tapia, etc.)                                              | int64         |
| P4015                   | Material predominante de los pisos (1 Alfombra, 2 Madera, etc.)                                                        | int64         |
| P4567                   | Material predominante del techo o cubierta (1 Plancha de concreto, 2 Tejas, etc.)                                     | int64         |
| P8520                   | Servicios públicos, privados o comunales de la vivienda (variable con errores, tipo object)                           | object        |
| P8520S1                 | Si cuenta con energía eléctrica (1 si sí, 2 si no)                                                                     | int64         |
| P8520S1A1               | Estrato para tarifa de energía eléctrica (valores del 1 al 9 y 0)                                                        | object        |
| P8520S5                 | Si cuenta con acueducto (1 si sí, 2 si no)                                                                           | int64         |
| P8520S3                 | Si cuenta con alcantarillado (1 si sí, 2 si no)                                                                       | int64         |
| P8520S4                 | Si cuenta con recolección de basuras (1 si sí, 2 si no)                                                               | int64         |
| P8520S4A1               | Periodicidad de recolección de basuras (valores del 0 al 9)                                                            | object        |
| P4065                   | Afectación por desastres naturales (variable con errores, tipo object)                                                 | object        |
| P4065S1                 | Inundaciones o desbordamientos de crecientes o arroyos (1 si sí, 2 si no)                                              | int64         |
| P4065S2                 | Avalanchas, derrumbes, deslizamientos (1 si sí, 2 si no)                                                              | int64         |
| P4065S3                 | Hundimiento de terreno (1 si sí, 2 si no)                                                                            | int64         |
| P4065S4                 | Ventarrones, tormenta, vendavales (1 si sí, 2 si no)                                                                 | int64         |
| P5661                   | Problemas ambientales (variable con errores, tipo object)                                                             | object        |
| P5661S1                 | Ruido proveniente del exterior (valores del 1 al 4)                                                                  | int64         |
| P5661S2                 | Malos olores provenientes del exterior (valores del 1 al 4)                                                           | int64         |
| P5661S3                 | Presencia de basuras en las calles (valores del 1 al 4)                                                              | int64         |
| P5661S4                 | Contaminación del aire (valores del 1 al 4)                                                                          | int64         |
| P5661S9                 | Contaminación en ríos, canales, lagos y embalses (valores del 1 al 4)                                                 | int64         |
| P5661S5                 | Invasión del espacio público (valores del 1 al 4)                                                                    | int64         |
| P5661S6                 | Presencia de animales molestos (valores del 1 al 4)                                                                  | int64         |
| P5661S7                 | Presencia de animales molestos (valores del 1 al 4)                                                                  | int64         |
| FEX_C                   | Factor de expansión cuantificado de forma numérica (tipo object)                                                       | object        |

A continuación el mapa de calor de estas variables

![MapaCalor](https://github.com/lauperalta44/aprend_no_supervisado/assets/129508229/65717965-b57a-4c6a-8efa-4cc8b85feca5)

## Instrucciones para Reproducir el Análisis

Si su intención es reproducir el análisis o explorar más a fondo los resultados, sigue estos pasos:

1. Clona este repositorio en tu máquina local utilizando `git clone`.

2. Asegúrate de tener todas las dependencias necesarias instaladas. Puedes encontrar información sobre las bibliotecas requeridas en los comentarios de los archivos de código.

3. Explora los códigos en la carpeta `Código`.

4. Ejecuta los códigos relevantes según tus necesidades.

5. Examina los resultados preliminares que se comentan en el notebook.

6. Si deseas una comprensión completa del estudio, consulta el documento en la carpeta `Documento_entrega`.

## Colaboración

Este proyecto es una oportunidad para involucrarse en la exploración de la pobreza multidimensional en Colombia. Te invitamos a colaborar, hacer preguntas y sumergirte en la búsqueda de respuestas que pueden tener un impacto real en las políticas y en la vida de las personas. Tu participación puede marcar la diferencia.

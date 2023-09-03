# Análisis Multidimensional de la Pobreza en Colombia: Descubriendo Historias en Datos de Vivienda

## Descripción del Proyecto

¡Bienvenidos a nuestro viaje de exploración a través de las complejidades de la pobreza multidimensional en Colombia! En este proyecto, hemos emprendido un recorrido por los datos de vivienda recopilados por el DANE en 2022, con un objetivo en mente: buscar patrones y comprender mejor la realidad de las familias colombianas que enfrentan situaciones de vulnerabilidad.

Este proyecto se basa en datos recopilados de hogares colombianos en la Encuesta Nacional de Calidad de Vida del DANE en 2022. Los datos brutos, disponibles en la carpeta "Datos," son el punto de partida para nuestra exploración. Aquí reside la información que nos ayudará a explorar la pobreza multidimensional en Colombia desde la perspectiva de la vivienda.

## Estructura del Repositorio

El repositorio está organizado de la siguiente manera:

- **Datos**: Esta carpeta contiene los datos de entrada utilizados en el análisis. Incluye la información de la Encuesta Nacional de Calidad de Vida del DANE (2022):
  
  - `Datos de la vivienda.zip`: Archivo comprimido que contiene el CSV de los datos.

- **Código**: Aquí se encuentra el código utilizado en el análisis. El archivo está comentado para facilitar la comprensión:
  
  - `Proyecto Aprendizaje No Supervisado.ipynb`: Código para preprocesar los datos y generar análisis descriptivo de los datos. Incluye la descripción detallada de los datos.

- **Documento_entrega**: Contiene el documento del estudio preliminar que introduce la pregunta a abordar, presenta una revisión preliminar de los antecedentes en la literatura e incluye un resumen de la descripción detallada de los datos. También presenta la propuesta metodológica para abordar la pregunta de interés y la bibliografía.

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

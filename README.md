# Proyecto de Gestión: DataSet de programación de citas de resonancia magnetica en Fundación Valle del Lili.

## Integrantes del Equipo:
Jesus David Franco & Oscar David Ulloa & Angel David Quintero & José Francisco Escudero.


### PROBLEMATICA Y VALOR AGREGADO

La clasificación de si un paciente asistirá o no a una cita de resonancia magnética en Fundación Valle del Lili es crucial para la gestión eficiente de recursos y la atención médica oportuna. La precisión en esta clasificación puede ayudar a reducir costos y tiempos de espera, así como a mejorar la calidad de atención para los pacientes.

La limpieza e imputación de datos en un dataset de este tipo son fundamentales para garantizar la validez y la fiabilidad de los resultados del análisis. La presencia de datos faltantes o erróneos puede distorsionar los patrones y llevar a conclusiones incorrectas. Al completar y corregir estos datos, se pueden obtener análisis más precisos y confiables, lo que facilita la identificación de patrones relevantes para predecir la asistencia a las citas de resonancia magnética. Además, la implementación de un sistema CRUD (Create, Read, Update, Delete) en el conjunto de datos limpiado y corregido es esencial para asegurar una manipulación eficiente y efectiva de los datos. Un CRUD proporciona una interfaz directa para interactuar con el conjunto de datos, permitiendo a los usuarios crear nuevas entradas, leer información existente, actualizar datos y eliminar registros obsoletos. 

### Contenido:

El respositorio contiene dos codigos organizados de manera ordinal, donde se buscará desde una base de datos cualquiera llenada manualmente por usuarios y que contiene cualquier cantidad de errores, hacer su debido procesamiento de limpieza para una optima manipulación y acceso a los datos de manera objetiva a la necesidad que requiera.

- [Limpieza de datos](#Limpieza_de_datos)
- [Manipulación de datos](#Manipulación_de_datos)

Después de aplicar los dos codigos conjuntos, tendremos un acceso pertinente al **Dataset con una cantidad de 29168 registros organizados en 10 variables** , donde desde el segundo archivo, se podrán hacer las manipulaciones controladas a los datos, por medio del CRUD, cuando se desee. Para entender un poco mejor el contenido de nuestro DataSet, debemos acceder al contexto y sus caracteristicas

- [Contexto de los datos](#Contexto_de_los_datos)
- [Caracteristicas necesarias para nuestro DataSet](#Caracteristicas_del_DataSet)



#### Contexto de los datos

Los datos fueron proporcionados por medio de la base de datos de la programación de citas para la utilización del resonador magnético en la Fundación Valle del Lili. Estos datos fueron recopilados desde el año 2015 al año 2020. Dentro del conjunto de datos, la identificación del paciente, sus características y variables que permiten determinar la razón por la modificación de la cita. Además, se maneja una variable objetivo del Tipo de cita, que se clasifica en 'ATENDIDA' y 'CANCELADA', con el fin de determinar si se llevó a cabo la cita programada o no y si se está utilizando el resonandor a una alta eficiencia de trabajo y gastos relacionados. 

#### Caracteristicas necesarias para nuestro DataSet 
Las caracteristicas tomadas en el DataSet son:
* Fecha: Fecha de asignación de la cita, es una variable en formato de fecha. Por ejemplo: 1/2/2018.
* Hora: Hora de la asignación de la cita, esta variable se encuentra en formato de 12 horas. Por ejemplo: 5:00:00 PM.
* Paciente: Identificador interno del paciente en la institución clínica. Es de tipo categórica nominal.
* Motivo de modificación: Variable categórica donde hay múltiples caracteres correspondientes al motivo de modificación de la cita.
* Nombre aseguradora: Nombres de las aseguradoras o EPS de cada paciente.
* Fecha de creación: Fecha de creación del sujeto dentro de la base de datos de la institución clínica.
* Fecha de modificación: Fecha de modificación de las citas en caso de que hayan sido aplazadas. En el caso de que no se haya aplazado la cita, este valor será el mismo que la fecha de asignación de la cita.
* Comentario: Variable categórica donde hay múltiples caracteres correspondientes a comentarios acerca de las características que poseen la cita según el paciente.
* Tipo de cita: Es la variable objetivo, cuya información me indica si el paciente asistió, canceló o se le asignó una cita (esto solo aplica para pacientes a los que no se les ha atendido la cita programada en su momento).



#### Limpieza de datos
HHHHHHHHH

#### Manipulación de datos
HHHHHHHHHHH


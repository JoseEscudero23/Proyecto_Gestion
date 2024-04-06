# Proyecto de Gestión: DataSet de programación de citas de resonancia magnetica.
<p align="center">
  <img src="resonador.jpg" alt="Texto alternativo" width="500"/>
</p>

## Integrantes del Equipo:
Jesus David Franco & Angel David Quintero & José Francisco Escudero.


### PROBLEMATICA Y VALOR AGREGADO

La clasificación de si un paciente asistirá o no a una cita de resonancia magnética en Fundación Valle del Lili es crucial para la gestión eficiente de recursos y la atención médica oportuna. La precisión en esta clasificación puede ayudar a reducir costos y tiempos de espera, así como a mejorar la calidad de atención para los pacientes.

La limpieza e imputación de datos en un dataset de este tipo son fundamentales para garantizar la validez y la fiabilidad de los resultados del análisis. La presencia de datos faltantes o erróneos puede distorsionar los patrones y llevar a conclusiones incorrectas. Al completar y corregir estos datos, se pueden obtener análisis más precisos y confiables, lo que facilita la identificación de patrones relevantes para predecir la asistencia a las citas de resonancia magnética. Además, la implementación de un sistema CRUD (Create, Read, Update, Delete) en el conjunto de datos limpiado y corregido es esencial para asegurar una manipulación eficiente y efectiva de los datos. Un CRUD proporciona una interfaz directa para interactuar con el conjunto de datos, permitiendo a los usuarios crear nuevas entradas, leer información existente, actualizar datos y eliminar registros obsoletos. 

### Contenido:

El respositorio contiene dos codigos organizados de manera ordinal, donde se buscará desde una base de datos cualquiera llenada manualmente por usuarios y que contiene cualquier cantidad de errores, hacer su debido procesamiento de limpieza para una optima manipulación y acceso a los datos de manera objetiva a la necesidad que requiera.

- [Limpieza de datos](#limpieza-de-datos)
- [Manipulación de datos](#manipulación-de-datos)

Después de aplicar los dos codigos conjuntos, tendremos un acceso pertinente al **Dataset con una cantidad de 29168 registros organizados en 10 variables** , donde desde el segundo archivo, se podrán hacer las manipulaciones controladas a los datos, por medio del CRUD, cuando se desee. Para entender un poco mejor el contenido de nuestro DataSet, debemos acceder al contexto y sus caracteristicas

- [Contexto de los datos](#Contexto-de-los-datos)
- [Caracteristicas necesarias para nuestro DataSet](#Caracteristicas-necesarias-para-nuestro-DataSet)

## Conclusiones y generador de valor:
la limpieza de datos y la implementación de un sistema CRUD no solo aseguran la integridad y la calidad de los datos, sino que también mejoran la eficiencia operativa, reducen los riesgos y aumentan la productividad, lo que en última instancia genera valor para la empresa.

##### En cuanto a la limpieza de datos:
La limpieza de datos es fundamental para garantizar la fiabilidad y la precisión en el análisis de datos. Al asegurar que los datos estén libres de errores, inconsistencias y duplicados, se mejora la confianza en los resultados obtenidos a partir de ellos. Esta fiabilidad es crucial en entornos como el sector médico, donde las decisiones pueden tener impactos significativos en la salud de los pacientes y en la eficiencia operativa de la empresa.

Además de la confiabilidad, la limpieza de datos conlleva una mayor eficiencia en los procesos empresariales. Al eliminar la necesidad de corregir datos incorrectos o tratar con registros duplicados, se agilizan los flujos de trabajo y se reducen los tiempos de procesamiento. Esto libera recursos que pueden ser utilizados en actividades más estratégicas y de mayor valor añadido para la empresa.

##### En cuanto a la manipulación de datos (CRUD):
La implementación de un sistema CRUD proporciona una forma intuitiva y eficiente de gestionar datos dentro de la empresa. Permite a los usuarios crear, leer, actualizar y eliminar registros de manera sencilla y directa, sin necesidad de conocimientos técnicos especializados. Esta facilidad de acceso y manipulación de datos aumenta la agilidad de la empresa para adaptarse a los cambios en los datos o en los requisitos del negocio.

La flexibilidad y la adaptabilidad son otros beneficios clave del sistema CRUD. Al permitir cambios instantáneos en los datos según sea necesario, el sistema proporciona a la empresa la capacidad de responder rápidamente a nuevas demandas o situaciones emergentes. Esto ayuda a mantener la relevancia y la eficacia de los procesos empresariales en un entorno en constante evolución.

###### Interfaz grafica

Ahora bien, como modelo de medida para visualizar los datos de una manera estructurada, es importante la simplificación de funciones. No todas las personas tienen acceso al codigo y el conocimiento para su manipulación. Debemos ser inclusivos en la forma de representar cualquier cambio en la base de datos. Para eso se crea la interfaz grafica, que integra la base de datos importada y la función CRUD.
![image](https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/f73983aa-8369-4290-a41c-db276d3bc297)

## ----------------------------------------------------------------------------------------------------------------------------------


#### Limpieza de datos
Desde este apartado, utilizamos la base de datos orginal que se nos otorgó y empezamos a realizar diferentes metodos de procesamiento para dejarla con las variables y patrones necesarios para su posterior manipulación.

Inicialmente se importa la base de datos original.
<img width="850" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/b61c4a19-348a-49e5-bc0c-b9518c2bc76e">

Seguido se hace el proceso de imputación de los datos, en donde se elimina la columna de Motivo_de_modificacion, debido a su alta variabilidad y poca relevancia de acuerdo a los objetivos del proyecto
<img width="928" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/5be87a90-2e9d-4f01-a404-be7226358d96">
Además es necesario, cambiar el tipo de variable para las fechas, que al ser importado se ubican por defecto en Object y si queremos hacer analisis profundo con ellas, debemos hacer el proceso de transformación.
<img width="926" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/f6a2c9fe-cf74-4d29-91d6-996b4b882309">
Otra caracteristica importante es el proceso de anonimización del paciente, ya qué si bien sabemos, es una base de datos real, donde contiene información que puede ser sensible para los pacientes, es de buena practica hacer el encriptamiento de sus identidades.
<img width="924" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/15093a54-f105-4248-a39a-f0e375993a75">
Ahora bien, al ser una base de datos donde los datos se ubicaron abiertamente, se reconoció que existen inmensas filiales de una misma aseguradora, por lo que fue necesario unificarlas en un nombre general de la aseguradora perteneciente y así poder hacer un analisis más detallado y especifico. Repetimos este proceso para todas las que presentaran el mismo caso. Y en el caso de qué se presentaran aseguradoras con menos de 40 personas, se unificaron a una sola denominada "otros"
<img width="709" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/f53fc0da-1d94-4ece-98c8-ceb3b23d5c6a">
<img width="920" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/89c35388-24be-48e1-86c1-cfe4fdaaa1da">
Ahora, hacemos una reducción de los comentarios para solamente quedarmos con los que tengan la palbra Ayuno, ya que son pertinentes para un posible caso de cancelación de cita.
<img width="921" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/e1173f7f-5049-4973-89dc-2c6d9c7153cf">

Terminada la limpieza, se procede a hacer la conexión del MySQL para empezar con la manipulación de los datos.
<img width="920" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/0b6ff6a0-dd25-4feb-accc-fe050a17b20e">



#### Manipulación de datos
Para este segundo codigo, donde ya tenemos una base organizada, iniciamos con la conexión del portal de Sql con el codigo de limpieza de datos. Seguido se implementan las funciones del CRUD que permitan la edición de la Base de datos otorgada al SQL.
Empezamos con la función de crear registros.
<img width="879" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/e754eaa3-d026-4b49-b1d1-2a7c60fd4772">
Seguido de la función de lectura de los registros.
<img width="882" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/36cede20-399c-4364-8587-bd775a9b21f9">
Continuando con la función de actualización del registro.
<img width="882" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/ebcb4a6b-cd72-4aa6-abcd-38afb36839a3">
Y finalmente tenemos la función de eliminación del registro.
<img width="878" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/4eab3aba-a21f-434a-8249-8373db97646d">
Después de aplicar las metricas para el funcionamiento de cada una de las funciones CRUD y hacer ciertas manipulaciones de ejemplos, se hace la descarga de datos.
<img width="881" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/ea719577-88a3-47dc-bc19-b986847871d8">
Finalmente, se hace el proceso para visualización por medio de graficos de los datos que permite poder hacer un tipo de analisis posterior para decisiones futuras.
<img width="877" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/c495c753-8ab4-4fe8-98d2-705f384b239b">
<img width="880" alt="image" src="https://github.com/JoseEscudero23/Proyecto_Gestion/assets/162381147/8352df10-c1cc-4a87-bbc8-5de3ceac4b87">




#### Contexto de los datos

Los datos fueron proporcionados por medio de la base de datos de la programación de citas para la utilización del resonador magnético en la Fundación Valle del Lili. Estos datos fueron recopilados desde el año 2015 al año 2020. Dentro del conjunto de datos, la identificación del paciente, sus características y variables que permiten determinar la razón por la modificación de la cita. Además, se maneja una variable objetivo del Tipo de cita, que se clasifica en 'ATENDIDA' y 'CANCELADA', con el fin de determinar si se llevó a cabo la cita programada o no y si se está utilizando el resonandor a una alta eficiencia de trabajo y gastos relacionados.



#### Caracteristicas originales de nuestro DataSet
Las caracteristicas tomadas en el DataSet original sin hacer el proceso de limpieza respectivo fueron las siguientes:
* Fecha: Fecha de asignación de la cita, es una variable en formato de fecha. Por ejemplo: 1/2/2018.
* Hora: Hora de la asignación de la cita, esta variable se encuentra en formato de 12 horas. Por ejemplo: 5:00:00 PM.
* Paciente: Identificador interno del paciente en la institución clínica. Es de tipo categórica nominal.
* Motivo de modificación: Variable categórica donde hay múltiples caracteres correspondientes al motivo de modificación de la cita.
* Nombre aseguradora: Nombres de las aseguradoras o EPS de cada paciente.
* Fecha de creación: Fecha de creación del sujeto dentro de la base de datos de la institución clínica.
* Fecha de modificación: Fecha de modificación de las citas en caso de que hayan sido aplazadas. En el caso de que no se haya aplazado la cita, este valor será el mismo que la fecha de asignación de la cita.
* Comentario: Variable categórica donde hay múltiples caracteres correspondientes a comentarios acerca de las características que poseen la cita según el paciente.
* Tipo de cita: Es la variable objetivo, cuya información me indica si el paciente asistió, canceló o se le asignó una cita (esto solo aplica para pacientes a los que no se les ha atendido la cita programada en su momento).

Terminado el proceso de limpieza, obtuvimos un DataSet de acuerdo a la necesidad que cumpliría con el objetivo del proyecto, representado por las siguientes variables:
* Fecha
* Hora
* Paciente
* Edad
* Nombre aseguradora
* Fecha de anulacion
* Ayuno (extraido de la columna de comentarios)
* Tipo de cita (Target)




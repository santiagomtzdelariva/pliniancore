# 1.- Añadir Unstructured Nat Hist data (UnstrucNatHistData) #

lo cual convertiría a los elemntos

  1. habit
> 2) life\_cycle
> 3) reproduction
> 4) annual\_cycle
> 5) feeding
> 6) behavior
> 7) interactions
> 8) chromosomic\_number\_n
> 9) molecular\_data
  1. ) migratory\_data
  1. ) ecological\_significance

En virtualmente una extensión de UnstrucNatHistData embebida en el propio FlatPlinian, con consecuencias muy prácticas, tales como --por ejemplo a nivel de portal--que cualquier búsqueda en los campos 1-11 de la lista anterior debe extenderse también al nuevo campo UnstrucNatHistData

//[\*\*Jose Cuadra:\*\* Esto significa dejar los elementos a como están actualmente en el esquema y solo considerar la división dentro del despliegue de los datos dentro del Portal? O más bien, tomar todos los 11 elementos citados anteriormente y eliminarlos del esquema y solo crear 1 elemento \*\*UnstrucNatHistData\*\*  --- //[jcuadra@inbio.ac.cr|Jose Cuadra](.md) 2008/06/13 12:40//
]//


//[\*\*Paco Pando:\*\* No lo tengo del todo claro, pero yo dejaría tan solo 1 elemento: \*\*UnstrucNatHistData\*\*  --- //[Paco Pando](.md) 2008/06/17 17:40 GMT//
]//


//[ Jaime: Desde el punto de vista técnico daría lo mismo tener los 11 elementos separados o agrupados en un campo que yo preferiría llamar "UnestructuredNatualHistory" (sin abreviaciones).  Ahora que se pierde y que se gana, pues..//
  * //Si los agrupamos que perdemos:// Creo que una de las cosas que se pierde es la posibilidad**de hacer búsquedas por algunos campos en particular, ejemplo: buscar especies cuyo cicla de vida sea "XYZ" (donde XYZ son algunas palabras que podrían describir un ciclo de vida). Estas consultas sería más específicas e inclusive tendrían un componente de análisis de datos. Además se pierde la opción de impulsar a los proveedores de datos a tratar de mantener su información lo más esquematizada posible (pensando en que luego se utilice el plinian jerárquico y la tarea vaya avanzada).**(digo la posibilidad porque no está implementado en el portal, pero se perdería la posibilidad de implementarlo a futuro)
  * //Agrupado en "UnestructuredNatualHistory" que ganamos:// : hacer el esquema plano más sencillo y fácil de usar.
  * //Para el usuario final:// Pensando en el usuario final que accede a la información a través del portal, creo que daría casi lo mismo cualquiera de las dos opciones. Si no los agrupamos la informacion se deplegaría separada por subtitulos correspondientes a cada elemento (habit, lifecycle, etc), algunos elementos no tendrán información y otros sí (responsabilidad del proveedor). Si los agrupamos se presentarían los datos juntos y quizás con un adecuado formato si el proveedor utiliza las etiquetas del estilo WIKI para un buen despliegue (de nuevo responsabilidad del proveedor)\\
En fin yo voto por agrupar los once campos en "UnestructuredNaturalHistory"  --- //[Gutierrez Alfaro](Jaime.md) 2008/06/25 05:17 //
]\\

[ Maria Mora: Es difícil lograr el balance perfecto entre lo estructurado (más flexible) y no estructurado (más fácil de utilizar).  Como bien analiza Jaime en las desventajas de agrupar los 11 elementos en uno solo, perderíamos lo que hace interesante estructurar un poco la información y es el poder hacer búsquedas en contexto, poder desplegar la información desagregada, que el usuario pueda seleccionar solo algunas bloques de información que le interesa para generar informes o productos diferentes (desagregar), entre otros beneficios.

Si hacemos un único elemento de estos 11,  estamos incluyendo en un solo campo de texto la mayor cantidad de información asociada a las especies y la más buscada por el público general.  Un usuario interesado en solo información de reproducción, tendría que leer un campo de texto grande para extraer de este la información que le interesa y en algunos casos podría ser que los proveedores de datos ya tuvieran la información estructurada.

Creo que la forma de estructurar la información que se propone es muy utilizada por las personas que generan información (por ejemplo para guias de campo y otros documentos de este tipo). Sin embargo, existe la desventaja que podemos facilmente encontrar casos en que la información que corresponde a dos o más conceptos del FlatPLIC (de estos 11) está en un solo campo, es decir no podemos dejar por fuera la opción de tener todo en un solo campo, pero el punto es hasta a dónde queremos llegar, es decir, de esta forma podemos llegar a la conclusión de que es mejor indexar páginas planas.

Voto por tener los 11 campos y el UnestructuredNaturalHistory y buscar en ambos conjuntos. Luego de contar con algo de información podríamos reevaluar la decisión y evitar la complejidad si la mayoría de los proveedores utiliza un único campo.--- //[mmora@inbio.ac.cr|María Mora] 2008/06/26 17:58// ]

[ Paco Pando: Primero: apoyo la propuesta de Jaime para este nombre, sin abreviaturas.

Segundo: La opción que ofrece María es la que más me gusta, es más trabajo para el portal (para la parte de las búsquedas), es en la práctica tratar "los 11 campos" como una extensión de  UnestructuredNaturalHistory. Este esquema tiene implicaciones que a lo mejor me podéis aclara:

1) ¿Podría haber dos tipos de proveedores unos con "los 11 campos"  y otros con UnestructuredNaturalHistory?

2) Si la respuesta a 1) es sí, entonces ¿no habría que manejar esta diferencia a nivel de los metadatos de cada dataset y abordar el problema en un escenario más abierto donde pueda haber más de un tipo de extensiones?
--- //[|Paco Pando] 2008/06/27 10:58// ]

[ Jaime: Voy a intentar aclarar los dos puntos que menciona Paco.

1) Formalmente no habrá dos tipos de proveedores, pues todo aquel que provea información en el esquema tendrá la capacidad (o posibilidad) de poner datos en los 11 campos en cuestión y/o en el UnestructuredNaturalHistory, es decir **todos** los proveedores de datos serán iguales en ese sentido, en el sentido de las capacidades que tendrían. Ahora en la practica la realidad es que **si** vamos a tener dos tipos de proveedores, porque la pieza de software que este interactuando con el proveedor (digase: harvester, portal, alguna otra cosa) deberá saber si el proveedor tiene datos en "UnestructuredNaturalHistory" y/o en los 11 campos, para saber que despliega y como lo despliega.

2) Es una buena idea... sin embargo preferiría ver como se comporta este caso con información concreta antes de generalizarlo a los demás.

Entonces creo que tendríamos un acuerdo? Dejamos entonces los 11 campos y además un UnestructuredNaturalHistory?
> --- //[jgutierrez@inbio.ac.cr|Jaime Gutierrez Alfaro] 2008/06/27 17:17//]\\

Por nuestra parte, sí. //Paco, 2008/07/01 17:17//

[ Ángela: Acabo de revisar la discusión y de acuerdo, la opción que plantea María es la más salomónica (además posiblemente la más práctica). Ahora, algo muy deseable sería que se mostraran al usuario final únicamente los campos que contienen información (por eso el portal o lo que sea tiene que saber cómo están los datos). ¿Eso es posible?
--- //[|Ángela Suárez M.] 2008/07/02 09:29-5GMT// ]

 Jaime:  En el caso especifico del portal(modificado a partir del de GBIF) si es posible  --- //[jgutierrez@inbio.ac.cr|Jaime Gutierrez Alfaro] 2008/07/02 17:48//
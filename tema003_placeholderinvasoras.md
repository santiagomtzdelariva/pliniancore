# 3.- [AS](AS.md), [FP](FP.md) Se necesita placeholder para invasoras (conexión con el std de GISIN - #
Global Invasive Species Information Network (GISIN)). Esto tiene repercusiones en el PliC jerárquico y en el FlatPliC.

[\*\*Jaime:\*\* Les parece si dejamos el placeholder para invasoras como un campo a discutir para el plic jerárquico (y lo discutimos en otro momento). Digo esto para mantener el plic plano lo mas sencillo posible.  --- //[jgutierrez@inbio.ac.cr|Jaime Gutierrez Alfaro](.md) 2008/06/25 18:53//]

[\*\*Maria Mora:\*\* De acuerdo con Jaime en que lo dejemos para luego.  Hay que tener una lista de puntos a incluir y discutir con el fin de no olvidarlos. --- //[mmora@inbio.ac.cr|María Mora](.md) 2008/06/26 19:08//]


[\*\*Paco Pando:\*\* ¿y no podríamos incluirlo  tanto en el Plinian jeraquico como en el flat si más: \*\*InvasivenessData\*\*, lo incluíos en el portal (considéralo de momento como un ejercicio de PR) y  ya lo trabajamos más adelante? --- //[|Paco Pando](.md) 2008/06/27 10:58// ]


[\*\*Jose Cuadra:\*\* Voy a dar mis "5 centavos" en este tema. De acuerdo a mi entendimiento de lo que se plantea en este hilo de discusión, se quiere hacer algo como //\*\*&lt;xs:element name="InvasivenessData" type="gisin:AlgunElemento"&gt;\*\*// ](.md), donde 'AlgunElemento' sería de tipo de elemento de un esquema externo referenciado por "gisin". Este placeholder sería un elemento que contenga mas elementos dentro de èl (hasta se podría dar el caso de que contenga un árbol de elementos estructurados). Me parece que para la versión Plana del Plinian Core, se debe manejar siguiendo las enseñanzas del Darwin Core, en otras palabras, utilizando extensiones. Así, seguimos con nuestra definición del Plinian Core "core" pensando en una extensión posterior del mismo para Especies Invasoras.
Podríamos tomar como ejemplo la [para interacciones entre especies](http://wiki.tdwg.org/twiki/bin/view/DarwinCore/InteractionExtension|extensión), extensión añadida recientemente al Darwin Core por la gente de la red de Polinizadores de IABIN.
\\
\\
En resumen, mi propuesta: Incluir un elemento 'InvasivenessData' tipo 'String' dentro del Plinian Core Plano y dejar la propuesta de una extensión para especies invasoras, como una futura extensión a desarrollar.
> --- //[jcuadra@inbio.ac.cr|Jose Cuadra] 2008/07/01 23:22// ]

[\*\*Paco: \*\* Eso es, con la salvedad de que la "extensión para especies invasoras" ya existe: http://wiki.tdwg.org/InvasiveSpecies/   --- //[|Paco Pando](.md) 2008/07/02 12:58// ]

[\*\*Ángela: \*\* De acuerdo con que en el flatPlinian debe ir un elemento que conecte con la extensión (que efectivamente ya existe y describe especies). No obstante, habría que precisar el contenido de "InvasivenessData", porque pensando en la GISIN o en la misma IABIN, un reguero de cosas no estructuradas ahí no les va a ser útil (y tampoco es de nuestra estricta competencia ahondar en el tema). ¿Qué tal si solamente se usa como "bandera" para mostrar que la especie es invasora o tiene potencial invasor y ya quien quiera detallar se remite directamente a la extensión?  --- //[amsuarez@humboldt.org.co|Ángela M. Suárez-Mayorga](.md) 2008/07/02 16:36// ]

[\*\*José Cuadra: \*\* Paco, gracias por la información, no sabía que había todo un sitio colaborativo en torno a este tema de las especies invasoras. Al parecer lo tienen bien desarrollado, me parece bien dejar \*\*'InvasivenessData'\*\* como placeholder en el Plinian Core jerárquico, y como un campo \*\*bandera\*\* (String) en el Plinian Core plano. Lo que si veo con este esquema de invasoras, es que van a tener que aplanarlo si alguna vez desean integrar datos de diferentes proveedores (a menos que instalen el BioCASE porque ni DiGIR ni TapirLink soportan mapeos jerárquicos de una manera fácil), pero bueno, será un tema que seguro están desarrollando, no estoy muy enterado sobre ellos.  --- //[jcuadra@inbio.ac.cr|Jose Cuadra](.md) 2008/07/02 23:13// ]

[\*\*Maria Mora: \*\* Perfecto, estoy de acuerdo con las sugerencias, al menos para esta versión y luego lo evaluamos: dejar InvasivenessData como placeholder en el Plinian Core jerárquico, y como un campo bandera en el Plinian Core plano.  --- //[mmora@inbio.ac.cr|María Mora](.md) 2008/07/09 20:11// ]

Jaime: ya agregue el campo al esquema plano2.3, que se puede observar en la pagina principal del wiki. Ahora creo que podriamos escribir un poco documentacion adecuada del campo en este link [PlinianCore\_InvasivenessData|InvasivenessData]  --- //[jgutierrez@inbio.ac.cr|Jaime Gutierrez Alfaro] 2008/07/11 17:31//
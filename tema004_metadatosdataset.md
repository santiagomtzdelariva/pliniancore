# 4. Metadatos #

> El elemento 'Metadata'que aparece en el PLIC jerárquico.
> > `ASM-FP-- Debería estár incluído en el FlatPlinian y ser obligatorio. Si no, no hay manera de saber a qué conectarse.`

Hace falta incluir elementos para dar cuenta de los metadatos del data set, y además han e ser obligatorios, estos serían:  Description, IconUri, Scope, Version, RevisionData, Owners, IPRStatements, Source. Lo que no tengo tan claro es si estos han de ir en cada registro o en un fichero aparte.

Hablando con Silvia, parece que el que los metadatos vayan en un fichero aparte da la posibilidad a que estos se manejen como un catálogo de metadatos tipo UDDI, lo que lo hace más sencillo y flexible en cuanto a su visualización y consulta.

¿Cabría la posibilidad de que fuera en el FlatPlinian un hipervínculo al metadato documentado (con la posibilidad de que fuera a cualquier catálogo de metadatos)?

[ Jose Cuadra: A ver si hago una distinción, talvez Silvia me ayude con esto. El protocólo TAPIR ya brinda elementos del data set al cual se está consultando. Estos metadatos se ingresan a la hora de configurar el TapirLink (como la instalación que se hizo en España)
\\
\\
Algunos de los elementos que brinda el TAPIR son: Descripcion, Cita bibliografica, Derechos, Lenguaje de los datos, Entidades que participan del dataset (por ejemplo, INBio-dueño de datos), y tambien Contactos del dataset (por ejemplo, Paco Pando-data administrator...y...Silvia Lusa-system administrator)
\\
\\
Todos los elementos que devuelve el TAPIR estan aca:
[http://www.tdwg.org/dav/subgroups/tapir/1.0/docs/TAPIRSpecification\_2008-02-07.html#toc40](http://www.tdwg.org/dav/subgroups/tapir/1.0/docs/TAPIRSpecification_2008-02-07.html#toc40)
\\
\\
Así, considero que lo mejor es separar lo que son datos "core" de la especie,  de los datos "core" del dataset, pues ambos se podrían extraer de mecanismos diferentes (Datos de especies --> Plinian Core, Datos del dataset --> Tapir Metadata), y así mantenemos una división entre ambos. 'InstitutionCode' será el único elemento que haría algun tipo de referencia al huesped de la información
\\
\\
Entonces propongo dejar solamente 'InstitutionCode' y extraer los demás elementos de la consulta de tapir por metadatos. Que les parece?
\\

> //--- [jcuadra@inbio.ac.cr|Jose Cuadra] 2008/06/25 19:38//
]

[ Paco Pando:
Me gusta. Solo echo en falta "version" pero se puede manejar con "Title", por otra parte elementos como institución, autor, colaboradores, editores, etc se pueden manejar bien con  "RelatedEntities"…. A ver que dice el SiB--- //[Pando](Paco.md) 2008/06/27 10:58// ]

[ Paco Pando:
Tengo un "pero". Puestos a dejar un elemento que haga referencia a todo el juego de datos en cada registro, yo dejaría el nombre del juego de datos, esto es el equivalente a "CollectionCode" de DarwinCore o al ("Title" de Plinian Core 2.0; en Dataset > Metadata >  Description > Title) ¿Sustituimos "InstitutionCode" por "Title"? Una iNstitución o entidad puede tener más de un juego de datos de Plinian… --- //[Pando](Paco.md) 2008/06/27 10:58// ]

[ Jose Cuadra:
El Plinian Core Flat que modificamos en España, le incluímos un elemento 'Version', pero no sé si este será el mismo 'Version' que usted quiere Paco, pues creo que el 'Version' que tiene actualmente el Plinian Core es sobre la versión del registro de especie propiamente. Pero me imagino que se podría resolver con "Title" como lo plantea.  --- //[jcuadra@inbio.ac.cr|Jose Cuadra] 2008/06/28 00:10//]

[ Jose Cuadra:
Acerca de utilizar 'Title' por 'InstitutionCode' yo no le veo problema en hacer el cambio. Solo que el único asunto es que este campo debe contener un identificador unico por institución , por ejemplo INB para INBio, GBIFES para GBIF.ES, MNCR para Museo Nacional de Costa Rica, y así sucesivamente. También, como calzamos la 'Version' dentro de este elemento 'Title'?  --- //[jcuadra@inbio.ac.cr|Jose Cuadra] 2008/06/28 00:26// ]

[ Paco Pando:
Yo pensaba mas bien que "InstitutionCode" quedara como metadato del Tapir, y que en  'Title' tuvieramos el nombre del juego de datos...Respecto de 'Version', si este elemento ya está a nivel de registro, perfecto y entonces podría quedar la versión del juego de datos como parte del título (o del plinian, o de los metadatos del Tapor, o--más probablemente-- en los dos  --- //[Paco](Paco.md) 2008/07/01 17:26// ]

[ Jose Cuadra:
Pero entonces dejamos "Title" y "Version" como elementos del Plinian Core? //(en este caso, estos dos elementos deberian ser asociados a la hora de //mapear// los registros de especies con los registros del PLiC plano.)// Y dejamos "InstitutionCode" para que sea manejado con la información que el TAPIR brinda sobre metadatos. //(en este caso, el responsable sería el que instala el software TAPIR a la hora de configurar dicho proveedor)//     --- //[jcuadra@inbio.ac.cr|Jose Cuadra] 2008/07/01 23:38// ]

[ Ángela: Ups! Creo que me perdí del rumbo de la discusión. Para intentar aclararme, consideración 1): según la licencia de uso del portal de especies de SSTN, por ejemplo, se debe retener por cada registro el identificador del propietario de los datos, así como la colección específica dentro de una institución (porque una institución puede proveer diferentes conjuntos de datos de especies). ¿Eso equivaldría a "InstitutionCode" y "CollectionCode", entendiendo "Collection" como "dataset", cierto? Consideración 2): Igual da identificar el dataset con el nombre ("Title"?), como dicen, y como efectivamente se ve (no sé cómo se guarde). Pero, Paco echa en falta la versión. Consideración 3): independientemente de dónde se guarden los metadatos del dataset deben evidentemente estar separados de los datos de la ficha, y contendrían la versión del conjunto de datos, ¿cierto? Entonces, preguntas concretas:
> - ¿Podemos prescindir de "Version" en el Flat Plinian?;
> - ¿No es más fácil y transparente que sólo haya un campo de metadatos para cada registro de especie, siempre que cumpla con las condiciones de la consideración 1?
> - Como no sabemos dónde se van a guardar los metadatos de los datasets (puede haber mil catálogos de metadatos como los nuestros, o registros UDDI o no sé qué montón de cosas...¿podría ser un hipervínculo al metadato del conjunto de datos (donde quiera que se guarde), lo que se incluya en el Flat Plinian? Es que creo que esa pregunta no se contestó.
> --- //[amsuarez@humboldt.org.co|Ángela M. Suárez-Mayorga] 2008/07/02 16:49//]


[ Jose Cuadra: Voy a responder a continuación. La respuesta es un poco extensa para ver si todos vamos en la misma linea.
\\
\\
Creo que ya estamos de acuerdo en que los metadatos del proveedor son diferentes a los datos del esquema (Plinian Core, por ejemplo). Ahora, actualmente el Plinian Core maneja el campo InstitutionCode para cada uno de los registros. Ahora, a nivel de metadatos del proveedor (fuera del Plinian Core), se manejan estos elementos de información:

| Proveedor de Datos y Recurso de Datos en el caso de DiGIR |
| Title en el caso de TAPIR. (Se podría hacer la analogía con "Proveedor de Datos") |

Así, encontramos:

PROVEEDOR DE DATOS --> Círculo Herpetológico de Panamá
> RECURSO DE DATOS --> Datos de los Especimenes de Anfibios y Reptiles del Círculo Herpetológico de Panamá.

PROVEEDOR DE DATOS --> Ministerio de recursos naturales y ambiente - MARENA
> RECURSO DE DATOS --> Insectos de Nicaragua - MEL
> RECURSO DE DATOS --> Plantas de Nicaragua-HULE

PROVEEDOR DE DATOS --> Museo de Historia Natural Marina de Colombia - INVEMAR
> RECURSO DE DATOS --> INVEMAR database (MHNMC) for IABIN

A nivel de Base de Datos de un portal, se hace una union entre todos estos elementos y por ejemplo, para un registro de especie, se tendrán los campos DATA\_PROVIDER, DATA\_RESOURCE, INSTITUTION\_CODE. Es por esto, que me parece correcto dejar solamente 'InstitutionCode' (o 'Title') en el Plinian Core y dejar que TAPIR maneje los demas metadatos. Lae separación de estos datos para el usuario no es una separación real, pues lo que le interesa al usuario es visualizar estos datos en un portal, el cual tendrá esos 3 elementos.

En relación al campo 'Version', Paco planteo que estuviera a nivel de registro. Personalmente desconozco si se guardan versiones de registros de especies, algo asi como:  Inga vera/1998/Version1  ...  Inga vera/2000/Version2  ...  Inga vera/2008/Version3. Si éste es el caso, entonces veo necesaria la inclusión de 'Version' como parte del Plinian Core. Para la 'Version' del Recurso de Datos, planteo que se maneje a nivel de metadatos de TAPIR. (En el campo 'Descripcion' de los metadatos del TAPIR?)

Hay una premisa en todo esto, y es que los datos de especies de cada proveedor existen, y no se les puede exigir a los proveedores que tengan que añadirle campos a los registros de especies que ya tengan. Es por esto que se crearon los metadatos de TAPIR, para poder "factorizar" esta información y solo tener que introducirla 1 sola vez y que todos los registros de esa colección queden ligados con esos metadatos. Me doy a explicar? Estos metadatos uno los ingresa a la hora de configurar el proveedor de datos; a la hora de instalar la herramienta de software y exponer los datos ya existentes de especies.

A como vá la discusión, tenemos un elemento 'Title' dentro del Plinian Core, y en los metadatos del Proveedor TAPIR, otro elemento 'Title'.  Como se vé esto? Dejamos un elemento 'InstitutionCode' en el PliCore y dejamos el 'Title' para los metadatos? Nos quedamos con un elemento 'Version' dentro del PLicore? y también manejamos la version del proveedor con los metadatos del Proveedor?

| Plinian Core | Metadatos TAPIR |
|:-------------|:----------------|
| InstitutionCode | Title |
| Version | Descripcion (que contenga Version y otras) |

o bien


| Plinian Core | Metadatos TAPIR |
|:-------------|:----------------|
| Title | Title |
| Version | Descripcion (que contenga Version y otras) |

Espero haberme explicado bien, quedo abierto a sugerenciaas.  --- //[jcuadra@inbio.ac.cr|Jose Cuadra] 2008/07/02 23:06// ]

[ Maria Mora: despues de todo lo expuesto voto por:
| Plinian Core | Metadatos TAPIR |
|:-------------|:----------------|
| InstitutionCode | Title |
| Version | Descripcion (que contenga Version y otras) |

Me parece más representativo llamar al código de la institución InstitutionCode y para algunos proveedores de datos la versión del registro es importante por lo que yo mantendría el concepto versión. Adicionalmente, me parece muy interesante la propuesta de Ángela de mantener en el esquema un puntero a los metadatos con esto si el esqueama se utiliza con otro protocolo que no sea Tapir estaría contemplada la opción de acceso a los metadatos, esto podemos discutirlo para la próxima versión.]
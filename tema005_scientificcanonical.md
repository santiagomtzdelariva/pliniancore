# 5. Sobre los elementos ScientificName, CanonicalName y CanonicalAuthorship #

Sobre: El elemento 'ScientificName' cambia de nombre a 'CanonicalName' (para seguir la nomenclatura del esquema jerárquico)
\\
> FP ---Yo lo dejaría como  ScientificName

Sobre: El elemento 'AuthorYearOfScientificName' cambia de nombre a 'CanonicalAuthorship' (para seguir la nomenclatura del TCS)
> FP---Esto hay que verlo en combinación con lo anterior (dejarlo como está)

\\


[ Jose Cuadra: Voy a plantear el por qué se propuso este punto. Como es sabido, actualmente solo está ScientificName dentro del esquema. Este nombre ScientificName puede venir sin o con el nombre del autor junto al nombre cientifico. Lo que se pensó fue en hacer una división del nombre científico en CanonicalName y CanonicalAuthorship, pero siempre dejando el ScientificName como un elemento extra. Esto abarcaría tres opciones de formato de datos en los proveedores. Se listan a continuacion:
\\ \\
  * Si el proveedor solo posee un campo NombreCientifico en donde tiene el nombre cientifico junto al nombre del autor, entonces este proveedor utilizaria el campo 'ScientificName' y dejaria los campos 'CanonicalAuthorship' y 'CanonicalName' sin llenar.
\\ \\
  * Si el proveedor posee un campo en donde guarda el NombreCientifico y otro campo en donde guarda el NombreDelAutor, entonces utilizaría los campos 'CanonicalAuthorship' y 'CanonicalName' y dejaría sin llenar el campo 'ScientificName'.
\\ \\
  * Si el proveedor posee solo el nombre cientifico sin autor, entonces llenaría solamente el campo 'CanonicalName' y dejaría vacios los campos 'CanonicalAuthorship' y 'ScientificName'.
\\ \\
Así, esto consideraría todas las posibles combinaciones de formatos desde el proveedor en torno al nombre cientifico. Si se optara por esta propuesta, habría que considerar cuales de ellos serán elementos obligatorios.

Pero igual, dejar solamente el elemento 'ScientificName' me parece también otra buena opción, tal y como lo usa el Darwin Core. Este punto es mejor que se defina de acuerdo a qué formato es el que usan la mayoría de los proveedores de datos.

> --- //[jcuadra@inbio.ac.cr|Jose Cuadra] 2008/06/25 19:38//
]
\\
\\

[\*\*Maria Mora:\*\* El problema que le veo a nuestra propuesta es que el ScientificName debería ser obligatorio y como lo estamos planteando no es posible definir la obligatoriedad del concepto en el esquema. De acuerdo con Paco.  --- //[mmora@inbio.ac.cr|María Mora](.md) 2008/06/26 19:15//]

\\
\\

[\*\*Paco Pando:\*\* Yo no haría coexistir Scientific Name y Canonicalname y CanonicalAuthorshio (sería como que los dos últimos fuesen una extensión del primero). Si en cambio seguiría la norma  de DarwinCore:  ScientificName + ScientificNameAuthor; (obligatorio el primero) --- //[|Paco Pando](.md) 2008/06/27 10:58// ]

\\
\\

[\*\*José Cuadra:\*\* Me parece bien dejar ScientificName y AuthorYearOfScientificName. El Darwin Core en su [http://wiki.tdwg.org/twiki/bin/view/DarwinCore/DarwinCoreVersions|version 1.2 y 1.21](.md) manejaba ScientificName y ScientificNameAuthor. En su version 1.4 fue cuando se hizo el cambio a ScientificName y AuthorYearOfScientificName. Me parece que lo mejor entonces es dejar el plinian core flat con los elementos ScientificName y AuthorYearOfScientificName o como Paco plantea, ScientificName y ScientificNameAuthor  --- //[jcuadra@inbio.ac.cr|Jose Cuadra] 2008/06/28 00:31// ]

[\*\*Paco Pando: \*\* Usamos los nombres de DwC 1.4 y listo. //Paco 2008/07/01 17:26// ](.md)

[\*\*Àngela: \*\* Sì, también de acuerdo en que un único campo con el criterio DwC es el mejor.  --- //[amsuarez@humboldt.org.co|Ángela M. Suárez-Mayorga](.md) 2008/07/03 18:46//]

[\*\*Maria: \*\* de acuerdo. --- //[mmora@inbio.ac.cr|María Mora](.md) 2008/07/10 19:18//]
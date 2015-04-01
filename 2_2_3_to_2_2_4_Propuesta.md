# Propuesta 2.2.3 --> 2.2.4 #

http://www.pliniancore.org/test/pl_corev2.2.4.xsd

1) Se eliminaron los elementos 'SpeciesPageAuthor' y 'CoAuthors' y se creó el elemento 'Creators' con su respectiva documentación. (la intención es seguir lo propuesto en el esquema jerárquico sobre elementos de Dublin Core)

2) El elemento 'Collaborators' cambia de nombre a 'Contributors' (propuesto sobre lo de Dublin Core)

3) El elemento 'PublicationDate' cambia de nombre a 'DateCreated' (para seguir la nomenclatura del esquema jerárquico)

4) Se inserta el elemento 'GlobalUniqueIdentifier' con su respectivo comentario.

5) El elemento 'ScientificName' cambia de nombre a 'CanonicalName' (para seguir la nomenclatura del esquema jerárquico)


6) El elemento 'AuthorYearOfScientificName' cambia de nombre a 'CanonicalAuthorship' (para seguir la nomenclatura del TCS)

7) El elemento 'SpeciesPublicationReference' cambia de nombre a 'PublishedIn'.

8) Se eliminan los elementos 'TypeCollector', 'TypeLocation', 'TypeDepository' y se crea un nuevo elemento 'Typification' (aquí se piensa que se debería crear una extensión para el Plinian Core)

9) El elemento 'Endemism' cambia de nombre a 'Endemicity (para seguir la nomenclatura del esquema jerárquico)

10) El elemento 'Countries' se elimina y se incluye en 'Distribution'. No hay obligatoriedad del elemento 'Distribution'.

11) El elemento 'DateLastModified' se cambia a 'DateModified'.

Propuesta
> Eliminar los elementos 'UnstructuredDocumentation' y 'Papers' y dejar solamente los elementos 'OtherInformationSources' y 'References'.
> Aquí se considera que 'UnstructuredDocumentation' y 'Papers' deberían ser parte de 'OtherInformationSources'.


Propuesta
> En relación a los puntos 5)CanonicalName y 6)CanonicalAuthorship se piensan las siguientes opciones:
> opcion a) Dejar los elementos "CanonicalName" y "CanonicalAuthorship" a como están.
> opcion b) Dejar solamente el "CanonicalName". Si viniera un autor, concatenar el nombre cientifico y el autor en una sola
> > tira y representarla como el elemento "CanonicalName"

> opcion c) Dejar la tira "ScientificName", "CanonicalName" y "CanonicalAuthorship" para considerar todos los casos. Por
> > ejemplo, si el proveedor solo posee un nombre científico sin año ni autor, entonces iría en el campo "CanonicalName" y
> > los campos "ScientificName" y "CanonicalAuthorship" se dejaría en blanco. Si viene el nombre científico junto al autor
> > en una misma columna, entonces se rellenaría el campo "ScientificName" y los demás se dejarían vacios. Si viene el
> > nombre científico en una columna y el autor en otra, entonces se utilizarían los campos "CanonicalName" y "CanonicalAuthorship"
> > y se dejaría "ScientificName" en blanco.

> opcion d) Dejar solamente el elemento "ScientificName" y continuar como estaba en la versión 2.2.3
> opcion e) Otra?




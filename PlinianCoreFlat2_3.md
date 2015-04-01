# Plinian Core Flat2.3 #

## Descripción de Archivos ##

  * [Esquema](http://www.pliniancore.org/test/PlinianCoreFlat2-3.xsd): Este está definido en un archivo .xsd, el cual es necesario para para configurar el TapirLink adecuadamente. En esta versión del esquema se evita el uso del "PlicElement" utilizado en versiones anteriores y que obligaba a hacer unas modificaciones al TapirLink para que funcionara correctamente. A partir de este versión se utiliza el "DwElement", por lo tanto no hay problemas con utilizar el TapirLink en su versión estándar.

  * [Output Model](http://www.pliniancore.org/test/PlinianCoreFlat2-3-OutputModel.xml): Se recomienda la utilización de este "Output Model" para estandarizar los resultados a las consultas realizadas al proveedor de datos.

  * [Estructura para OutputModel](http://www.pliniancore.org/test/PlinianCoreFlat2-3-StructureForOutputModel.xsd): Este archivo es necesario por el OutputModel. Separando la estructura del OutputModel se evita saturar ese archivo y mantener modularidad.




## Instalación y Configuración de un Proveedor [con Plinian Core Flat2.3](TapirLink.md) ##

Esta parte no pretende ser una guía sino solo contarles como me fué en eso --- //[jgutierrez@inbio.ac.cr|Jaime Gutierrez Alfaro] 2008/07/12 19:37//

Software Utilizado:
  * TapirLink
  * Apache
  * PHP5
  * MySQL


Instalación en Ubuntu 8.04 [Instalación recomendada ;-) ](.md) --- //[jgutierrez@inbio.ac.cr|Jaime Gutierrez Alfaro] 2008/07/12 19:40//]\\
La versión de Tapir Link en este caso fue la 0.6.0 (revisión 660) y para los otros programas se utilizó la última versión disponible en los repositorios. En un primer caso intenté utilizar PostgreSQL en vez de MySQL pero tuve problemas con el plugin de PHP5, entonces recurrí a MySQL, revisando esa pulga no debería haber problemas en utilizar cualquiera de los dos motores de BD.\\

Instalacion de apache2

`$sudo apt-get install apache2`

Instalacion de php5 y su modulo para apache2

`$sudo apt-get install php5 libapache2-mod-php5`

Por algún motivo se dieron problemas con las sesiones. Por lo tanto se decidió modificar la dirección de la carpeta donde se almacenan las sesiones en PHP y apache2. La dirección que viene predefinida es "/var/lib/php5" y aunque en el archivo de configuración esta viene comentada es mejor definirle una nueva dirección, la cual sería "/tmp". El archivo a modificar es: /etc/php5/apache2/php.ini\\
Justo donde dice:

`;session.save_path = /var/lib/php5`

Se debe reemplazar con:

`session.save_path = /tmp''`

El archivo de configuración de apache esta ubicado en "/etc/apache2/httpd.conf". Ahí se le indica a apache que puede "ver" y que no, para que vea a Tapir debe agregarse unas cuantas lineas. Suponiendo que la variables $TAPIRLINK va a apuntar al directorio donde fue descomprimido TapirLink (Ejemplo: si descomprimí TapirLink en /var/www/tapirlink-0.6.0 entonces escribir eso donde diga $TAPIRLINK). Entonces en el archivo /etc/apache2/httpd.conf debería decir algo así:
```
Alias /tapirlink "$TAPIRLINK/www"
    
    <Directory "$TAPIRLINK/www">
        Options Indexes MultiViews
        AllowOverride None
        Order allow,deny
        Allow from all
    </Directory>

Alias /tapirlink-admin "$TAPIRLINK/admin"
    
    <Directory "$TAPIRLINK/admin">
	Options Indexes MultiViews
        AllowOverride All
        Order allow,deny
        Allow from all
    </Directory>
```

jaime: Claramente a esto se le puede hacer mejoras a nivel de seguridad... comentarios son más que bienvenidos --- //[jgutierrez@inbio.ac.cr|Jaime Gutierrez Alfaro] 2008/07/12 19:55//

En este punto ya debería servir el TapirLink, sin ningún recurso configurado.

Instalación del soporte de PHP5 para MySQL

`$sudo apt-get install php5-mysql`

Agregar el Recurso
Utilizar el driver: "MySQL using newer PHP5 API",
Cuando se solicita el datasource dejarlo en blanco, solo ingresar el Username, password y nombre de la BD.\\

Cuando se solicita la localización del esquema utilizar: "http://www.pliniancore.org/test/PlinianCoreFlat2-3.xsd" y en el formato seleccionar: "new darwin core".\\

Luego simplemente mapear los conceptos.

Nota:
  * Se adjunta un script de BD para crear una tabla con la cual se puede mapear el esquema para hacer pruebas.  [acá](Esta.md)
jaime: No supe como subir el archivo, entonces lo copio acá  --- //[jgutierrez@inbio.ac.cr|Jaime Gutierrez Alfaro] 2008/07/12 20:22//
```
create table flat2_3 (
        id int unsigned NOT NULL auto_increment

     ,  scientific_name varchar(255) not null
     ,  institution_code varchar(255) not null
     ,  date_last_modified varchar(255) not null
     ,  taxon_record_id varchar(255) not null
     ,  language varchar(255) not null
     ,  creators varchar(255) not null
     ,  distribution text default NULL
     ,  abstract text default NULL
     ,  kingdom varchar(150) default NULL
     ,  phylum varchar(150) default NULL
     ,  class varchar(250) default NULL
     ,  order_rank varchar(50) default NULL
     ,  family varchar(250) default NULL
     ,  genus varchar(150) default NULL
     ,  synonyms text default NULL
     ,  author_year_of_scientific_name varchar(255) default NULL
     ,  species_publication_reference text default NULL
     ,  common_names text default NULL
     ,  typification text default NULL
     ,  global_unique_identifier varchar(255) default NULL
     ,  contributors text default NULL
     ,  date_created varchar(255) default NULL
     ,  habit text default NULL
     ,  life_cycle text default NULL
     ,  reproduction text default NULL
     ,  annual_cycle text default NULL
     ,  scientific_description text default NULL
     ,  brief_description text default NULL
     ,  feeding text default NULL
     ,  behavior text default NULL
     ,  interactions text default NULL
     ,  chromosomic_number_n text default NULL
     ,  molecular_data text default NULL
     ,  population_biology text default NULL
     ,  threat_status text default NULL
     ,  legislation text default NULL
     ,  habitat text default NULL
     ,  territory text default NULL 
     ,  endemicity text default NULL
     ,  the_uses text default NULL
     ,  the_management text default NULL
     ,  folklore text default NULL
     ,  the_references text default NULL
     ,  unstructed_documentation text default NULL
     ,  other_information_sources text default NULL
     ,  papers text default NULL
     ,  identification_keys text default NULL
     ,  migratory_data text default NULL
     ,  ecological_significance text default NULL
     ,  unstructured_natural_history text default NULL
     ,  invasiveness_data text default null
     ,  target_audiences text default null
     ,  version text default null
     ,  url_image1 varchar(1000) default NULL
     ,  caption_image1 varchar(1000) default NULL
     ,  url_image2 varchar(1000) default NULL
     ,  caption_image2 varchar(1000) default NULL
     ,  url_image3 varchar(1000) default NULL
     ,  caption_image3 varchar(1000) default NULL
     ,  PRIMARY KEY  (id)
) ENGINE=MyISAM DEFAULT CHARSET=latin1;
```

## Hacer Consultas al Proveedor ##

Acceder a al cliente de tapirLink que usualmente está(cambiando localhost por el lugar donde se instaló) en: http://localhost/tapirlink/tapir_client.php Luego seleccionar la opción de Búsquedas y en el cuadro donde va la consulta escribir alguna de las siguientes(o mejor, copiar y pegar).

Consulta normal
```
<?xml version="1.0" encoding="UTF-8" ?>
<request 
    xmlns="http://rs.tdwg.org/tapir/1.0"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://rs.tdwg.org/tapir/1.0 
                        http://rs.tdwg.org/tapir/1.0/schema/tapir.xsd">
  <header>
    <source sendtime="2005-11-11T12:23:56.023+01:00">
      <software name="tapir_client.php" version="1.0"/>
    </source>
  </header>
  <search count="true" start="0" limit="20" envelope="true">
    <outputModel>
      <structure>
        <xs:schema targetNamespace="http://example.net/simple_specimen" xmlns:xs="http://www.w3.org/2001/XMLSchema" xsi:schemaLocation="http://www.w3.org/2001/XMLSchema http://www.w3.org/2001/XMLSchema.xsd">
          <xs:element name="records">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="record" minOccurs="0" maxOccurs="unbounded" type="unitType">
                </xs:element>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:complexType name="unitType">
            <xs:sequence>
              <xs:element name="name" type="xs:string"/>
              <xs:element name="crea" type="xs:string"/>
            </xs:sequence>
          </xs:complexType>
        </xs:schema>
      </structure>
      <indexingElement path="/records/record"/>
      <mapping>
        <node path="/records/record/name">
          <concept id="http://www.pliniancore.org/plic/pcfcore/ScientificName"/>
        </node>
        <node path="/records/record/crea">
          <concept id="http://www.pliniancore.org/plic/pcfcore/Creators"/>
        </node>
      </mapping>
    </outputModel>
    <filter>
        <not>
          <isnull>
            <concept id="http://www.pliniancore.org/plic/pcfcore/ScientificName"/>
          </isnull>
        </not>
     </filter>
  </search>
</request>
```

Consulta al estilo del Portal
Esta consulta simula una consulta tal como la haría el Portal (IABIN, GBIF.ES). Si esta consulta funciona en el proveedor es muy probable que el Portal sea capaz de acceder a la información proveída.

```
<?xml version="1.0" encoding="UTF-8" ?>
<request 
    xmlns="http://rs.tdwg.org/tapir/1.0"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://rs.tdwg.org/tapir/1.0 
                        http://rs.tdwg.org/tapir/1.0/schema/tapir.xsd">
  <header>
    <source sendtime="2005-11-11T12:23:56.023+01:00">
      <software name="tapir_client.php" version="1.0"/>
    </source>
  </header>
  <search count="true" start="0" limit="20" envelope="true">
    <externalOutputModel location="http://www.pliniancore.org/test/PlinianCoreFlat2-3-OutputModel.xml"/>
    <filter>
        <not>
          <isnull>
            <concept id="http://www.pliniancore.org/plic/pcfcore/ScientificName"/>
          </isnull>
        </not>
    </filter>
  </search>
</request>
```

jaime: Esto esta funcionando bastante bien, solo falta determinar porque (en mi caso) me está dando 3 warnings al hacer la consulta, pero aún con eso no hay problema.






## Archivos Adjuntos ##

  * [Plantilla de la Base de datos para Microsoft Access (comprimida)](http://www.gbif.es/plinian/lib/exe/fetch.php?id=pliniancoreflat2_3&cache=cache&media=plicflat2_3_dbv2_3_.zip)

Nota: Esta base de datos que se ofrece no sigue la nomenclatura de nombres utilizada en bases de datos, pues se encuentra optimizada para que se pueda realizar el auto mapeo en el tapirlink.
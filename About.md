Based on the poster presented at TDWG 2013. Fiorenze http://purl.org/pliniancore/posterTDWG2013

# Abstract #

> Plinian Core aims to be a standard for sharing information mainly at the species level. It was conceived as a way to publish species information and to make it interoperable. By “species information” we refer to all kinds of properties and traits related to taxa (of any rank), including descriptions, nomenclature, conservation status, management, natural history, etc. Thus, Plinian Core coverage goes beyond taxonomic descriptions.
> The objective of this poster is to present the process and advances of the conceptual development of Plinian Core v3.1 (abstract model) and its implementation (application profiles).


> ![http://img822.imageshack.us/img822/7586/h309.jpg](http://img822.imageshack.us/img822/7586/h309.jpg)

> The development of Plinian Core has been leaded by the National Institute of Biodiversity (INBio, Costa Rica), the Spanish Node of GBIF (GBIF Spain), the University of Granada (UG, Spain), the Alexander von Humboldt Institute (IAvH , Colombia), the National Commission for the Knowledge and Use of Biodiversity (Conabio, Mexico) and the University of Sao Paulo (USP, Brazil). This group reviewed the existing data standards to reuse as many elements as possible and avoid redundancy.

> Plinian Core design requirements included to be  easy to use, self-contained, able to support  data integration from multiple databases, and ability to handle different levels of granularity. The current version of Plinian Core specifically supports species pages publication reasonably well, it is structured in 18 classes (i.e. complex elements) and it is well-documented:

> •	Abstract Model: (https://purl.org/pliniancore/am_v3.1)<br>
<blockquote>•	Application Profile (<a href='https://purl.org/pliniancore/ap_v3.1'>https://purl.org/pliniancore/ap_v3.1</a>)<br></blockquote>


<blockquote>Plinian Core is currently used by the institutions mentioned above and the Chilean Ministry of Environment. Now we aim to make Plinian Core a truly global standard by bringing together teams and institutions from all over the world under the umbrella of TDWG.</blockquote>


<h1>History</h1>


<blockquote>A previous version of Plinian Core, know as “Plinian Core Flat”, consisted  of a plain list of elements to represent the information associated to any given taxon. Limitations of this approach were evident and a new development was impulse to overcome them.</blockquote>


<blockquote>As a result of the process started in 2012, a new version, Plinian Core v3.1 was defined. This  provides more flexibility to fully represent the information of a species in a variety of scenarios. New elements to deal with aspects such as IPR, related resources, referenced, etc. were introduced, and elements already included were better-defined and documented.</blockquote>

<blockquote><img src='http://img138.imageshack.us/img138/36/wpkg.jpg' /></blockquote>


<blockquote>Other new features are the possibility to represent each element in unstructured or structured terms,  and attach provenance, references, or license information to them.</blockquote>

<blockquote><img src='http://img46.imageshack.us/img46/8936/no02.jpg' /></blockquote>


<h1>Other standards</h1>

<blockquote>Plinian Core v3.1 incorporates a number of elements already defined within standards in use. This is an important consideration in advancing towards robust semantic web architecture for biodiversity information. The following table depicts the relationships between other standards and the elements used by Plinian Core v3.1:</blockquote>


<table><thead><th>Standard</th><th>List of elements</th><th>url</th></thead><tbody>
<tr><td>EML</td><td>associatedParty, keywordSet, coverage.</td><td><a href='http://knb.ecoinformatics.org/software/eml/'>http://knb.ecoinformatics.org/software/eml/</a></td></tr>
<tr><td>ABCD</td><td>Description, IPRStatements.</td><td><a href='http://www.tdwg.org/schemas/abcd/2.06'>http://www.tdwg.org/schemas/abcd/2.06</a></td></tr>
<tr><td>DC</td><td>created, pubdate.</td><td><a href='http://purl.org/dc/terms/'>http://purl.org/dc/terms/</a></td></tr>
<tr><td>DWC</td><td>taxonConceptID, Hierarchy, MeasurementOrFact, ResourceRelationShip.</td><td><a href='http://rs.tdwg.org/dwc/terms/'>http://rs.tdwg.org/dwc/terms/</a></td></tr>
<tr><td>GISIN</td><td>origin, presence, persistence, distribution, harmful, modified, startValidDate, endValidDate, countryCode, stateProvince, county, localityName, county, language, citation, abundance...</td><td><a href='http://www.gisin.org/GISIN/SpeciesStatus_4_0_0.xsd'>http://www.gisin.org/GISIN/SpeciesStatus_4_0_0.xsd</a></td></tr>
<tr><td>TCS</td><td>scientificName</td><td><a href='http://www.tdwg.org/schemas/tcs/1.01'>http://www.tdwg.org/schemas/tcs/1.01</a></td></tr>
<tr><td>EOL</td><td>AncillaryData: DataObjectBase</td><td><a href='http://www.eol.org/transfer/content/0.3'>http://www.eol.org/transfer/content/0.3</a></td></tr></tbody></table>



<h1>Application Profile</h1>

<blockquote>As the Plinian Core Abstract Model would be impractical to implement, a generic application Profile –intended for production implementations, including GBIF’s IPT--  was developed. Besides, species information gathered under previous versions of Plinian Core can be easily imported into the new application profile.</blockquote>

<blockquote><img src='http://img600.imageshack.us/img600/6194/x9u4.jpg'></blockquote>

<blockquote>The use of controlled vocabularies is recommended in Plinian Core v3.1 for many elements. A controlled vocabulary will improve datasets interoperability and allow final users to search for detailed information from all structured fields.</blockquote>


<h1>Data Flow</h1>

<blockquote><img src='http://img12.imageshack.us/img12/7862/zoxa.jpg' /></blockquote>

<h1>Future directions</h1>

<blockquote>Species data is crucial for a large number of users, including decision makers worldwide. Therefore it is central to made data available in better-structured ways; thus, we aim to make Plinian Core the product of a wider and more diverse community, embedded in the processes of TDWG. This will definitely introduce some complexity in the decision-making processes, but we are also confident that the outcome will be more robust and usable for a wider community. We count on all interested parties in this new phase of Plinian Core.
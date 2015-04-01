<h2><b>Schema and Legend:</b></h2>


![http://img521.imageshack.us/img521/7227/8xtw.jpg](http://img521.imageshack.us/img521/7227/8xtw.jpg)

|Image|Description|
|:----|:----------|
|<img src='http://imageshack.us/a/img16/5397/multipleg.jpg' width='26' height='24' />|Complex Type|
|<img src='http://img6.imageshack.us/img6/1315/sequencej.jpg' width='26' height='24' />|Sequence structure|
|<img src='http://img266.imageshack.us/img266/2791/choice.jpg' width='26' height='24' />|Choice structure|
|<img src='http://img52.imageshack.us/img52/2777/elementkw.jpg' width='26' height='24' />|Obligatory element|
|<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />|Optional element|
|<img src='http://img19.imageshack.us/img19/4356/infinitol.jpg' width='26' height='24' />|minOccurs=0 maxOccurs=unbounded|
|<img src='http://img198.imageshack.us/img198/6134/unoinfinito.jpg' width='26' height='24' />|minOccurs=1 maxOccurs=unbounded|


<h2><b>Ancillary Data Class: EOL Data Object Base Type</b></h2>

<img src='http://imageshack.us/a/img16/5397/multipleg.jpg' width='26' height='24' /> <img src='http://img6.imageshack.us/img6/1315/sequencej.jpg' width='26' height='24' />

**Quick Reference:**


# dc:identifier #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

<b>Quick Reference:</b>

Recommended to use a globally unique identifier to unambiguously refer to the resource.

<b>Class:</b>

# Data Type #

<img src='http://img52.imageshack.us/img52/2777/elementkw.jpg' width='26' height='24' />

Required. Describes the nature of the resource using the DCMI Type vocabulary.


# mime Type #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

Describes the file format of the resource. Recommended for use with media resources, but not needed for text descriptions.


# agent #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' /> <img src='http://img19.imageshack.us/img19/4356/infinitol.jpg' width='26' height='24' />

Examples of an agent include a person, organization, and software agent which has contributed to the creation of the resource. Strongly recommended to include the role the agent played in the creation of the resource.

# dcterms:created #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

Examples of an agent include a person, organization, and software agent which has contributed to the creation of the resource. Strongly recommended to include the role the agent played in the creation of the resource.


# dcterms:modified #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

Date on which the resource was changed.


# dc:title #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

A name given to the resource. Recommended for use with all text descriptions as well as sound and video media. Detailed captions for media should be included in the description element below.

# license #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

License under which the resource is provided. To the greatest extent possible, the Encyclopedia of Life promotes an open-source, open-access approach.

# dc:rights #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

Statement of rights associated with the resource. Creative Commons licenses require the resource to be attributed "in the manner specified by the author or licensor", and this is where that should be specified.

# dcterms:rightsHolder #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

A person or organization owning or managing rights over the resource.


# dcterms:bibliographicCitation #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

A bibliographic reference for the resource. Sufficient bibliographic detail should be included to identify the resources as unambiguously as possible.


# audience #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' /> <img src='http://img19.imageshack.us/img19/4356/infinitol.jpg' width='26' height='24' />

A class of entity for whom the resource is intended or useful.


# dc:source #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

The URL of a web page which describes the resource.


# subject #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' /> <img src='http://img19.imageshack.us/img19/4356/infinitol.jpg' width='26' height='24' />

The topic of the resource.


# dc:description #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

An account of the resource. For text descriptions, the entire account should be located here. For media resources, captions should be included here. Recommended to remove all embedded HTML tags and include only plain text.

# mediaURL #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' /> <img src='http://img19.imageshack.us/img19/4356/infinitol.jpg' width='26' height='24' />

A URL reference directly to the media resource.


# thumbnailURL #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

A URL reference directly to a thumbnail image associated with the media resource.


# location #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

Natural language description of the locality where the resource was collected or created. Not recommended for use with text descriptions.


# geo:Point #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

Location of the entity in decimal WGS84 latitude and longitude (and optional altitude) as defined by the W3C Basic Geo Vocabulary. See http://www.w3.org/2003/01/geo/ for more information on this standard.

# reference #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' /> <img src='http://img19.imageshack.us/img19/4356/infinitol.jpg' width='26' height='24' />

A related resource that is referenced, cited, or otherwise pointed to by the described resource. Recommended to use well-formed bibliographic citations. Strongly recommended to include identifiers which unambiguously refer to the specified resource when available.


# additionalInformation #

<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />

Anything can be put in here. Use only when necessary as information in this element may be ignored by consumers
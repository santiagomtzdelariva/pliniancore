<img src='http://imageshack.us/a/img16/5397/multipleg.jpg' width='26' height='24' /> <img src='http://img6.imageshack.us/img6/1315/sequencej.jpg' width='26' height='24' />

Hierarchical categories. Modified from Linnean Core. Option: fill all or principal ranks and optionally provide keys.

![http://img716.imageshack.us/img716/3753/y19v.jpg](http://img716.imageshack.us/img716/3753/y19v.jpg)



|Name|Type|Description|References|
|:---|:---|:----------|:---------|
|Kingdom|xs:string|Kingdom name|http://rs.tdwg.org/dwc/2009-09-23/terms/index.htm#kingdom|
|Phylum|xs:string|superPhylum name|http://rs.tdwg.org/dwc/2009-09-23/terms/index.htm#phylum|
|superclass|xs:string|Class name|http://rs.tdwg.org/dwc/2009-09-23/terms/index.htm#class|
|Order|xs:string|Order name|http://rs.tdwg.org/dwc/2009-09-23/terms/index.htm#order|
|Family|xs:string|Family name|http://rs.tdwg.org/dwc/2009-09-23/terms/index.htm#family|
|Genus|xs:string|Genus name|http://rs.tdwg.org/dwc/2009-09-23/terms/index.htm#genus|
|Sub Genus|xs:string|Subgenus name|http://rs.tdwg.org/dwc/2009-09-23/terms/index.htm#subgenus|
|TaxonRank|xs:string|The taxonomic rank of the most specific name in the scientificName. Recommended best practice is to use a controlled vocabulary.|http://rs.tdwg.org/dwc/2009-09-23/terms/index.htm#taxonRank|
|specific Epithet|xs:string|The name of the first or species epithet of the scientificName.|http://rs.tdwg.org/dwc/2009-09-23/terms/index.htm#specificEpithet|
|Infraspecific Epithet|xs:string|The name of the lowest or terminal infraspecific epithet of the scientificName, excluding any rank designation.|http://rs.tdwg.org/dwc/2009-09-23/terms/index.htm#infraspecificEpithet|
|higher Classification|dwc:higherClassification|A list (concatenated and separated) of taxa names terminating at the rank immediately superior to the taxon referenced in the taxon record. Recommended best practice is to order the list starting with the highest rank and separating the names for each rank with a semi-colon (";").|http://rs.tdwg.org/dwc/terms/higherClassification|
|Parent Taxon|xs:string|ID Parent Taxon|  |
|Ancillary Data|  |  |Class: http://code.google.com/p/pliniancore/wiki/AncillaryDataClass|

<br>

<h2><b>Legend:</b></h2>

<table><thead><th>Image</th><th>Description</th></thead><tbody>
<tr><td><img src='http://imageshack.us/a/img16/5397/multipleg.jpg' width='26' height='24' /></td><td>Complex Type</td></tr>
<tr><td><img src='http://img6.imageshack.us/img6/1315/sequencej.jpg' width='26' height='24' /></td><td>Sequence structure</td></tr>
<tr><td><img src='http://img266.imageshack.us/img266/2791/choice.jpg' width='26' height='24' /></td><td>Choice structure</td></tr>
<tr><td><img src='http://img52.imageshack.us/img52/2777/elementkw.jpg' width='26' height='24' /></td><td>Obligatory element</td></tr>
<tr><td><img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' /></td><td>Optional element</td></tr>
<tr><td><img src='http://img19.imageshack.us/img19/4356/infinitol.jpg' width='26' height='24' /></td><td>minOccurs=0 maxOccurs=unbounded</td></tr>
<tr><td><img src='http://img198.imageshack.us/img198/6134/unoinfinito.jpg' width='26' height='24' /></td><td>minOccurs=1 maxOccurs=unbounded</td></tr>
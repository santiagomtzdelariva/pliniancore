<h1><b>Plinian Core 3</b></h1> Plinian Core is a standard oriented to share species level information. Its hierarchical schema allows to develop species data sheets that can be shown in websites.

> <a href='http://purl.org/pliniancore/About'>About Plinian Core</a>

> <b>New Abstract model release:</b> https://pliniancore.googlecode.com/svn/trunk/xsd/PlinianCore_AbstractModel_v3.2.xsd

> <b>Application profiles already defined:</b>

> <b>- For the <a href='http://www.sibcolombia.net/'>SIB-COLOMBIA</a>:</b>https://pliniancore.googlecode.com/svn/trunk/xsd/ap/PliC3.2_AP_SIB-COLOMBIA.xsd

> <b>- For the <a href='http://www.conabio.gob.mx/'>CONABIO</a>:</b> https://pliniancore.googlecode.com/svn/trunk/xsd/ap/PliC3.2_AP_CONABIO.xsd

> <b>- For the <a href='http://www.magrama.gob.es/es/'>MAGRAMA</a>:</b>  https://pliniancore.googlecode.com/svn/trunk/xsd/ap/PliC3.2_AP_MAGRAMA.xsd

> <b>Unstructured Documentation:</b> http://purl.org/pliniancore/doc/

> <b>Poster:</b> http://purl.org/pliniancore/posterTDWG2013

Below, you can see a structure that can  be used it to look at the elements that make up Plinian Core 3.


<h2><b>- Elements:</b></h2>
  * [Plinian Core Elements](PlinianCore_Elements.md)
    * [Dataset](DataSet.md)
      * [Metadata](Metadata.md)
        * [DataSet\_ID](http://code.google.com/p/pliniancore/wiki/MetadataClass#Data_Set_ID)
        * [IconURI](http://code.google.com/p/pliniancore/wiki/MetadataClass#Icon_URI)
        * [Source](http://code.google.com/p/pliniancore/wiki/MetadataClass#Source)
        * [associatedParty](http://code.google.com/p/pliniancore/wiki/MetadataClass#associated_Party)
        * [Description](http://code.google.com/p/pliniancore/wiki/MetadataClass#Description)
        * [Revision](http://code.google.com/p/pliniancore/wiki/MetadataClass#Revison)
        * [IPRStatements](http://code.google.com/p/pliniancore/wiki/MetadataClass#IPR_Statements)
        * [Coverage](http://code.google.com/p/pliniancore/wiki/MetadataClass#Coverage)
        * [Version](http://code.google.com/p/pliniancore/wiki/MetadataClass#Version)
        * [keywordSet](http://code.google.com/p/pliniancore/wiki/MetadataClass#keyword_Set)
      * [TaxonRecord](TaxonRecord.md)
        * [RecordMetadata](RecordMetadata.md)
        * [BaseElements](BaseElements.md)
        * [NomenclatureAndClassification](NomenclatureAndClassification.md)
        * [TaxonomicalDescription](Description.md)
        * [NaturalHistory](NaturalHistory.md)
        * [Invasiveness](Invasiveness.md)
        * [HabitatAndDistribution](HabitatAndDistribution.md)
        * [DemographyAndConservation](DemographyAndConservation.md)
        * [UsesManagementAndConservation](UsesManagementAndConservation.md)
        * [associatedParty](http://knb.ecoinformatics.org/software/eml/eml-2.1.1/eml-resource.html#associatedParty)
        * [References](References.md)
        * [AncillaryData](AncillaryData.md)
      * [AncillaryData](AncillaryData.md)


Each element is of a kind of data or Class. So, in each definition in Plinian Core 3, you can see: the name, the properties, the definition, class and, if the element belongs to other standard, a Quick Reference to the source standard.

e.g.

![http://img801.imageshack.us/img801/4161/nyba.jpg](http://img801.imageshack.us/img801/4161/nyba.jpg)

Now, you can see a legend of the properties of the elements.

> <h3><b>+ List of Properties:</b></h3>

|Image|Description|
|:----|:----------|
|<img src='http://imageshack.us/a/img16/5397/multipleg.jpg' width='26' height='24' />|Complex Type, the element is structured by more elements|
|<img src='http://img6.imageshack.us/img6/1315/sequencej.jpg' width='26' height='24' />|Sequence structure, the element is structured by a sequence of elements.|
|<img src='http://img266.imageshack.us/img266/2791/choice.jpg' width='26' height='24' />|Choice structure, the element is structured by only one element of the sequence.|
|<img src='http://img52.imageshack.us/img52/2777/elementkw.jpg' width='26' height='24' />|Obligatory element|
|<img src='http://img585.imageshack.us/img585/4808/optional.jpg' width='26' height='24' />|Optional element|
|<img src='http://img19.imageshack.us/img19/4356/infinitol.jpg' width='26' height='24' />|minOccurs=0 maxOccurs=unbounded|
|<img src='http://img198.imageshack.us/img198/6134/unoinfinito.jpg' width='26' height='24' />|minOccurs=1 maxOccurs=unbounded|

<h2><b>- Classes:</b></h2>

In this structure you can see all the classes that are defined in Plinian Core 3:

  * [Plinian Core Classes](PlinianCore_Classes.md)
    * [Metadata Class](MetadataClass.md)
    * [Version Class](VersionClass.md)
    * [Revision Class](RevisionClass.md)
    * [NomenclatureAndClassification Class](NomenclatureAndClassificationClass.md)
      * [Synonyms Class](SynonymsClass.md)
        * [SynonymsAtomized Class](SynonymsAtomizedClass.md)
      * [CommonNames Class](CommonNamesClass.md)
        * [CommonNamesAtomized Class](CommonNamesAtomizedClass.md)
      * [Hierarchy Class](HierarchyClass.md)
      * [MiscDetails Class](MiscDetailClass.md)
        * [Detail Class](DetailClass.md)
    * [TaxonomicalDescription Class](TaxonomicalDescriptionClass.md)
      * [BriefDescription](http://code.google.com/p/pliniancore/wiki/TaxonomicalDescriptionClass#Brief_Description)
      * [FullDescription Class](FullDescriptionClass.md)
      * [Identification Keys](http://code.google.com/p/pliniancore/wiki/TaxonomicalDescriptionClass#Identification_Keys)
    * [NaturalHistory Class](NaturalHistoryClass.md)
      * [LifeForm Class](LifeFormClass.md)
      * [LifeCycle Class](LifeCycleClass.md)
      * [Reproduction Class](ReproductionClass.md)
      * [AnnualCycles Class](AnnualCyclesClass.md)
        * [AnnualCyclesAtomized Class](AnnualCyclesAtomizedClass.md)
      * [Feeding Class](FeedingClass.md)
        * [FeedingAtomized Class](FeedingAtomizedClass.md)
      * [Dispersal Class](DispersalClass.md)
        * [DispersalAtomized Class](DispersalAtomizedClass.md)
      * [Behavior Class](BehaviorClass.md)
      * [Interactions Class](InteractionsClass.md)
        * [InteractionAtomized Class](InteractionAtomizedClass.md)
      * [MolecularData Class](MolecularDataClass.md)
        * [MolecularDataAtomized Class](MolecularDataAtomizedClass.md)
      * [Migratory Class](MigratoryClass.md)
        * [MigratoryAtomized Class](MigratoryAtomizedClass.md)
      * [EcologicalSignificance Class](EcologicalSignificanceClass.md)
      * [MiscDetails Class](MiscDetailClass.md)
        * [Detail Class](DetailClass.md)
      * [EnvironmentalEnvelope Class](EnvironmentalEnvelopeClass.md)
    * [Invasiveness Class](InvasivenessClass.md)
      * [InvasivenessAtomized Class](InvasivenessAtomizedClass.md)
    * [HabitatAndDistribution Class](HabitatAndDistributionClass.md)
      * [Habitats Class](HabitatsClass.md)
      * [Distribution Class](DistributionClass.md)
        * [DistributionAtomized Class](DistributionAtomizedClass.md)
      * [Endemic Class](EndemicClass.md)
        * [EndemicAtomized Class](EndemicAtomizedClass.md)
    * [DemographyAndThreat Class](DemographyAndThreatClass.md)
      * [Territory Class](TerritoryClass.md)
        * [TerritoryAtomized Class](TerritoryAtomizedClass.md)
      * [PopulationBiology Class](PopulationBiologyClass.md)
        * [PopulationBiologyAtomized Class](PopulationBiologyAtomizedClass.md)
      * [ThreatStatus](http://code.google.com/p/pliniancore/wiki/DemographyAndThreatClass#Threat_Status)
      * [Legislation Class](LegislationClass.md)
      * [DirectThreats](http://code.google.com/p/pliniancore/wiki/DemographyAndThreatClass#Direct_Threats)
        * [LegislationAtomized Class](LegislationAtomizedClass.md)
    * [UsesManagementAndConservation Class](UsesManagementAndConservationClass.md)
      * [Uses Class](UsesClass.md)
        * [UsesAtomized Class](UsesAtomizedClass.md)
      * [ManagementAndConservation Class](ManagementAndConservationClass.md)
        * [ManagementAtomized Class](ManagementAtomizedClass.md)
    * [AncillaryData Class](AncillaryDataClass.md)
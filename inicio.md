# Plinian Core Plano #


## Introducción ##

Este wiki ha sido creado con la intención que todos los interesados aporten sugerencias para mejorar el esquema, **en su versión plana** (Plinan Core Flat).


El "Plinian Core Flat" es una versión simplificada  --destinada originalmente a servir de base para el desarrollo de páginas web con fichas de especies-- de un esquema conceptual jerárquico, semánticamente más rico y detallado.  La última versión de este esquema se puede  obtener aquí:
[Plinian\_2.0.xsd\_comprimido\_como\_.zip](http://www.gbif.es/plinian/data/media/plinian_2.0.xsd_comprimido_como_.zip)

Y una visualización del esquema como pdf aquí: [poster\_plinian\_core\_v2.pdf](http://www.gbif.es/plinian/lib/exe/fetch.php?id=Inicio&cache=cache&media=poster_plinian_core_v2.pdf)




## Versiones ##

Estas son las versiones del esquema plano.

  * Versión 2.2.1: http://www.pliniancore.org/test/pl_corev2.2.1.xsd

  * Versión 2.2.2: http://www.pliniancore.org/test/pl_corev2.2.2.xsd

  * Versión 2.2.3: http://www.pliniancore.org/test/pl_corev2.2.3.xsd (no disponible)

  * Versión 2.2.4: http://www.pliniancore.org/test/pl_corev2.2.4.xsd (no disponible)

  * [Plinian Core Flat2.3](PlinianCoreFlat2_3.md)





















## Elementos ##

> La constitución actual del Plinian Core plano es la siguiente.
> Para comentar con respecto a cualquier elemento, hacer clic en el elemento.

|  **PC 2.2.1**  |  **PC 2.2.2**  |  **PC 2.2.3**  |  **PC 2.2.4**  |  **Plinian Core Flat2.3**  |
|:---------------|:---------------|:---------------|:---------------|:---------------------------|
|  **ScientificName `(*)`**  |  **ScientificName `(*)`**  |  **ScientificName `(*)`**  |  **[CanonicalName](PlinianCore_CanonicalName.md) `(*)`**  |  **[ScientificName](PlinianCore_ScientificName.md)** `(*)`  |
|  **[InstitutionCode](PlinianCore_InstitutionCode.md) `(*)`**  |  **[InstitutionCode](PlinianCore_InstitutionCode.md) `(*)`**  |  **[InstitutionCode](PlinianCore_InstitutionCode.md) `(*)`**  |  **[InstitutionCode](PlinianCore_InstitutionCode.md) `(*)`**  |  **[InstitutionCode](PlinianCore_InstitutionCode.md) `(*)`**  |
|  **DateLastModified `(*)`**  |  **DateLastModified `(*)`**  |  **DateLastModified `(*)`**  |  **[DateModified](PlinianCore_DateModified.md) `(*)`**  |  **[DateLastModified](PlinianCore_DateModified.md)`(*)`**  |
|  **Code `(*)`**  |  **Code `(*)`**  |  **[TaxonRecordID](PlinianCore_TaxonRecordID.md) `(*)`**  |  **[TaxonRecordID](PlinianCore_TaxonRecordID.md) `(*)`**  |  **[TaxonRecordID](PlinianCore_TaxonRecordID.md) `(*)`**  |
|  **[Language](PlinianCore_Language.md) `(*)`**  |  **[Language](PlinianCore_Language.md) `(*)`**  |  **[Language](PlinianCore_Language.md) `(*)`**  |  **[Language](PlinianCore_Language.md) `(*)`**  |  **[Language](PlinianCore_Language.md) `(*)`**  |
|  **Coauthors**  |  **Coauthors**  |  **Coauthors**  |  |  |
|  **SpeciesPageAuthor `(*)`**  |  **SpeciesPageAuthor `(*)`**  |  **SpeciesPageAuthor `(*)`**  |  |  |
|  |  |  |  **[Creators](PlinianCore_Creators.md) `(*)`**  |  **[Creators](PlinianCore_Creators.md) `(*)`**  |
|  **[Countries](PlinianCore_Countries.md) `(*)`**  |  **[Countries](PlinianCore_Countries.md) `(*)`**  |  **[Countries](PlinianCore_Countries.md) `(*)`**  |  |  |
|  **[Distribution](PlinianCore_Distribution.md)**  |  **[Distribution](PlinianCore_Distribution.md)**  |  **[Distribution](PlinianCore_Distribution.md)**  |  **[Distribution](PlinianCore_Distribution.md)**  |  **[Distribution](PlinianCore_Distribution.md)**  |
|  |  **[Abstract](PlinianCore_Abstract.md)**  |  **[Abstract](PlinianCore_Abstract.md)**  |  **[Abstract](PlinianCore_Abstract.md)**  |  **[Abstract](PlinianCore_Abstract.md)**  |
|  **[Kingdom](PlinianCore_Kingdom.md)**  |  **[Kingdom](PlinianCore_Kingdom.md)**  |  **[Kingdom](PlinianCore_Kingdom.md)**  |  **[Kingdom](PlinianCore_Kingdom.md)**  |  **[Kingdom](PlinianCore_Kingdom.md)**  |
|  **[Phylum](PlinianCore_Phylum.md)**  |  **[Phylum](PlinianCore_Phylum.md)**  |  **[Phylum](PlinianCore_Phylum.md)**  |  **[Phylum](PlinianCore_Phylum.md)**  |  **[Phylum](PlinianCore_Phylum.md)**  |
|  **[Class](PlinianCore_Class.md)**  |  **[Class](PlinianCore_Class.md)**  |  **[Class](PlinianCore_Class.md)**  |  **[Class](PlinianCore_Class.md)**  |  **[Class](PlinianCore_Class.md)**  |
|  **[Order](PlinianCore_Order.md)**  |  **[Order](PlinianCore_Order.md)**  |  **[Order](PlinianCore_Order.md)**  |  **[Order](PlinianCore_Order.md)**  |  **[Order](PlinianCore_Order.md)**  |
|  **[Family](PlinianCore_Family.md)**  |  **[Family](PlinianCore_Family.md)**  |  **[Family](PlinianCore_Family.md)**  |  **[Family](PlinianCore_Family.md)**  |  **[Family](PlinianCore_Family.md)**  |
|  **[Genus](PlinianCore_Genus.md)**  |  **[Genus](PlinianCore_Genus.md)**  |  **[Genus](PlinianCore_Genus.md)**  |  **[Genus](PlinianCore_Genus.md)**  |  **[Genus](PlinianCore_Genus.md)**  |
|  **[Synonyms](PlinianCore_Synonyms.md)**  |  **[Synonyms](PlinianCore_Synonyms.md)**  |  **[Synonyms](PlinianCore_Synonyms.md)**  |  **[Synonyms](PlinianCore_Synonyms.md)**  |  **[Synonyms](PlinianCore_Synonyms.md)**  |
|  **AuthorYearOfScientificName**  |  **AuthorYearOfScientificName**  |  **AuthorYearOfScientificName**  |  |  **[AuthorYearOfScientificName](AuthorYearOfScientificName.md)**  |
|  |  |  |  **[CanonicalAuthorship](PlinianCore_CanonicalAuthorship.md)**  |  |
|  **[SpeciesPublicationReference](PlinianCore_SpeciesPublicationReference.md)**  |  **[SpeciesPublicationReference](PlinianCore_SpeciesPublicationReference.md)**  |  **[SpeciesPublicationReference](PlinianCore_SpeciesPublicationReference.md)**  |  **[PublishedIn](PlinianCore_PublishedIn.md)**  |  **[SpeciesPublicationReference](PlinianCore_SpeciesPublicationReference.md)**  |
|  **[CommonNames](PlinianCore_CommonNames.md)**  |  **[CommonNames](PlinianCore_CommonNames.md)**  |  **[CommonNames](PlinianCore_CommonNames.md)**  |  **[CommonNames](PlinianCore_CommonNames.md)**  |  **[CommonNames](PlinianCore_CommonNames.md)**  |
|  **TypeLocation**  |  **TypeLocation**  |  **TypeLocation**  |  |  |
|  **TypeDepository**  |  **TypeDepository**  |  **TypeDepository**  |  |  |
|  **TypeCollector**  |  **TypeCollector**  |  **TypeCollector**  |  |  |
|  |  |  |  **[Typification](PlinianCore_Typification.md)**  |  **[Typification](PlinianCore_Typification.md)**  |
|  |  |  |  **[GlobalUniqueIdentifier](PlinianCore_GlobalUniqueIdentifier.md)**  |  **[GlobalUniqueIdentifier](PlinianCore_GlobalUniqueIdentifier.md)**  |
|  **Collaborators**  |  **Collaborators**  |  **Collaborators**  |  **[Contributors](PlinianCore_Contributors.md)**  |  **[Contributors](PlinianCore_Contributors.md)**  |
|  **PublicationDate**  |  **PublicationDate**  |  **PublicationDate**  |  **[DateCreated](PlinianCore_DateCreated.md)**  |  **[DateCreated](PlinianCore_DateCreated.md)**  |
|  **[Habit](PlinianCore_Habit.md)**  |  **[Habit](PlinianCore_Habit.md)**  |  **[Habit](PlinianCore_Habit.md)**  |  **[Habit](PlinianCore_Habit.md)**  |  **[Habit](PlinianCore_Habit.md)** |
|  **[LifeCycle](PlinianCore_LifeCycle.md)**  |  **[LifeCycle](PlinianCore_LifeCycle.md)**  |  **[LifeCycle](PlinianCore_LifeCycle.md)**  |  **[LifeCycle](PlinianCore_LifeCycle.md)**  |  **[LifeCycle](PlinianCore_LifeCycle.md)**  |
|  **[Reproduction](PlinianCore_Reproduction.md)**  |  **[Reproduction](PlinianCore_Reproduction.md)**  |  **[Reproduction](PlinianCore_Reproduction.md)**  |  **[Reproduction](PlinianCore_Reproduction.md)**  |  **[Reproduction](PlinianCore_Reproduction.md)**  |
|  **Seasons**  |  |  |  |  |
|  **Phenology**  |  |  |  |  |
|  |  **[AnnualCycle](PlinianCore_AnnualCycle.md)**  |  **[AnnualCycle](PlinianCore_AnnualCycle.md)**  |  **[AnnualCycle](PlinianCore_AnnualCycle.md)**  |  **[AnnualCycle](PlinianCore_AnnualCycle.md)**   |
|  **[ScientificDescription](PlinianCore_ScientificDescription.md)**  |  **[ScientificDescription](PlinianCore_ScientificDescription.md)**  |  **[ScientificDescription](PlinianCore_ScientificDescription.md)**  |  **[ScientificDescription](PlinianCore_ScientificDescription.md)**  |  **[ScientificDescription](PlinianCore_ScientificDescription.md)**  |
|  **[BriefDescription](PlinianCore_BriefDescription.md)**  |  **[BriefDescription](PlinianCore_BriefDescription.md)**  |  **[BriefDescription](PlinianCore_BriefDescription.md)**  |  **[BriefDescription](PlinianCore_BriefDescription.md)**  |  **[BriefDescription](PlinianCore_BriefDescription.md)**  |
|  **[Feeding](PlinianCore_Feeding.md)**  |  **[Feeding](PlinianCore_Feeding.md)**  |  **[Feeding](PlinianCore_Feeding.md)**  |  **[Feeding](PlinianCore_Feeding.md)**  |  **[Feeding](PlinianCore_Feeding.md)**  |
|  **[Behavior](PlinianCore_Behavior.md)**  |  **[Behavior](PlinianCore_Behavior.md)**  |  **[Behavior](PlinianCore_Behavior.md)**  |  **[Behavior](PlinianCore_Behavior.md)**  |  **[Behavior](PlinianCore_Behavior.md)**  |
|  **SymbioticRelationship**  |  **[Interactions](PlinianCore_Interactions.md)**  |  **[Interactions](PlinianCore_Interactions.md)**  |  **[Interactions](PlinianCore_Interactions.md)**  |  **[Interactions](PlinianCore_Interactions.md)**  |
|  **[ChromosomicNumberN](PlinianCore_ChromosomicNumberN.md)**  |  **[ChromosomicNumberN](PlinianCore_ChromosomicNumberN.md)**  |  **[ChromosomicNumberN](PlinianCore_ChromosomicNumberN.md)**  |  **[ChromosomicNumberN](PlinianCore_ChromosomicNumberN.md)**  |  **[ChromosomicNumberN](PlinianCore_ChromosomicNumberN.md)**  |
|  **[MolecularData](PlinianCore_MolecularData.md)**  |  **[MolecularData](PlinianCore_MolecularData.md)**  |  **[MolecularData](PlinianCore_MolecularData.md)**  |  **[MolecularData](PlinianCore_MolecularData.md)**  |  **[MolecularData](PlinianCore_MolecularData.md)**  |
|  **Population**  |  |  |  |  |
|  **PopulationState**  |  |  |  |  |
|  |  **[PopulationBiology](PlinianCore_PopulationBiology.md)**  |  **[PopulationBiology](PlinianCore_PopulationBiology.md)**  |  **[PopulationBiology](PlinianCore_PopulationBiology.md)**  |  **[PopulationBiology](PlinianCore_PopulationBiology.md)**  |
|  **ConservationStatusCITES**  |  **ConservationStatusCITES**  |  |  |  |
|  **ConservationStatusUICN**  |  **ConservationStatusUICN**  |  |  |  |
|  |  |  **[ThreatStatus](PlinianCore_ThreatStatus.md)**  |  **[ThreatStatus](PlinianCore_ThreatStatus.md)**  |  **[ThreatStatus](PlinianCore_ThreatStatus.md)**  |
|  **NationalLegislation**  |  **NationalLegislation**  |  |  |  |
|  **RegionalLegislation**  |  **RegionalLegislation**  |  |  |  |
|  |  |  **[Legislation](PlinianCore_Legislation.md)**  |  **[Legislation](PlinianCore_Legislation.md)**  |  **[Legislation](PlinianCore_Legislation.md)**  |
|  **[Habitat](PlinianCore_Habitat.md)**  |  **[Habitat](PlinianCore_Habitat.md)**  |  **[Habitat](PlinianCore_Habitat.md)**  |  **[Habitat](PlinianCore_Habitat.md)**  |  **[Habitat](PlinianCore_Habitat.md)**  |
|  **[Territory](PlinianCore_Territory.md)**  |  **[Territory](PlinianCore_Territory.md)**  |  **[Territory](PlinianCore_Territory.md)**  |  **[Territory](PlinianCore_Territory.md)**  |  **[Territory](PlinianCore_Territory.md)**  |
|  **Endemism**  |  **Endemism**  |  **Endemism**  |  **[Endemicity](PlinianCore_Endemicity.md)**  |  **[Endemicity](PlinianCore_Endemicity.md)**  |
|  **DocumentedUses**  |  |  |  |  |
|  **TraditionalUses**  |  |  |  |  |
|  |  **[Uses](PlinianCore_Uses.md)**  |  **[Uses](PlinianCore_Uses.md)**  |  **[Uses](PlinianCore_Uses.md)**  |  **[Uses](PlinianCore_Uses.md)**  |
|  |  **[Management](PlinianCore_Management.md)**  |  **[Management](PlinianCore_Management.md)**  |  **[Management](PlinianCore_Management.md)**  |  **[Management](PlinianCore_Management.md)**  |
|  **[Folklore](PlinianCore_Folklore.md)**  |  **[Folklore](PlinianCore_Folklore.md)**  |  **[Folklore](PlinianCore_Folklore.md)**  |  **[Folklore](PlinianCore_Folklore.md)**  |  **[Folklore](PlinianCore_Folklore.md)**  |
|  **[References](PlinianCore_References.md)**  |  **[References](PlinianCore_References.md)**  |  **[References](PlinianCore_References.md)**  |  **[References](PlinianCore_References.md)**  |  **[References](PlinianCore_References.md)**  |
|  |  **[UnstructuredDocumentation](PlinianCore_UnstructuredDocumentation.md)**  |  **[UnstructuredDocumentation](PlinianCore_UnstructuredDocumentation.md)**  |  **[UnstructuredDocumentation](PlinianCore_UnstructuredDocumentation.md)**  |  **[UnstructuredDocumentation](PlinianCore_UnstructuredDocumentation.md)**  |
|  **[OtherInformationSources](PlinianCore_OtherInformationSources.md)**  |  **[OtherInformationSources](PlinianCore_OtherInformationSources.md)**  |  **[OtherInformationSources](PlinianCore_OtherInformationSources.md)**  |  **[OtherInformationSources](PlinianCore_OtherInformationSources.md)**  |  **[OtherInformationSources](PlinianCore_OtherInformationSources.md)**  |
|  **[Papers](PlinianCore_Papers.md)**  |  **[Papers](PlinianCore_Papers.md)**  |  **[Papers](PlinianCore_Papers.md)**  |  **[Papers](PlinianCore_Papers.md)**  |  **[Papers](PlinianCore_Papers.md)**  |
|  |  **[IdentificationKeys](PlinianCore_IdentificationKeys.md)**  |  **[IdentificationKeys](PlinianCore_IdentificationKeys.md)**  |  **[IdentificationKeys](PlinianCore_IdentificationKeys.md)**  |  **[IdentificationKeys](PlinianCore_IdentificationKeys.md)**  |
|  |  **[MigratoryData](PlinianCore_MigratoryData.md)**  |  **[MigratoryData](PlinianCore_MigratoryData.md)**  |  **[MigratoryData](PlinianCore_MigratoryData.md)**  |  **[MigratoryData](PlinianCore_MigratoryData.md)**  |
|  |  **[EcologicalSignificance](PlinianCore_EcologicalSignificance.md)**  |  **[EcologicalSignificance](PlinianCore_EcologicalSignificance.md)**  |  **[EcologicalSignificance](PlinianCore_EcologicalSignificance.md)**  |  **[EcologicalSignificance](PlinianCore_EcologicalSignificance.md)**  |
|  |  |  |  |  **[UnstructuredNaturalHistory](PlinianCore_UnstructuredNaturalHistory.md)**  |
|  |  |  |  |  **[InvasivenessData](PlinianCore_InvasivenessData.md)**  |
|  |  |  **[TargetAudiences](PlinianCore_TargetAudiences.md)**  |  **[TargetAudiences](PlinianCore_TargetAudiences.md)**  |  **[TargetAudiences](PlinianCore_TargetAudiences.md)**  |
|  |  |  **[Version](PlinianCore_Version.md)**  |  **[Version](PlinianCore_Version.md)**  |  **[Version](PlinianCore_Version.md)**  |
|  **[URLImage1](PlinianCore_URLImage1.md)**  |  **[URLImage1](PlinianCore_URLImage1.md)**  |  **[URLImage1](PlinianCore_URLImage1.md)**  |  **[URLImage1](PlinianCore_URLImage1.md)**  |  **[URLImage1](PlinianCore_URLImage1.md)**  |
|  **[CaptionImage1](PlinianCore_CaptionImage1.md)**  |  **[CaptionImage1](PlinianCore_CaptionImage1.md)**  |  **[CaptionImage1](PlinianCore_CaptionImage1.md)**  |  **[CaptionImage1](PlinianCore_CaptionImage1.md)**  |  **[CaptionImage1](PlinianCore_CaptionImage1.md)**  |
|  **[URLImage2](PlinianCore_URLImage2.md)**  |  **[URLImage2](PlinianCore_URLImage2.md)**  |  **[URLImage2](PlinianCore_URLImage2.md)**  |  **[URLImage2](PlinianCore_URLImage2.md)**  |  **[URLImage2](PlinianCore_URLImage2.md)**  |
|  **[CaptionImage2](PlinianCore_CaptionImage2.md)**  |  **[CaptionImage2](PlinianCore_CaptionImage2.md)**  |  **[CaptionImage2](PlinianCore_CaptionImage2.md)**  |  **[CaptionImage2](PlinianCore_CaptionImage2.md)**  |  **[CaptionImage2](PlinianCore_CaptionImage2.md)**  |
|  **[URLImage3](PlinianCore_URLImage3.md)**  |  **[URLImage3](PlinianCore_URLImage3.md)**  |  **[URLImage3](PlinianCore_URLImage3.md)**  |  **[URLImage3](PlinianCore_URLImage3.md)**  |  **[URLImage3](PlinianCore_URLImage3.md)**  |
|  **[CaptionImage3](PlinianCore_CaptionImage3.md)**  |  **[CaptionImage3](PlinianCore_CaptionImage3.md)**  |  **[CaptionImage3](PlinianCore_CaptionImage3.md)**  |  **[CaptionImage3](PlinianCore_CaptionImage3.md)**  |  **[CaptionImage3](PlinianCore_CaptionImage3.md)**  |

> `(*)` obligatorios

## Historial de Revisiones ##

Se parte desde la version 2.2.1 del Plinian Core plano.
http://www.pliniancore.org/test/pl_corev2.2.1.xsd


  * [2.2.1 --> 2.2.2](2_2_1_to_2_2_2.md)
  * [2.2.2 --> 2.2.3](2_2_2_to_2_2_3.md)
  * [Propuesta 2.2.3 --> 2.2.4](2_2_3_to_2_2_4_Propuesta.md)
  * [Versión PlinianCoreFlat 2.3](2_2_3___2_2_4_to_2_3.md)














## Hacia una versión Flat 2.4: Propuestas de cambios ##

  * Agregar elemento "dataset\_code" [F. Pando]
  * Mejorar el tipo de dato a utilizar en el elemento "distribution", pasar de un campo textual a algo que sea útil para poder "pintarlo" sobre un mapa. Además implica  buscar opciones desde el punto de vista técnico. [F. Pando]
  * Elementos que precisan de vocabularios controlados:
    * [Habit](PlinianCore_Habit.md)
    * [Feeding](PlinianCore_Feeding.md)
    * [Behavior](PlinianCore_Behavior.md)
    * [Interactions](PlinianCore_Interactions.md)
    * [ThreatStatus](PlinianCore_ThreatStatus.md)
    * [Habitat](PlinianCore_Habitat.md)
    * [Uses](PlinianCore_Uses.md)
    * [TargetAudiences](PlinianCore_TargetAudiences.md)
> > > [F. Pando]

Prueba de enlace a "Terms": [Terms](PlinianCore_Terms.md)
y a un término específico: [InstitutionCode ](PlinianCore_Terms#2..md)


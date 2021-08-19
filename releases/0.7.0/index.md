---
title: 0.7.0 Release
layout: releases
custom_css: releases
---

## {{ page.title }}

###### Date: 2021-08-18


#### Release Notes

UCO 0.7.0 is primarily focused on the conversion of UCO ontologies to leverage the Shapes Constraint Language (SHACL) rather than domain assertions and owl property restrictions to define class shapes. In addition, it added a Continuous Integration (CI) method for testing and verifying the ontology and it corrects several minor issues and bugs.

[UCO 0.7.0 Release Notes](./UCO-0.7.0-ReleaseNotes.md)

#### [Change proposals addressed in UCO 0.7.0](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/61243393/Change+Proposals)

* CP-5: Refactor and improve contacts
* CP-23: Convert current property restrictions and domain assertions to SHACL shapes
* CP-38: Change NTFSFileSystemFacet to NTFSFileFacet
* CP-39: Establish unit tests and Continuous Integration for ontology repository
* CP-46: Change range of observable:partitionID from xsd:integer to xsd:string within DiskPartitionFacet
* CP-48: Correct RDFS concept IRI typos introduced in UCO 0.6.0
* CP-52: Treat "nameserver" as two-word term
* CP-53: Fix URI typo in core:ExternalReference and observable:OnlineServiceFacet
* CP-54: Add clarifying comment to use of observable:sizeInBytes on observable:FileFacet
* CP-55: Change definition of core:specVersion to include subontologies
* CP-57: Change name of identity:CountriesOfResidence to conform to naming standard
* CP-58: Modify range of observable:clockSetting from xsd:string to xsd:dateTime
* CP-59: Modify cardinality of observable:hasChanged on observable:ObservableObject from 1 to 0..1
* CP-60: Remove duplicate definitions from some properties
* CP-62: Correct misuse of identity:Identity and marking:MarkingDefinition within the core namespace
* CP-63: Remove "minimum" restriction from core:id
* CP-64: Remove observable:faxNumber
* CP-65: Fix typo in observable:profilelanguage
* CP-66: Remove core:role
* CP-67: observable:region_end_address is a typo within obervable-da.ttl
* CP-69: Fix several typos within observable.ttl prior to SHACL release
* CP-71: Set ontology Continuous Integration to use Java 8
* CP-72: Remove xsd:string values from sh:datatype on property shapes for observable:mockLocationsAllowed and observable:phoneActivationTime
* CP-73: observable:status property is being used in multiple classes with multiple datatypes
* CP-74: observable:priority is used across multiple context with multiple datatypes
* CP-75: Remove xsd:float from observable:WindowsPESection
* CP-76: Range of observable:owner should only be core:UcoObject
* CP-77: types:entry has multiple contexts with multiple datatypes
* CP-78: observable:listedCount was not created during the implementation of CP-7
* CP-79: Add test for sh:datatype count validity


#### Ontology File(s)

[GitHub](https://github.com/ucoProject/UCO/releases/tag/0.7.0)

#### Documentation

[UCO 0.7.0 Documentation](./docs/index.html)

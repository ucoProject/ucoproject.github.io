---
title: 0.9.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

###### Date: TBD

## Ontology File(s)

###### GitHub: Release TBD

## Release Notes


#### Breaking Changes
*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*

* Removed observable:AttachmetFacet and added two new vocabulary terms to vocabulary:ObservableObjectRelationshipVocab ([*Change Proposal 81*](https://drive.google.com/file/d/1-NM50XbDTjSi4Ke3MTpIEPm1OI5ipmyo/view))
* Changed observable:userName from an owl:ObjectProperty to an owl:DatatypeProperty ([*GitHub Issue 351*](https://github.com/ucoProject/UCO/issues/351))

#### Changes
*(These are general changes to the preexisting ontology that are not breaking or range changes.)*

* Removed cardinality bound on observable:mimeType ([*Change Proposal 104*](https://drive.google.com/file/d/1X3POH_L5g-MMgxVSj8cpcvE-w9GVaPt1/view))
* Changed any rdfs:comment within an sh:PropertyShape to sh:description ([*GitHub Issue 357*](https://github.com/ucoProject/UCO/issues/357))
* Removed minimum cardinality bound on observable:isMimeEncoded and observable:isMultipart within observable:EmailMessageFacet ([*GitHub Issue 383*](https://github.com/ucoProject/UCO/issues/383))

## Documentation
TBD

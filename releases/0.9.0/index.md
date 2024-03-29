---
title: 0.9.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

###### Date: 2022-06-16

## Ontology File(s)

[GitHub](https://github.com/ucoProject/UCO/releases/tag/0.9.0)

## Release Notes
UCO 0.9.0 primarily focused on workflow technology transitions, and was necessitated by a Java dependency upgrade.  The workflow used to normalize Turtle files in UCO and in downstream repositories now minimally requires Java 11, which impacts several public repositories---especially within the [CASE](https://caseontology.org/) community---that present Turtle files as part of their review process.  The workflow to interface with the UCO and CASE ontologies has transitioned to Github Issues, which has caused some files related to programming Github interfaces to become versioned with the ontology.  SHACL documentation will now use `sh:description` when documenting SHACL shapes.  OWL-level ontological commitments are being restored since the transition to SHACL, starting with clarifying that `core:UcoObject` and `core:Facet` are disjoint classes.  In SHACL validation updates, 0.9.0 refines some properties in email stub graph objects, polyglot designations with multiple MIME types, and a correction with names of accounts.

### Errata
*Note*: The release notes included in the ontology errantly describe inclusion of a proposal on designating `core:hasFacet` as an OWL inverse-functional property.  That proposal, anchored at [Issue 379](https://github.com/ucoProject/UCO/issues/379), was still undergoing committee review at the time of release, and was not yet integrated into the ontology.


#### Breaking Changes
*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*

* Removed observable:AttachmetFacet and added two new vocabulary terms to vocabulary:ObservableObjectRelationshipVocab ([*Change Proposal 81*](https://drive.google.com/file/d/1-NM50XbDTjSi4Ke3MTpIEPm1OI5ipmyo/view))
* Changed observable:userName from an owl:ObjectProperty to an owl:DatatypeProperty ([*GitHub Issue 351*](https://github.com/ucoProject/UCO/issues/351))
* Updated rdf-toolkit to version 1.11.0 and Java to version 11 ([*GitHub Issue 373*](https://github.com/ucoProject/UCO/issues/373))
* Defined core:Facet and core:UcoObject as disjoint classes ([*GitHub Issue 378*](https://github.com/ucoProject/UCO/issues/378))
* Changed observable:inReplyTo to an owl:DatatypeProperty with an rdfs:range of xsd:string ([*GitHub Issue 380*](https://github.com/ucoProject/UCO/issues/380))

#### Changes
*(These are general changes to the preexisting ontology that are not breaking or range changes.)*

* Removed cardinality bound on observable:mimeType ([*Change Proposal 104*](https://drive.google.com/file/d/1X3POH_L5g-MMgxVSj8cpcvE-w9GVaPt1/view))
* Changed any rdfs:comment within an sh:PropertyShape to sh:description ([*GitHub Issue 357*](https://github.com/ucoProject/UCO/issues/357))
* Removed minimum cardinality bound on observable:isMimeEncoded and observable:isMultipart within observable:EmailMessageFacet ([*GitHub Issue 383*](https://github.com/ucoProject/UCO/issues/383))

## Documentation

Since UCO 0.8.0, generated documentation has been available at this site:

[https://ontology.unifiedcyberontology.org/](https://ontology.unifiedcyberontology.org/)

Be aware that the documentation will show the most recent release, until an ontology versioning strategy currently in initial implementation completes its testing.  The upper-left corner of the documentation pages shows the ontology version being reviewed.

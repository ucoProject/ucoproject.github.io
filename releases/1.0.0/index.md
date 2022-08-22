---
title: 1.0.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

###### Date: TBD

## Ontology File(s)


## Release Notes


#### Breaking Changes
*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*

* Added the resource 'uco' to the file layout ([*GitHub Issue 387*](https://github.com/ucoProject/UCO/issues/387))
* Imported the Collections Ontology to handle ordered lists ([*GitHub Issue 389*](https://github.com/ucoProject/UCO/issues/389))
* Disambiguated the two "Thread" classes within the observable namespace ([*GitHub Issue 391*](https://github.com/ucoProject/UCO/issues/391))
* Implemented ordering in observable:MessageThread ([*GitHub Issue 393*](https://github.com/ucoProject/UCO/issues/393))
* Added observable:startTime and observable:endTime to observable:EventFacet ([*GitHub Issue 396*](https://github.com/ucoProject/UCO/issues/396))
* Change minCount from 1 to 0 on multiple properties ([*GitHub Issue 428*](https://github.com/ucoProject/UCO/issues/428))

#### Changes
*(These are general changes to the preexisting ontology that are not breaking or range changes.)*

* Add Properties to observable:WindowsComputerSpecificationFacet ([*Change Proposal 35*](https://drive.google.com/file/d/152FAccATI0XIrrm8VFLmVDif-3hnxSBR/view)) 
* Representing Recoverability of Unallocated/Unavailable Files ([*Change Proposal 43*](https://drive.google.com/file/d/1EethPrq0ZpAIulrqviZV1etpvB64n0Pk/view))
* Cell Tower Representation ([*Change Proposal 101*](https://drive.google.com/file/d/1i6QGC_HhL3Ni81DVmZuUA5k5qtDPjV8e/view))
* Add service name and raw properties to observable:EventFacet ([*GitHub Issue 401*](https://github.com/ucoProject/UCO/issues/401))
* UCO should perform OWL 2 DL review with SHACL-SPARQL ([*GitHub Issue 406*](https://github.com/ucoProject/UCO/issues/406))
* Add time properties to observable:PDFFileFacet ([*GitHub Issue 421*](https://github.com/ucoProject/UCO/issues/421))
* Convert glom_graph.py to rdfpipe ([*GitHub Issue 424*](https://github.com/ucoProject/UCO/issues/424))

#### Bug Fixes
*(These are bugs found within the preexisting ontology that have been fixed.)*

* Remove errant rdf:List artifact ([*GitHub Pull Request 456*](https://github.com/ucoProject/UCO/pull/456))
* Remove usage of sh:declare ([*GitHub Pull Request 463*](https://github.com/ucoProject/UCO/pull/463))

## Documentation


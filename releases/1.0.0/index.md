---
title: 1.0.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

###### Date: 2022-08-31

## Ontology File(s)

[GitHub](https://github.com/ucoProject/UCO/releases/tag/1.0.0)

## Release Notes

UCO 1.0.0 incorporates required refinements and updates to provide a stable version for adopters to use. Following [SemVer](https://semver.org/spec/v2.0.0.html), additive improvements will continue to be accepted, but backwards-incompatible changes will be scheduled only for the 2.0.0 release, which will come after at least 6 months to possibly 12 months.


#### Breaking Changes
*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*

* Removed observable:MSISDN from observable:MobileDeviceFacet ([*GitHub Issue 361*](https://github.com/ucoProject/UCO/issues/361))
* Updated observable:EventRecordFacet to reference things rather than strings ([*GitHub Issue 375*](https://github.com/ucoProject/UCO/issues/375))
* Encoded core:hasFacet an inverse-functional property ([*GitHub Issue 379*](https://github.com/ucoProject/UCO/issues/379))
* Added the resource 'uco' to the file layout ([*GitHub Issue 387*](https://github.com/ucoProject/UCO/issues/387))
* Imported the Collections Ontology to handle ordered lists ([*GitHub Issue 389*](https://github.com/ucoProject/UCO/issues/389))
* Disambiguated the two "Thread" classes within the observable namespace ([*GitHub Issue 391*](https://github.com/ucoProject/UCO/issues/391))
* Implemented ordering in observable:MessageThread ([*GitHub Issue 393*](https://github.com/ucoProject/UCO/issues/393))
* Added OWL 2 DL review with SHACL-SPARQL for UCO ([*GitHub Issue 406*](https://github.com/ucoProject/UCO/issues/406))
  * (While this is not necessarily a backwards-incompatible change within the scope of UCO, it does identify what end users might not have realized were broader OWL errors.)
* Changed observable:Event to observable:EventRecord ([*GitHub Issue 416*](https://github.com/ucoProject/UCO/issues/416))
* Converted glom_graph.py to rdfpipe ([*GitHub Issue 424*](https://github.com/ucoProject/UCO/issues/424))
* Removed core:id ([*GitHub Issue 431*](https://github.com/ucoProject/UCO/issues/431))
* Removed core:type ([*GitHub Issue 433*](https://github.com/ucoProject/UCO/issues/433))
* Corrected OWL 2 DL syntax of enumerations of literals ([*GitHub Issue 435*](https://github.com/ucoProject/UCO/issues/435))
* Graph individuals are now required to not be blank nodes, and an IRI ending with a UUID is suggested ([*GitHub Issue 430*](https://github.com/ucoProject/UCO/issues/430))
* UCO now uses `owl:versionIRI`, `owl:priorVersion` and `owl:backwardCompatibleWith` or `owl:incompatibleWith` to declare and relate ontology versions ([*GitHub Issue 437*](https://github.com/ucoProject/UCO/issues/437))
  * (Due to new OWL-level testing, this has the same backwards-incompatibility interpretation as Issue 406.)

#### Changes
*(These are general changes to the preexisting ontology that are not breaking or range changes.)*

* Added properties to observable:WindowsComputerSpecificationFacet ([*Change Proposal 35*](https://drive.google.com/file/d/152FAccATI0XIrrm8VFLmVDif-3hnxSBR/view)) 
* Added represention for Recoverability of Unallocated/Unavailable Files ([*Change Proposal 43*](https://drive.google.com/file/d/1EethPrq0ZpAIulrqviZV1etpvB64n0Pk/view))
* Added representation for Cell Sites ([*Change Proposal 101*](https://drive.google.com/file/d/1i6QGC_HhL3Ni81DVmZuUA5k5qtDPjV8e/view))
* Added properties to represent application version history ([*GitHub Issue 372*](https://github.com/ucoProject/UCO/issues/372))
* Added observable:startTime and observable:endTime to observable:EventFacet ([*GitHub Issue 396*](https://github.com/ucoProject/UCO/issues/396))
* Added service name and raw properties to observable:EventFacet ([*GitHub Issue 401*](https://github.com/ucoProject/UCO/issues/401))
* Removed requirement of repeating all property constraints from parent to child classes ([*GitHub Issue 417*](https://github.com/ucoProject/UCO/issues/417))
* Added time properties to observable:PDFFileFacet ([*GitHub Issue 421*](https://github.com/ucoProject/UCO/issues/421))
* Changed minCount from 1 to 0 on multiple properties ([*GitHub Issue 428*](https://github.com/ucoProject/UCO/issues/428))
* Added the 'configuration' namespace to support tool and software details ([*GitHub Issue 432*](https://github.com/ucoProject/UCO/issues/432))
* Added various hierarchical classes to support observable:DeviceType ([*GitHub Issues 434*](https://github.com/ucoProject/UCO/issues/434))

#### Bug Fixes
*(These are bugs found within the preexisting ontology that have been fixed.)*

* Added missing observable:mutexName property ([*GitHub Issue 443*](https://github.com/ucoProject/UCO/issues/443))
* Removed confusion around core:Facet subclasses ([*GitHub Issue 445*](https://github.com/ucoProject/UCO/issues/445))
* Made types:ControlledDictionary a subclass of types:Dictionary ([*GitHub Issue 469*](https://github.com/ucoProject/UCO/issues/469))
* Removed errant rdf:List artifact ([*GitHub Pull Request 456*](https://github.com/ucoProject/UCO/pull/456))
  * Users should be aware that a yet-undiagnosed bug somewhere in the UCO format-normalizing tool chain causes extra `rdf:Lists` fragments to be emitted in some normalized `pyshacl` output.
* Removed usage of sh:declare ([*GitHub Pull Request 463*](https://github.com/ucoProject/UCO/pull/463))
* Fixed typo in rdfs:comment for observable:ApplicationFacet ([*GitHub Pull Request 466*](https://github.com/ucoProject/UCO/pull/466))
* Fixed MyPy issues within CI ([*GitHub Pull Request 478*](https://github.com/ucoProject/UCO/pull/478))


## Known issues

* After release, an errant concept reference in UCO 1.0.0 was found to prevent some OWL tools from parsing the ontology.  This bug was corrected as part of resolving [UCO Issue 488](https://github.com/ucoProject/UCO/issues/488), and the correction is released in [UCO 1.1.0](../1.1.0/).


## Documentation

Generated documentation is available at this site:

[https://ontology.unifiedcyberontology.org/](https://ontology.unifiedcyberontology.org/)

Be aware that the documentation at that site will only show the most recent release.  The upper-left corner of the documentation pages shows the ontology version being reviewed.

After the following UCO release, users interested seeing the rendered documentation at this version "Back in time" should locally clone the repository, check out [this branch](https://github.com/ucoProject/ontology.unifiedcyberontology.org/tree/archive/release-1.0.0), and follow the deployment directions in `CONTRIBUTE.md`.

---
title: 0.8.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

###### Date: 2022-03-23

## Ontology File(s)

[GitHub](https://github.com/ucoProject/UCO/releases/tag/0.8.0)

## Release Notes
UCO 0.8.0 is primarily focused on an initial implementation of Shapes Constraint Language (SHACL) review of semi-open vocabulary usage, restructuring of all UCO ontology IRIs and file structures to enable delivery of ontology resources from a new subdomain, flattening actionActionReferencesFacet properties directly onto action:Action, normalizing decimal number properties to xsd:decimal, improvements to unit and CI testing, numerous modifications and improvements to the Observable namespace, and correcting several minor issues and bugs.


#### Breaking Changes
*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*


* Remove observable:fileSystemType from FileFacet ([*Change Proposal 45*](https://drive.google.com/file/d/1YTgMo06AT73wV5aYwoUtAfJeMZoAS45g/view))
* Restructured repository by moving previously prefixed uco-* ontology files under new directory /ontology/* ([*Change Proposal 56*](https://drive.google.com/file/d/1PCjdCGw7wgFnPfbsCn0Fdvdnq9NDW6yA/view))
* Identifies software creators as uco-identity:Identity ([*Change Proposal 68*](https://drive.google.com/file/d/1-NOpnSqjWVbr-XMCFS8vXhjlMsv5njOb/view))
* Normalized all decimal number properties in the ontology to xsd:decimal ([*Change Proposal 80*](https://drive.google.com/file/d/1NKwEehcRDWh9zk9QOENckd7njYWxgVE4/view))
* Make observable:AlternateDataStream into a Facet subclass ([*Change Proposal 87*](https://drive.google.com/file/d/1qOo-0RGJErJ2w3yMGgs6lIlkldsEUHBb))
* Remove ActionReferenceFacet and move properties into action:Action ([*Change Proposal 89*](https://drive.google.com/file/d/1UFWFgSMaKZZ_Y1q1MS5hODkQC4QoBMTt/view))
* Adds support for multiple participants in the PhoneCallFacet ([*Change Proposal 92*](https://drive.google.com/file/d/1qJCgOLlMi1UZkibpuo6fRTT1DkllxuGv/view))
* Implement semi-openess of vocabularies ([*Change Proposal 100*](https://drive.google.com/file/d/13wRER2YI-nm9nMkr-1IPGex8GMejemcV/view))
  * This change implemented SHACL validation for all properties that had associated vocabulary assertions in Release 0.7.0. It did not add any new such vocabulary assertions to existing properties. For any properties without associated vocabulary assertions (e.g., core:kindOfRelationship), serialized values should be asserted simply as xsd:strings without any vocabulary-related datatype annotations. In JSON-LD that means to express a contained-within relationship, a plain `"Contained_Within"` string value should be used, instead of an datatype-annotating JSON dictionary `{"@type": "vocabulary:ObservableObjectRelationshipVocab", "@value": "Contained_Within"}`.
* Revise UCO IRI structure, similar to CASE CP-34, to utilize an "ontology" subdomain, end with a slash and remove @base ([*Change Proposal 107*](https://drive.google.com/file/d/14bT4_Yy2ZJrRK2Ndb0CpwMNoVHEeJbKu/view))
  * Users of UCO 0.7.0 and earlier should be aware that their UCO IRI prefixes should be adjusted.  For instance, the prefix of the Action namespace `https://unifiedcyberontology.org/ontology/uco/action#` is now `https://ontology.unifiedcyberontology.org/uco/action/`.


#### Changes
*(These are general changes to the preexisting ontology that are not breaking or range changes.)*

* Add AndroidDeviceFacet, with device information as properties as a subclass of Device ([*Change Proposal 50*](https://drive.google.com/file/d/15R0z_i2wt325tKRClCtcuq-bswU2kavx/view))
* Updated CI testing (Makefiles) to reflect repository restructure ([*Change Proposal 56*](https://drive.google.com/file/d/1PCjdCGw7wgFnPfbsCn0Fdvdnq9NDW6yA/view))
* Add vocabulary namespace to uco.ttl in uco-master ([*Change Proposal 82*](https://drive.google.com/file/d/1qQibtD9QAqciLOBkkk6WdDcrz7nEQZL2/view))
* Fix namespace prefix for WhoisContactTypeVocab from observable to vocabulary ([*Change Proposal 84*](https://drive.google.com/file/d/1KbYImZyxzL3kPfA9-SP4Xi_pXnEkOw0W/view))
* Remove sh:datatype property entries from observable.ttl added by SHACL data conversion errors ([*Change Proposal 85*](https://drive.google.com/file/d/1Wu2fQ5kYKxQWfmK-0s1IIBytKcnW0Tjw/view))
* Normalize unit tests for SHACL validation ([*Change Proposal 91*](https://drive.google.com/file/d/1qJCgOLlMi1UZkibpuo6fRTT1DkllxuGv))
* Remove duplicated and conflicting property description from uco-core:EnclosingCompilation ([*Change Proposal 95*](https://drive.google.com/file/d/1W8r5GWS1h3x7K-U5k23HVDF8aqvH29li/view))
* Add missing fields for "lastTimeContacted" to the ontology ([*Change Proposal 97*](https://drive.google.com/file/d/1185Uur_wPqdI8VBawZ4E4mplVu-gZkYR))
* Add missing "observable:to" field in EmailMessageFacet and MessageFacet ([*Change Proposal 102*](https://drive.google.com/file/d/1xaHhTl1Uls8MpMjL2P8KoGjqkklClYl-/view))
* Remove lower bounds in uco-observable:CallFacet to unrestrict cardinality ([*Change Proposal 103*](https://drive.google.com/file/d/1HHv5x2szbYtWToycNkrzikVCT87-vtjm/view))
* Removes lower bounds in uco-observable:NoteFacet as described by UCO CP-103 ([*Change Proposal 105*](https://drive.google.com/file/d/1-HgTtjkx-O7w_gQSiZFmwESJWWw6weR-/view))
* Expand uco-observable:WirelessNetworkConnectionFacet properties support of network details (password, SecurityMode) ([*Change Proposal 106*](https://drive.google.com/file/d/1OhrkdYXotZbIvSA-bHdG00URqrIj0_QQ/view))
* Fix vocabulary namespace which incorrectly maps to ContactAddressScopeVocab ([*Change Proposal 109*](https://drive.google.com/file/d/18WvZD3FSGBstq5r1QVmCDXrAWur0zCrJ/view))

## Documentation

Starting with UCO 0.8.0, generated documentation is available at this site:

[https://ontology.unifiedcyberontology.org/](https://ontology.unifiedcyberontology.org/)

Be aware that the documentation will show the most recent release, until an ontology versioning strategy currently in initial implementation completes its testing.  The upper-left corner of the documentation pages shows the ontology version being reviewed.

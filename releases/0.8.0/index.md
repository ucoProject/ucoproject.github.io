---
title: 0.8.0 Release
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

* Restructured repository by moving previously prefixed uco-* ontology files under new directory /ontology/* ([*Change Proposal 56*](https://drive.google.com/file/d/1PCjdCGw7wgFnPfbsCn0Fdvdnq9NDW6yA/view))
* Adds support for multiple participants in the PhoneCallFacet ([*Change Proposal 92*](https://drive.google.com/file/d/1qJCgOLlMi1UZkibpuo6fRTT1DkllxuGv/view))

#### Changes
*(These are general changes to the preexisting ontology that are not breaking or range changes.)*
* Remove observable:fileSystemType from FileFacet ([*Change Proposal 45*](https://drive.google.com/file/d/1YTgMo06AT73wV5aYwoUtAfJeMZoAS45g/view))
* Add AndroidDeviceFacet, with device information as properties as a subclass of Device ([*Change Proposal 50*](https://drive.google.com/file/d/15R0z_i2wt325tKRClCtcuq-bswU2kavx/view))
* Updated CI testing (Makefiles) to reflect repository restructure ([*Change Proposal 56*](https://drive.google.com/file/d/1PCjdCGw7wgFnPfbsCn0Fdvdnq9NDW6yA/view))
* Identifies software creators as uco-identity:Identity ([*Change Proposal 68*](https://drive.google.com/file/d/1-NOpnSqjWVbr-XMCFS8vXhjlMsv5njOb/view))
* Normalized all decimal number properties in the ontology to xsd:decimal ([*Change Proposal 80*](https://drive.google.com/file/d/1NKwEehcRDWh9zk9QOENckd7njYWxgVE4/view))
* Add vocabulary namespace to uco.ttl in uco-master ([*Change Proposal 82*](https://drive.google.com/file/d/1qQibtD9QAqciLOBkkk6WdDcrz7nEQZL2/view))
* Fix namespace prefix for WhoisContactTypeVocab from observable to vocabulary ([*Change Proposal 84*](https://drive.google.com/file/d/1KbYImZyxzL3kPfA9-SP4Xi_pXnEkOw0W/view))
* Remove sh:datatype property entries from observable.ttl added by SHACL data conversion errors ([*Change Proposal 85*](https://drive.google.com/file/d/1Wu2fQ5kYKxQWfmK-0s1IIBytKcnW0Tjw/view))
* Make observable:AlternateDataStream into a Facet subclass ([*Change Proposal 87*](https://drive.google.com/file/d/1qOo-0RGJErJ2w3yMGgs6lIlkldsEUHBb))
* Remove ActionReferenceFacet and move properties into action:Action ([*Change Proposal 89*](https://drive.google.com/file/d/1UFWFgSMaKZZ_Y1q1MS5hODkQC4QoBMTt/view))
* Normalize unit tests for SHACL validation ([*Change Proposal 91*](https://drive.google.com/file/d/1qJCgOLlMi1UZkibpuo6fRTT1DkllxuGv))
* Remove duplicated and conflicting property description from uco-core:EnclosingCompilation ([*Change Proposal 95*](https://drive.google.com/file/d/1W8r5GWS1h3x7K-U5k23HVDF8aqvH29li/view))
* Add missing fields for "lastTimeContacted" to the ontology ([*Change Proposal 97*](https://drive.google.com/file/d/1185Uur_wPqdI8VBawZ4E4mplVu-gZkYR))
* Add missing "observable:to" field in EmailMessageFacet and MessageFacet ([*Change Proposal 102*](https://drive.google.com/file/d/1xaHhTl1Uls8MpMjL2P8KoGjqkklClYl-/view))
* Remove lower bounds in uco-observable:CallFacet to unrestrict cardinality ([*Change Proposal 103*](https://drive.google.com/file/d/1HHv5x2szbYtWToycNkrzikVCT87-vtjm/view))
* Removes lower bounds in uco-observable:NoteFacet as described by UCO CP-103 ([*Change Proposal 105*](https://drive.google.com/file/d/1-HgTtjkx-O7w_gQSiZFmwESJWWw6weR-/view))
* Expand uco-observable:WirelessNetworkConnectionFacet properties support of network details (password, SecurityMode) ([*Change Proposal 106*](https://drive.google.com/file/d/1OhrkdYXotZbIvSA-bHdG00URqrIj0_QQ/view))
* Revise UCO IRI structure, similar to CASE CP-34, to end with a slash and remove @base ([*Change Proposal 107*](https://drive.google.com/file/d/14bT4_Yy2ZJrRK2Ndb0CpwMNoVHEeJbKu/view))
* Fix vocabulary namespace which incorrectly maps to ContactAddressScopeVocab ([*Change Proposal 109*](https://drive.google.com/file/d/18WvZD3FSGBstq5r1QVmCDXrAWur0zCrJ/view))
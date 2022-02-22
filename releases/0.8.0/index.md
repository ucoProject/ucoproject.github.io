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
* Remove ActionReferenceFacet and move properties into action:Action ([*Change Proposal 89*](https://drive.google.com/file/d/1njOUmpNNCTolnGkXoKv5ext-ZK18108u/view))

#### Changes
*(These are general changes to the preexisting ontology that are not breaking or range changes.)*

* Remove observable:fileSystemType from FileFacet ([*Change Proposal 45*](https://drive.google.com/file/d/1ycbboFe8wEYzD3AD6lbUadwXXFuGF3Dl/view))
* Updated CI testing (Makefiles) to reflect repository restructure ([*Change Proposal 56*](https://drive.google.com/file/d/1PCjdCGw7wgFnPfbsCn0Fdvdnq9NDW6yA/view))
* Normalized all decimal number properties in the ontology to xsd:decimal ([*Change Proposal 80*](https://drive.google.com/file/d/1NKwEehcRDWh9zk9QOENckd7njYWxgVE4/view))
* Add vocabulary namespace to uco.ttl in uco-master ([*Change Proposal 82*](https://drive.google.com/file/d/1qQibtD9QAqciLOBkkk6WdDcrz7nEQZL2/view))
* Fix namespace prefix for WhoisContactTypeVocab from observable to vocabulary ([*Change Proposal 84*](https://drive.google.com/file/d/1KbYImZyxzL3kPfA9-SP4Xi_pXnEkOw0W/view))
* Remove sh:datatype property entries from observable.ttl added by SHACL data conversion errors ([*Change Proposal 85*](https://drive.google.com/file/d/1Wu2fQ5kYKxQWfmK-0s1IIBytKcnW0Tjw/view))
* Make observable:AlternateDataStream into a Facet subclass ([*Change Proposal 87*](https://drive.google.com/file/d/1qOo-0RGJErJ2w3yMGgs6lIlkldsEUHBb))
* Add missing fields for "lastTimeContacted" to the ontology ([*Change Proposal 97*](https://drive.google.com/file/d/1185Uur_wPqdI8VBawZ4E4mplVu-gZkYR))

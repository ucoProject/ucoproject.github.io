---
title: 1.4.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

*Date: TBD*


## Ontology File(s)


## Release Notes


### Focus


#### Breaking Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*

UCO 2.0.0 **will** consider the following breaking changes.  They are implemented in UCO 1.4.0 as "Warning"-level SHACL violations; in 2.0.0, they will be "Error"-level.

* Warned if target or source on an `ObservableRelationship` are not `Observable`s ([*GitHub Issue 573*](https://github.com/ucoProject/UCO/issues/573))
* Warned of prior disjointedness declarations in `core:` and `types:` ([*GitHub Issue 586*](https://github.com/ucoProject/UCO/issues/586))
* Warned if an `AlternateDataStream` instance is not also a `FileSystemObject` ([*GitHub Issue 590*](https://github.com/ucoProject/UCO/issues/590))
* Warned if a `observable:Disk` instance is not also a `observable:StorageMedium` ([*GitHub Issue 612*](https://github.com/ucoProject/UCO/issues/612))


#### Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology.)*

* Removed 1-member minimum on core:ContextualCompilation ([*GitHub Issue 599*](https://github.com/ucoProject/UCO/issues/599))
* Added review mechanisms for key-uniqueness in `types:Dictionary` ([*GitHub Issue 602*](https://github.com/ucoProject/UCO/issues/602))
   - Added new subclasses of `types:Dictionary`, `types:ProperDictionary` and `types:ImproperDictionary`
   - Added test for key uniqueness of dictionary entries for `types:Dictionary`, with "Warning"-level SHACL violations raised if repeated keys are found
   - Encoded key uniqueness as a SHACL-validated requirement in `types:ProperDictionary`
   - Changed definition of `types:Dictionary` to separate expectation of key uniqueness in `types:Dictionary` from formally validated requirement in `types:ProperDictionary`
* Added `core:objectStatus` ([*GitHub Issue 549*](https://github.com/ucoProject/UCO/issues/549))


#### Bug Fixes

*(These are bugs found within the preexisting ontology that have been fixed.)*

* Replaced errant reference to non-existent concept `owl:Datatype` ([*GitHub Issue 584*](https://github.com/ucoProject/UCO/issues/584))


## Documentation

---
title: 1.2.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

*Date: 2023-03-29*


## Ontology File(s)

[GitHub](https://github.com/ucoProject/UCO/releases/tag/1.2.0)


## Release Notes

UCO 1.2.0 incorporates required refinements and updates, building on the stable 1.0.0 release.  Following [SemVer](https://semver.org/spec/v2.0.0.html), additive improvements will continue to be accepted, but backwards-incompatible changes will be scheduled only for the 2.0.0 release, which will come after at least 6 months to possibly 12 months.

This release includes additive updates as well as exercising a process for introducing backwards-incompatible changes in preparation for UCO 2.0.0.  A new feature incorporates construction of support for offline development with some ontology tools that require local-file substitution for imported IRIs.  Community member testing identified and mitigated environmental assumptions revealed by exercising UCO with processing frameworks not included in Cyber Domain Ontology automated testing.  Some mobile device property cardinalities are now relaxed care of a user encountering and reporting an encountered, uncommon device configuration.  Vocabularies have expanded to cover further cryptography needs.  One bug fix in class alignment for a "Data structure" class (`types:Thread`) has introduced a backwards-incompatible fix for the 2.0.0 release cycle, with a warning now being raised within the 1.x.0 release cycle if the future pattern enforcement will fail.


### Focus


#### Breaking Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*


#### Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology.)*

* Added support for Protégé ([*GitHub Issue 449*](https://github.com/ucoProject/UCO/issues/449))
* Added `observable:StorageMediumFacet` and `observable:totalStorageCapacityInBytes` ([*GitHub Issue 501*](https://github.com/ucoProject/UCO/issues/501))
* `observable:IMEI` now has an unrestricted cardinality within `observable:MobileDeviceFacet` ([*GitHub Issue 521*](https://github.com/ucoProject/UCO/issues/521))
* `vocabulary:ObservableObjectRelationshipVocab` now includes `Signed_By` ([*GitHub Issue 525*](https://github.com/ucoProject/UCO/issues/525))
* `vocabulary:HashNameVocab` now lists SHA-3 hash functions ([*GitHub Issue 526*](https://github.com/ucoProject/UCO/issues/526))


#### Bug Fixes

*(These are bugs found within the preexisting ontology that have been fixed.)*

* Deprecated and replaced `observable:creationTime` with `observable:observableCreatedTime` ([*GitHub Issue 508*](https://github.com/ucoProject/UCO/issues/508))
* Aligned `types:Thread` with `core:UcoThing` subclass hierarchy; consequently added CI tests to ensure `core:UcoObject` and `co:Collection` are disjoint in accordance with current implementation patterns ([*GitHub Issue 509*](https://github.com/ucoProject/UCO/issues/509))
* Fixed classname reference for `UcoThing-indentifier-regex-shape` ([*GitHub Pull Request 510*](https://github.com/ucoProject/UCO/pull/510))
* Added missing prefixes for a few SPARQL constraints ([*GitHub Issue 513*](https://github.com/ucoProject/UCO/issues/513))
* Clarified Continuous Integration test output for vocabulary synchronization ([*GitHub Pull Request 528*](https://github.com/ucoProject/UCO/pull/528))


## Documentation

Generated documentation is available at this site:

[https://ontology.unifiedcyberontology.org/](https://ontology.unifiedcyberontology.org/)

Be aware that the documentation at that site will only show the most recent release.  The upper-left corner of the documentation pages shows the ontology version being reviewed.

After the following UCO release, users interested seeing the rendered documentation at this version "Back in time" should locally clone the repository, check out [this branch](https://github.com/ucoProject/ontology.unifiedcyberontology.org/tree/archive/release-1.2.0), and follow the deployment directions in `CONTRIBUTE.md`.

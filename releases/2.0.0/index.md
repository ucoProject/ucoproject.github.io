---
title: 2.0.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

*Date: TBD*


## Ontology File(s)


## Release Notes


### Focus


### Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology.)*


#### Breaking Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*

* Enforced `observable:File` and `:URL` disjointedness ([*GitHub Issue 536*](https://github.com/ucoProject/UCO/issues/536))
* Required target or source on an `ObservableRelationship` be `Observable`s ([*GitHub Issue 573*](https://github.com/ucoProject/UCO/issues/573))
* Enforced prior disjointedness declarations in `core:` and `types:` ([*GitHub Issue 586*](https://github.com/ucoProject/UCO/issues/586))
* Revised `pattern:patternExpression` to be object property, and tested for error form ([*GitHub Issue 562*](https://github.com/ucoProject/UCO/issues/562))


#### General changes

*(These are general changes to the preexisting ontology that are not breaking or range changes.)*


#### Bug Fixes

*(These are bugs found within the preexisting ontology that have been fixed.)*

* Removed deprecated property: `observable:creationTime` ([*GitHub Issue 508*](https://github.com/ucoProject/UCO/issues/508))
* Aligned `types:Thread` with `core:UcoInherentCharacterizationThing` ([*GitHub Issue 509*](https://github.com/ucoProject/UCO/issues/509))
* Designated `observable:ObservablePattern` a subclass of `pattern:Pattern` ([*GitHub Issue 543*](https://github.com/ucoProject/UCO/issues/543))
* Designated `action:ActionLifecycle` a subclass of `action:ActionPattern` ([*GitHub Issue 556*](https://github.com/ucoProject/UCO/issues/556))
* Changed `AlternateDataStream` parent class to `FileSystemObject` ([*GitHub Issue 590*](https://github.com/ucoProject/UCO/issues/590))


## Documentation

---
title: 1.1.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

*Date: 2022-11-22*


## Ontology File(s)

[GitHub](https://github.com/ucoProject/UCO/releases/tag/1.1.0)


## Release Notes

UCO 1.1.0 incorporates required refinements and updates, building on the stable 1.0.0 release.  Following [SemVer](https://semver.org/spec/v2.0.0.html), additive improvements will continue to be accepted, but backwards-incompatible changes will be scheduled only for the 2.0.0 release, which will come after at least 6 months to possibly 12 months.

This release adds an Analysis namespace for representing analytic actions and outcomes, and starts a framework for representing classifications by Artifical Intelligence frameworks.  Database cells can now be represented and related to various levels of a database storage hierarchy.  Two properties found to lack ranges have had ranges assigned in accordance with existing related properties.  Additional conformance testing has been added to verify UCO conformance with its design vocabularies (currently RDF, RDFS, OWL, and SHACL).  Various SHACL-OWL tests have received corrections.


### Focus


#### Breaking Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*


#### Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology.)*

* Added Analysis namespace and relevant classes/properties ([*GitHub Issue 400*](https://github.com/ucoProject/UCO/issues/400))
* Added the ability to represent a database record at the cell level ([*GitHub Issue 415*](https://github.com/ucoProject/UCO/issues/415))
* Added a typo checker to upstream design vocabularies ([*GitHub Issue 488*](https://github.com/ucoProject/UCO/issues/488))
* Expanded CI trigger-branches to include multiple develops and unstables ([*GitHub Issue 493*](https://github.com/ucoProject/UCO/issues/493))
* Integrated a SHACL conformance checking system into CI ([*GitHub Issue 504*](https://github.com/ucoProject/UCO/issues/504))

#### Bug Fixes

*(These are bugs found within the preexisting ontology that have been fixed.)*

* Added missing types to untyped properties ([*GitHub Issue 487*](https://github.com/ucoProject/UCO/issues/487))
* Removed the errant concept of owl:ontologyIRI ([*GitHub Issue 491*](https://github.com/ucoProject/UCO/issues/491))
* Fixed spelling pattern for some SHACL-SPARQL components ([*GitHub Issue 499*](https://github.com/ucoProject/UCO/issues/499))
* Reversed logic for SHACL-SPARQL constraints sequence paths review ([*GitHub Issue 502*](https://github.com/ucoProject/UCO/issues/502))

## Documentation

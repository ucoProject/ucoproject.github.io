---
title: 1.3.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

*Date: 2024-01-23*


## Ontology File(s)

[GitHub](https://github.com/ucoProject/UCO/releases/tag/1.3.0)


## Release Notes

UCO 1.3.0 incorporates required refinements and updates, building on the stable 1.0.0 release.  Following [SemVer](https://semver.org/spec/v2.0.0.html), additive improvements will continue to be accepted, but backwards-incompatible changes will be scheduled only for the 2.0.0 release, which will come after at least 6 months to possibly 12 months.

This release includes additive updates and further preparations for backwards-incompatible changes in preparation for UCO 2.0.0.  A clarifying disjointedness statement has been added to distinguish `observable:File`s from `observable:URL`s, in response to a question on how to represent a URL that serves a file with expected contents.  Events are now representable with the general-purpose class `core:Event`, fit for further specializing.  A test of OWL syntax has had its scope corrected to prevent incorrect flagging of `rdf:List` forms outside of class descriptions.


### Focus


#### Breaking Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*

UCO 2.0.0 **will** consider the following breaking changes.  They are implemented in UCO 1.3.0 as "Warning"-level SHACL violations; in 2.0.0, they will be "Error"-level.

* Declared and warned of `observable:File` and `:URL` disjointedness ([*GitHub Issue 536*](https://github.com/ucoProject/UCO/issues/536))


#### Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology.)*

* Added `core:Event` ([*GitHub Issue 541*](https://github.com/ucoProject/UCO/issues/541))
   - Designated `action:Action` and `core:Event` disjoint ([*GitHub Issue 563*](https://github.com/ucoProject/UCO/issues/563))


#### Bug Fixes

*(These are bugs found within the preexisting ontology that have been fixed.)*

* Reduced UCO OWL RDF List review scope to OWL Sequences ([*GitHub Issue 571*](https://github.com/ucoProject/UCO/issues/571))


## Documentation

Generated documentation is available at this site:

[https://ontology.unifiedcyberontology.org/](https://ontology.unifiedcyberontology.org/)

Be aware that the documentation at that site will only show the most recent release.  The upper-left corner of the documentation pages shows the ontology version being reviewed.

After the following UCO release, users interested seeing the rendered documentation at this version "Back in time" should locally clone the repository, check out [this branch](https://github.com/ucoProject/ontology.unifiedcyberontology.org/tree/archive/release-1.3.0), and follow the deployment directions in `CONTRIBUTE.md`.

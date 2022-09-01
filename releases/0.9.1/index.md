---
title: 0.9.1 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

*Date: 2022-08-31*


## Ontology File(s)

[GitHub](https://github.com/ucoProject/UCO/releases/tag/0.9.1)


## Release Notes

UCO 0.9.1 implements a starting point in UCO for ontology version designation and backwards-compatibility tracking.  OWL versioning features are implemented and tested on top of UCO 0.9.0, as part of demonstrating version incrementing for UCO 1.0.0 and exercising the documentation deployment process.  No other changes are implemented since UCO 0.9.0.


### Breaking Changes
*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*

*(None.)*


### Changes
*(These are general changes to the preexisting ontology that are not breaking or range changes.)*

* `owl:versionIRI` and UCO-specific tests for its usage in the transitive closure of `owl:imports` between UCO ontologies have been added  ([*GitHub Issue 437*](https://github.com/ucoProject/UCO/issues/437))


## Documentation

Coming soon to this site:

[https://ontology.unifiedcyberontology.org/](https://ontology.unifiedcyberontology.org/)

Be aware that the documentation at that site will only show the most recent release.  The upper-left corner of the documentation pages shows the ontology version being reviewed.

After the following UCO release, users interested seeing the rendered documentation at this version "Back in time" should locally clone the repository, check out [this branch](https://github.com/ucoProject/ontology.unifiedcyberontology.org/tree/archive/release-0.9.1), and follow the deployment directions in `CONTRIBUTE.md`.

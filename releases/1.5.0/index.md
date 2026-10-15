---
title: 1.5.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

*Date: 2026-07-24*


## Ontology File(s)

[GitHub](https://github.com/ucoProject/UCO/releases/tag/1.5.0)


## Release Notes

UCO 1.5.0 incorporates required refinements and updates, building on the stable 1.0.0 release.  Following [SemVer](https://semver.org/spec/v2.0.0.html), additive improvements will continue to be accepted, but backwards-incompatible changes will be scheduled only for the 2.0.0 release, which will come after at least 6 months to possibly 12 months.

This release introduces a mechanism for framework developers to manage a catalogue of enumerated classes of actions.  The UCO Action namespace now defines UCO's first meta-class, `Technique,` whose instances are themselves specialized subclasses of `Action`.  This adds a third tier above the usual two-tier class structure: the `Technique` meta-class, the `Technique` classes that instantiate it, and the `Actions` that instantiate those.  This design allows a specific `Action` to *follow* a general `Technique` explicitly by being typed with that `Technique` class, and enables SHACL validation of requirements specific to that `Technique`.  For instance, a disk imaging `Technique` can require a device of a certain class, such as a hardware write blocker.  Then an `Action` can *follow* this `Technique` using a specific disk imaging tool with a given hardware write blocker. A `Technique` class can refine one or more parent `Techniques` bringing the benefits of inheretance and multi-classing. The design supports controlled collection of `Action`-subclasses within a framework, and also supports extension of one framework's `Techniques` by another, while keeping clear the framework within which any `Technique`---extension or not---is defined.


### Focus


#### Breaking Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*


#### Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology.)*

* Added `core:UcoType` and `core:Technique` ([*GitHub Issue 666*](https://github.com/ucoProject/UCO/issues/666))


#### Bug Fixes

*(These are bugs found within the preexisting ontology that have been fixed.)*

* Documentation typos have been corrected, in:
   - the `rdfs:label` for `observable:MessageThread` ([*GitHub Issue 667*](https://github.com/ucoProject/UCO/issues/667))
   - the `rdfs:comment` for `types:Thread` ([*GitHub Issue 669*](https://github.com/ucoProject/UCO/issues/669))
   - the `rdfs:comment` for `observable:bluetoothDeviceName` ([*GitHub Issue 670*](https://github.com/ucoProject/UCO/issues/670))


## Documentation

Generated documentation is available at this site:

[https://ontology.unifiedcyberontology.org/](https://ontology.unifiedcyberontology.org/)

Be aware that the documentation at that site will only show the most recent release.  The upper-left corner of the documentation pages shows the ontology version being reviewed.

After the following UCO release, users interested seeing the rendered documentation at this version "Back in time" should locally clone the repository, check out [this branch](https://github.com/ucoProject/ontology.unifiedcyberontology.org/tree/archive/release-1.5.0-2), and follow the deployment directions in `CONTRIBUTE.md`.

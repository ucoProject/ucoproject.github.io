---
title: 1.4.0 Release
layout: releases
custom_css: releases
---

# {{ page.title }}

*Date: 2025-05-28*


## Ontology File(s)


## Release Notes

UCO 1.4.0 incorporates required refinements and updates, building on the stable 1.0.0 release.  Following [SemVer](https://semver.org/spec/v2.0.0.html), additive improvements will continue to be accepted, but backwards-incompatible changes will be scheduled only for the 2.0.0 release, which will come after at least 6 months to possibly 12 months.

This release includes additive updates and further preparations for backwards-incompatible changes in preparation for UCO 2.0.0.

Additions include new classes and properties, and new placements for some existing properties.  The `types:Dictionary` class now has specializations to handle when a dictionary must have unique keys, and/or detect when a conflicting second assignment for a key is present (enacted with classes `types:ProperDictionary` and `types:ImproperDictionary`), in response to finding an ambiguity in the pre-1.4.0 definition of `types:Dictionary`.  `core:informalType` now unifies properties that are used to describe an object's type with an unrestricted or semi-restricted string.  `core:objectStatus` is added to optionally house a graph node's implementation status.  `observable:Device`s now have CPEs associable in `observable:DeviceFacet`, consistent with the CPE Naming Specification, Version 2.3 ([NIST IR 7695](https://nvlpubs.nist.gov/nistpubs/Legacy/IR/nistir7695.pdf)).

One relaxation put into place is that `core:ContextualCompilation` is now permitted to have no members, for instances when the definition context constrains away the possibility for members.  E.g., a contextual compilation can now be recorded of files in a certain directory that happens to be empty.

Coming backwards-incompatible changes include some class rearrangement, link constraining, and a semi-open vocabulary usage revision (with the vocabulary matter described in the following subsection).  Several classes have had their position in the class hierarchy position adjusted (`observable:AlternateDataStream`, `observable:Disk`, and `observable:OperatingSystem`).  Disjointedness declarations that weren't previously encoded outside of an OWL statement are now started with a SHACL warning-level check.  `observable:ObservableRelationship` now warns if non-`observable:Observable`s are the related things.


### Semi-open vocabulary syntax change

One new data behavior likely to catch user attention is a warning, which will become an error in UCO 2.0.0, around semi-open vocabulary syntax forms.  Generally, Literals that were using a UCO (or CASE) semi-open vocabulary datatype will now typed as `xsd:string`, which, as the default datatype for RDF Literals, generally relieves the need for datatype annotations on these vocabulary Literals.  For example, this would be how a `uco-types:Hash` was represented prior to UCO 1.4.0:

```json
{
    "@context": {
        "kb": "http://example.org/kb/",
        "uco-types": "https://ontology.unifiedcyberontology.org/uco/types/",
        "uco-vocabulary": "https://ontology.unifiedcyberontology.org/uco/vocabulary/",
        "xsd": "http://www.w3.org/2001/XMLSchema#"
    },
    "@graph": [
        {
            "@id": "kb:Hash-6c971341-17c9-46cd-ab32-d274fd064c9b",
            "@type": "uco-types:Hash",
            "uco-types:hashMethod": {
                "@type": "uco-vocabulary:HashNameVocab",
                "@value": "SHA3-256"
            },
            "uco-types:hashValue": {
                "@type": "xsd:hexBinary",
                "@value": "a7ffc6f8bf1ed76651c14756a061d662f580ff4de43b49fa82d80a4b80f8434a"
            }
        }
    ]
}
```

This is how a `uco-types:Hash` will be represented at and after UCO 1.4.0.  Note the reduction in `uco-types:hashMethod`.

```json
{
    "@context": {
        "kb": "http://example.org/kb/",
        "uco-types": "https://ontology.unifiedcyberontology.org/uco/types/",
        "xsd": "http://www.w3.org/2001/XMLSchema#"
    },
    "@graph": [
        {
            "@id": "kb:Hash-6c971341-17c9-46cd-ab32-d274fd064c9b",
            "@type": "uco-types:Hash",
            "uco-types:hashMethod": "SHA3-256",
            "uco-types:hashValue": {
                "@type": "xsd:hexBinary",
                "@value": "a7ffc6f8bf1ed76651c14756a061d662f580ff4de43b49fa82d80a4b80f8434a"
            }
        }
    ]
}
```

See ([*UCO GitHub Issue 629*](https://github.com/ucoProject/UCO/issues/629)) for further descriptions and motivations of this revision.


### Focus


#### Breaking Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)*

UCO 2.0.0 **will** consider the following breaking changes.  They are implemented in UCO 1.4.0 as "Warning"-level SHACL violations; in 2.0.0, they will be "Error"-level.

* Warned if target or source on an `ObservableRelationship` are not `Observable`s ([*GitHub Issue 573*](https://github.com/ucoProject/UCO/issues/573))
* Warned of prior disjointedness declarations in `core:` and `types:` ([*GitHub Issue 586*](https://github.com/ucoProject/UCO/issues/586))
* Warned if an `AlternateDataStream` instance is not also a `FileSystemObject` ([*GitHub Issue 590*](https://github.com/ucoProject/UCO/issues/590))
* Warned if a `observable:Disk` instance is not also a `observable:StorageMedium` ([*GitHub Issue 612*](https://github.com/ucoProject/UCO/issues/612))
* Warned if an `OperatingSystem` instance is not also a `Software` ([*GitHub Issue 632*](https://github.com/ucoProject/UCO/issues/632))


#### Changes

*(These are changes to ontologies, classes or properties in the preexisting ontology.)*

* Added `core:objectStatus` ([*GitHub Issue 549*](https://github.com/ucoProject/UCO/issues/549))
* Removed 1-member minimum on `core:ContextualCompilation` ([*GitHub Issue 599*](https://github.com/ucoProject/UCO/issues/599))
* Added review mechanisms for key-uniqueness in `types:Dictionary` ([*GitHub Issue 602*](https://github.com/ucoProject/UCO/issues/602))
   - Added new subclasses of `types:Dictionary`, `types:ProperDictionary` and `types:ImproperDictionary`
   - Added test for key uniqueness of dictionary entries for `types:Dictionary`, with "Warning"-level SHACL violations raised if repeated keys are found
   - Encoded key uniqueness as a SHACL-validated requirement in `types:ProperDictionary`
   - Changed definition of `types:Dictionary` to separate expectation of key uniqueness in `types:Dictionary` from formally validated requirement in `types:ProperDictionary`
* Added `observable:cpeid` to `observable:DeviceFacet` ([*GitHub Issue 624*](https://github.com/ucoProject/UCO/issues/624))
* Added `core:informalType` and linked as parent of type-describing properties ([*GitHub Issue 640*](https://github.com/ucoProject/UCO/issues/640))


#### Bug Fixes

*(These are bugs found within the preexisting ontology that have been fixed.)*

* Replaced errant reference to non-existent concept `owl:Datatype` ([*GitHub Issue 584*](https://github.com/ucoProject/UCO/issues/584))
* Removed `owl:onDatatype` from vocabulary definitions ([*GitHub Issue 593*](https://github.com/ucoProject/UCO/issues/593))
* Revised vocabulary pattern ([*GitHub Issue 629*](https://github.com/ucoProject/UCO/issues/629))
* Fixed copy-paste error ([*GitHub Pull Request 654*](https://github.com/ucoProject/UCO/pull/654))


## Documentation

Generated documentation is available at this site:

[https://ontology.unifiedcyberontology.org/](https://ontology.unifiedcyberontology.org/)

Be aware that the documentation at that site will only show the most recent release.  The upper-left corner of the documentation pages shows the ontology version being reviewed.

After the following UCO release, users interested seeing the rendered documentation at this version "Back in time" should locally clone the repository, check out [this branch](https://github.com/ucoProject/ontology.unifiedcyberontology.org/tree/archive/release-1.4.0), and follow the deployment directions in `CONTRIBUTE.md`.

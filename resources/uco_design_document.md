---
title: UCO Design Document
jumbo_desc:
---

# 1 UCO Foundational Principles
The following foundational principles outline the fundamental ethos of the Cyber Domain Ontology ecosystem. These principles are immutable and lay the foundation for the activities of the Technical Steering Committee (TSC) and relevant initiatives within the Cyber Domain Ontology project:

1. Concepts and capabilities that are relevant to more than one application domain should be placed into UCO. Concepts and capabilities that are relevant to a single application domain should be placed in the relevant application domain ontology.
1. UCO concept semantics, structure and constraints at both a design and implementation level must always support broad applicability across the cyber domain and not be biased to any particular one or more application domains. Maintaining broad applicability may involve compromises from optimal solutions for any single application domain in order to support the strategic objective for the overall ecosystem initiative.
1. Due to the inherency of incomplete understanding and conceptual coverage at any point in time, the inexorable evolution of domain needs over time, and the uniquely specialized needs of adopters, UCO must support practical extensibility at both an explicit design level and an implicit user level.
	1. 	At an explicit design-level, this would include the potential for adopters to define relevant class, property, datatype or vocabulary extensions to UCO to support their needs as long as they are not in conflict with existing UCO definitions and structures. If relevant to other adopters and multiple application domains these extensions may be considered for future inclusion in UCO.
	1. 	At an implicit user-level, this would include classes asserting open shapes (to allow custom properties to be added at time of use) and defined vocabularies to be open to provide suggested values for consistent normalization but also allow values outside the predefined set. Validation should flag such customizations as warnings but not as errors.
1. UCO must seek a balance between top-down and bottom-up ontological rigor with a clear decisive bias toward practicality and flexibility.
1. UCO should bias toward inclusion rather than exclusion of conceptual coverage. Concepts and structure should be included in UCO if they are relevant to more than one application domain even if they are not relevant to all application domains.

&nbsp;


# 2 Ontological Approach and Intent

 The primary purpose of the Unified Cyber Ontology (UCO) is to provide a consistent basis model for expressing, exchanging and analyzing information native to the cyber domain or relevant to the implementation, execution or results of analytic processes related to the cyber domain.
 
 At a fundamental level this requires defining relevant concepts and the relevant relationships between them. This would include both high-level domain concepts as well as more granular concepts involved in characterizing the domain level concepts.
 
 These definitions can then support expression of a diverse range of instance content of these concepts and relationships. Unlike many information standardization efforts targeted to support either solely information exchange or information analysis, UCO is very intentionally targeted to support both including analysis unbounded by any particular scope of exchange. Similarly, UCO is targeted to support expression of information across the scope of temporality including characterizations of past, present or potential future occurrences or states.
 
 UCO recognizes the highly complex, diverse and rapidly evolving nature of the cyber domain and as such begins from a fundamental presumption that UCO can never fully define a complete model that provides adequate definition for all possible relevant use cases and scenarios. At any point in time no understanding can be presumed complete given the extreme diversity of the domain. Specification of UCO will always be an activity trailing the evolution of the domain over time. There will always be niche use cases and scenarios within the domain that are critical to support as part of the broader domain but not appropriate to attempt to standardize formally within the broadly targeted UCO. As such, to support practical adoption and use it is a critical requirement that UCO not only define known relevant concepts and relationships but also provide mechanisms for extension of the UCO at both a design and end-user level independent of current formal UCO specification at any point in time. The leading point of the evolutionary spear will typically be end-users discovering required use cases and scenarios that are not yet supported by the formal UCO specification and will need to be free to express what they need to express in a way that is as integrated as possible with existing specified UCO. Over time these end-user evolutions will be reviewed by adopting organizations or communities and defined as design-level extensions to UCO that provide improved clarity, consistency and rigor than simple ad-hoc user level extensions. Over time these design-level extensions can be submitted to the UCO community for consideration and possible inclusion in future releases of the formal UCO specification.
 
 Efforts to standardize information representations within a given organization or system context are often pursued as formal data models defining an enterprise's data elements and connections between them. Such an approach can be effective when the exact scope, nature and use of the data is well-understood and tightly bound to a context controlled by the organization. Such approaches are typically not effective for standardizing information representations outside the scope of a given organization as such presumptions of homogeneity and control cease to be valid.
 
 Efforts to standardize information exchange representations between systems or organizations are often pursued as defined serialization schemas (json schema, XML schema, protocol buffers, etc.). Such schemas provide consistent lexical and syntactic structure for known exchange structures. However such schematic approaches also suffer from significant limitations. 

 * Often lack definition of meaning for the concepts and relationships involved. Where meaning is provided it is typically in the form of an accompanying prose specifications that often suffer from ambiguities and inconsistencies due to human interpretation and lack a formal mechanism to ensure the formal schema specification and potential validation mechanism fully align to the prose specification.
 * Are often brittle to evolution and change where changes in one are may cause unseen impact in other areas. 
 * Are tied to specific technical environment presumptions of use and inflexible to other environments.
 * Transformation to any other serialization is treated as an external transformation.
  * Require n-to-n separate transformation specifications and implementations to transform from one serialization to another.

To achieve its targeted objectives UCO has chosen to pursue an ontological approach to its specification and use. An ontology encompasses a representation, formal naming, and definition of the categories, properties, and relations between the concepts, data, and entities that substantiate one, many, or all domains of discourse. [Ontology (information science) - Wikipedia](https://en.wikipedia.org/wiki/Ontology_(information_science)). An ontological approach offers many advantages over alternative approaches:
 
* Ontology models are inherently graph-centric which aligns very well to the nature of relevant information within the targeted scope of UCO.
* The UCO ontology model can be formally specified using a combination of RDFS/OWL/SHACL thus reducing/removing ambiguity in the specification and supporting automated validation of the specification itself and instance content defined conformant to the specification.
	* The W3C Resource Description Framework (RDF) provides a mechanism for expressing structured information in a flexible manner
	* The W3C Resource Description Framework Schema (RDFS) provides a data modeling vocabulary for RDF data enabling the definition of relevant concept classes and properties and any relevant relationships between them
	* The W3C Web Ontology Language (OWL) provides the ability to represent rich and complex knowledge about things, groups of things, and relations between things such as those defined with RDFS. OWL is a computational logic-based language such that knowledge expressed in OWL can be exploited by computer programs, e.g., to verify the consistency of that knowledge or to make implicit knowledge explicit.
	* The W3C Shapes Constraint Language (SHACL) defines the internal structure or shape for a given object node instance for a concept as well as constraints on any properties defined within that object node internal structure.
	   *   SHACL node shapes support the ability to validate appropriate syntactic and semantic constraints for the ontology model.
	   *   SHACL node shapes can be defined as open supporting validation of content that is present while still enabling flexible evolution and extension of content.
	   *   SHACL node shapes support the mapping of RDF-based graphs to labeled property graphs. It should be noted that labeled property graph data representations do not necessarily convert to RDF forms with the full flexibility of native RDF representations.
* Ontology models are more resilient to change as their formal specification provides improved visibility to impact of changes across the model.
* Ontology-based models are more flexible to evolution and change as instance content conformant to varying backward-compatible versions of the ontology model can peacefully coexist in the same graph.
* Formal RDFS/OWL/SHACL ontology models benefit from an extensive RDF ecosystem of standards and tools.
* Ontology-based models within the RDF ecosystem have the formality and flexibility to inherently support both information exchange and analysis.
* Formal RDFS/OWL/SHACL ontology models offer capability to formally define semantics of information and yield analytic value from such semantics such as logical inferencing. The level of semantic formality defined must always be balanced with the other requirements for UCO with a clear bias toward practical flexibility.
* Ontology-based models very flexibly support multiple diverse serializations with many natively supported in a lossless fashion within the RDF ecosystem.
* Formal RDFS/OWL/SHACL ontology models can support semantic-web/linked-data [Linked Data](https://www.w3.org/standards/semanticweb/data) use cases for integrating machine-readable UCO content (and specification) for an unbounded scope of contexts in a "live" dynamic form rather than limited to static serialized exchanges

 An RDF-based ontology approach was chosen over a labeled property graph approach primarily for reasons of informational flexibility and secondarily for ability to support semantic formality and capability.
 
 The scope of UCO is targeted to serve as a middle-level ontology for the cyber domain and its use cases. 
 
 It is NOT intended to target definition of upper ontology-level concepts and is not currently bound to any particular upper ontology for reasons of practical flexibility. This decisions may be revisited in the future if an appropriate upper ontology alignment can be identified that offers the beneficial semantic consistency of an upper ontology with the requisite level of practical flexibility required by the targeted usage scope of UCO.
 
 It is also NOT intended to target definition of detailed concepts specific to particular application-level subdomains (cyber investigation, cyber threat intelligence, risk management, etc.) of the cyber domain. Such application domains may initially be targeted within UCO with definitions within context-specific namespaces but these application domain ontologies built on UCO should be separated out into application domain focused efforts wherever appropriate.
 
 &nbsp;
 
 

# 3 Objects

UCO conceptual content is represented as a graph with nodes and edges.
The nodes in the graph are objects (instances of ontology classes) and the edges are explicitly defined relationships between objects.

It is important to note the difference in granularity between the RDF graph and the UCO domain graph.
In the RDF graph ALL instances of classes and all literal values of properties are objects/nodes and all properties are edges.

Imagine UCO content expressing that a person John Smith is located at 5th Ave in New York City.
An RDF graph of this would look like:
![RDF Graph example](../object-example-rdf-graph.drawio.png "RDF graph example")

In the UCO RDFS/OWL/SHACL ontology, classes are defined for any relevant domain concept as well as for any structured concept characterizing some aspect of a domain concept. Domain concept classes (e.g., File, Action, Identity, Location, Device, etc.) are defined as subclasses of the UcoObject class while structured concept classes characterizing some aspect of a domain concept are considered part of the domain concept and thus are not. A subset of some structured concept classes characterizing some aspect of a domain concept are defined as facet classes as described in #5 below.

All objects in UCO must specify a globally unique identifier (discussed in #4 below) and an assertion of the class type of the object.

Instances of UcoObject subclasses (domain concept classes) are the granularity of discourse in the cyber domain and are thus objects/nodes in the UCO domain graph. Relationships between UcoObject subclasses (either in the form of OWL ObjectProperties or in the form of Relationship object subclasses of UcoObject as described below) are edges in the domain graph. Some relationships between UcoObject subclasses may require further characterization beyond simply expressing an association. These relationships are represented with the Relationship class which itself is a subclass of UcoObject and therefore a node itself in the domain graph. This is further discussed in #6 below.

The domain graph of the above example would look like:
![RDF Graph example](../object-example-domain-graph.drawio.png "Domain graph example")


The UCO domain graph is also the standard granularity that content is typically serialized or queried at as well. If you query for or serialize a domain object you do so as a complete atomic entity including any non-domain objects characterizing the domain object.

A serialization of the example domain graph above would look something like:

```json
{
  "@graph": [
    {
      "@id": "kb:person-952c09ff-5a38-483b-9dcf-6d8f0b27dfac",
      "@type": "identity:Person",
      "core:objectCreatedTime": {
        "@type": "xsd:dateTime",
        "@value": "2017-06-25T12:12:12.12Z"
      },
      "core:name": "John Smith",
      "core:hasFacet": [
        {
          "@id": "kb:5ecfbe78-e7c7-4b23-97fd-5ede9cc32123",
          "@type": "identity:SimpleNameFacet",
          "identity:givenName": "John",
          "identity:familyName": "Smith"
        }
      ]
    },
    {
      "@id": "kb:relationship-cecfbe8c-8357-4105-b448-b491177fedf2",
      "@type": "core:Relationship",
      "core:kindOfRelationship": "located-at",
      "core:source": "kb:person-952c09ff-5a38-483b-9dcf-6d8f0b27dfac",
      "core:target": "kb:location-7044bee0-d5d2-45f3-bb5d-2ced42bfd3f4"
    },
    {
      "@id": "kb:location-7044bee0-d5d2-45f3-bb5d-2ced42bfd3f4",
      "@type": "location:Location",
      "uco-core:hasFacet": [
        {
          "@id": "kb:69e9fe37-f2ee-435b-998f-7b1b0d60a405",
          "@type": "location:SimpleAddressFacet",
          "location:locality": "New York City",
          "location:region": "New York",
          "location:country": "USA",
          "location:street": "5th Ave"
        }
      ]
    }
  ]
}
```

The UCO domain graph can be thought of similarly to a labeled property graph where the nodes are domain objects and the associated properties are a part of those objects. Any RDF graph can be formed losslessly into a labeled property graph but a labeled property graph cannot be formed into an RDF semantic graph with the full flexibility of RDF.

&nbsp;


# 4 Object Identifiers

All objects, both domain and non-domain, must have globally unique identifiers. This means that all objects created, regardless of producer, that are intended to represent different instances of concepts should never have the same id. These globally unique identifiers enable high integrity referencing of objects by other objects as well as by resources external to UCO.


Non-domain objects (non-UcoObject subclasses) exist within the domain graph only as part of other domain objects. In localized RDF content, such objects are often referred to as blank nodes and are by default given simple identifiers that are not unique outside of the local graph they are defined in. Given the fact that UCO is intended to support aggregation and analysis of content across multiple graphs, such non-unique identifiers are inadequate. Such objects can also be given full globally unique identifiers. UCO non-domain objects should leverage this capability to ensure integrity of the aggregated or integrated graph.


As RDF identifiers these object identifiers must be International Resource Identifiers (IRIs). 

An IRI can follow one of several schemes, including URN, HTTP, or HTTPS. In order to ensure global uniqueness and to support use as [Linked Data](https://en.wikipedia.org/wiki/Linked_data), UCO object identifiers should adhere to a formatting pattern consisting of a prefix portion combined with a suffix portion where the prefix portion is an HTTP or HTTPS URI based namespace controlled by the producer of the object and the suffix portion is a combination of an indicator of the object type followed by a [UUID](https://en.wikipedia.org/wiki/Universally_unique_identifier#Versions).

	<namespace><object type>-<UUID>
	
An example of this could be something like:

	http://example.org/kb/location-f1e888a4-7a9d-42d9-af5e-01144ceda3ef

If the producer of the object controlled the namespace domain (example.org) then not only would this ensure global uniqueness but would also support the resolution of the identifier IRI to the object as Linked Data content if the producer desired though there is no requirement that UCO object identifiers be resolvable.

Namespaces in RDF typically end in with the Hash or slash? decision: Should the identifier namespace. end with a # character to represent an HTML within-page anchor point, or with a / character to represent an independent page at the end of an IRI?

UCO specifies that identifier namespaces should end with a slash character, based on the assumption that a UCO content producer might be supporting multiple elementary types of clients: Graph engines, which might make programmatic requests of the IRI; and web browsers, for users wanting to view HTTP renders of the IRI. IRIs that end in hash might cause an expectation that a content producer provide a dump of all object identifiers to a web browser, and rely on the browser to skip into the middle of the page.

By default the UUIDs used in object identifiers should be randomly generated UUIDv4. If a producer desires to support consistent object reproduction without duplication or automatic correlation of semantically identical objects, a UUIDv5 may be used to deterministically and repeatably generate the UUID from semantically-relevant properties of the object.

&nbsp;



# 5 Facets

A facet is a grouping of characteristics unique to a particular aspect of an object. It is a special type of non-domain class/object as it is designed as a general characterizing extension for a domain object. It is defined as a subclass of core:Facet (or one of its context-specific subclasses) and is conveyed as part of a domain object using the ```core:hasFacet``` property. Ideally, facets within a particular context scope (e.g., identity, location, observable, etc.) should be defined as subclasses of a context-specific subclass of ```core:hasFacet``` such as ```identity:IdentityFacet```. Facets are heavily used in context-specific areas such as identity, location and especially for observables. Properties of observable objects (e.g. ```observable:File```) are expressed utilizing facets (e.g., ```observable:FileFacet```, ```observable:ContentDataFacet```, etc.). This serves to enable Duck Typing as described in #5.1 below and flexible characterization of subclasses of observable objects through combinations of facets rather than more complex property inheritance via definition directly on observable object subclasses that proved highly problematic in other information standards efforts such as CybOX.

For instance, a digital photograph is represented as an ```observable:RasterPicture``` subclass of ```observable:ObservableObject``` with the ```observable:FileFacet```, ```observable:ContentDataFacet```, and ```observable:RasterPictureFacet```.

```json
{
            "@id": "kb:raster-picture-f970b1a2-c6f1-4082-a2fb-3e8f4a7913b2",
            "@type": "observable:RasterPicture",
            "core:hasFacet": [
                {
                    "@id": "kb:file-facet-a9a8cd7e-5e09-49c5-8ff4-c2cde2782d4d",
                    "@type": "observable:FileFacet",
                    "observable:fileSystemType": "EXT4",
                    "observable:fileName": "IMG_0123.jpg",
                    "observable:filePath": "/sdcard/IMG_0123.jpg",
                    "observable:extension": "jpg",
                    "observable:sizeInBytes": {
                        "@type": "xsd:long",
                        "@value": 35002
                    }
                },
                {
                    "@id": "kb:content-data-facet-434100af-bbd1-45d5-8926-92b191793f84",
                    "@type": "observable:ContentDataFacet",
                    "observable:byteOrder": "BigEndian",
                    "observable:magicNumber": "/9j/ww==",
                    "observable:mimeType": "image/jpg",
                    "observable:sizeInBytes": {
                        "@type": "xsd:long",
                        "@value": 35000
                    },
                    "observable:dataPayload": "<base 64 encoded data of the file>",
                    "observable:hash": [
                        {
                            "@id": "kb:hash-a63dc64c-a07d-4c23-8013-c84ccd6592d8",
                            "@type": "types:Hash",
                            "types:hashMethod": {"SHA256"},
                            "types:hashValue": {
                                "@type": "xsd:hexBinary",
                                "@value": "6b86b273ff34fce19d6b804eff5a3f5747ada4eaa22f1d49c01e52ddb7875b4b"
                            }
                        }
                    ]
                },
                {
                    "@id": "kb:raster-picture-facet-9763e696-c5b9-4695-bd37-9dd831cc61da",
                    "@type": "observable:RasterPictureFacet",
                    "observable:pictureType": "jpg",
                    "observable:pictureHeight": 12345,
                    "observable:pictureWidth": 12345,
                    "observable:bitsPerPixel": 2
                },
}
```


The generalized approach of facets on domain objects provides value in simple support for use of particular facets across multiple classes/objects, for simplified 3rd party extension of UCO classes/objects, and for clean granularity for adopting profiles or application domain extensions to choose which adornments they want to use.

If particular characterizing properties are directly relevant to the object across most use cases they are typically defined as properties directly on the class/object but where they may be characterizing a particular aspect of an object relevant to some but not all use cases they are typically defined as a facet that can be applied to the class/object when appropriate.

For example, the properties ```core:source``` and ```core:target``` are always relevant to the ```core:Relationship``` class/object in all use cases and are therefore defined as direct properties of ```core:relationship```. On the other hand, differing use cases may characterize a ```location:Location``` as a simple address, or as a set of latitude-longitude coordinates, or as a set of GPS coordinates or any combination thereof. Because of this variation, properties characterizing a location in the form of an address are defined using the ```location:SimpleAddressFacet```, properties characterizing a location in the form of a set of latitude-longitude coordinates are defined using the ```location:LatLongCoordinatesFacet```, and a location in the form of a set of GPS coordinates are defined using the ```location:GPSCoordinatesFacet```.

Facets are intended to be unique when specified on a given object meaning that no single facet class should appear more than once on a single object.


## 5.1 Duck Typing

 The Cyber-investigation Analysis Standard Expression (CASE) is an application domain ontology extension of UCO that is focused on supporting the cyber investigation domain.

CASE uses facets to represent various properties of the associated Observable Objects. CASE uses the programing concept of ‘duck typing’, allowing an object to be enriched with any rational combination of facets. Cyber-investigations can involve various kinds of data, including unexpected combinations of properties in a single object. CASE uses duck typing which allows data to be defined by its inherent characteristics rather than enforcing strict data typing. CASE objects can be assigned any rational combination of facets, such as a file that is an image and a thumbnail. When employing this approach, data types are evaluated with the duck test, allowing data to be represented more truly without imposing a rigid class structure. Simply stated, if it walks like a duck, swims like a duck, quacks like a duck, and looks like a duck, then it probably is a duck. For certain common combinations of facets, it is possible to assign them a higher-level class, such a PDF File or WhatsApp Message. “This flexible approach is favored over using the OWL concept of inheritance to define an object with various properties. Using inheritance requires permitted properties to be formally defined for each object type, which becomes un-wieldy when unexpected combinations of objects are encountered, such as one type of data embedded within another type of data that was not imagined when the ontology was designed.” (Casey et al, 2017)

The example from #5 above could also be expressed with duck typing as a general ```observable:ObservableObject``` adorned with the multiple facets. 

```json
{
            "@id": "kb:observable-object-c5e0e9be-b206-401b-91ed-810de6c79730",
            "@type": "observable:ObservableObject",
            "core:hasFacet": [
                {
                    "@id": "kb:file-facet-5c581af4-dd44-4fe9-9fe7-84498a02c22b",
                    "@type": "observable:FileFacet",
                    "observable:fileSystemType": "EXT4",
                    "observable:fileName": "IMG_0123.jpg",
                    "observable:filePath": "/sdcard/IMG_0123.jpg",
                    "observable:extension": "jpg",
                    "observable:sizeInBytes": {
                        "@type": "xsd:long",
                        "@value": 35002
                    }
                },
                {
                    "@id": "kb:content-data-facet-9bf2df61-2df9-4690-a2d8-6ac14b75ed5b",
                    "@type": "observable:ContentDataFacet",
                    "observable:byteOrder": "BigEndian",
                    "observable:magicNumber": "/9j/ww==",
                    "observable:mimeType": "image/jpg",
                    "observable:sizeInBytes": {
                        "@type": "xsd:long",
                        "@value": 35000
                    },
                    "observable:dataPayload": "<base 64 encoded data of the file>",
                    "observable:hash": [
                        {
                            "@id": "kb:hash-1c49e84b-fd98-48a9-b384-7f937f7f7c2b",
                            "@type": "types:Hash",
                            "types:hashMethod": {"SHA256"},
                            "types:hashValue": {
                                "@type": "xsd:hexBinary",
                                "@value": "6b86b273ff34fce19d6b804eff5a3f5747ada4eaa22f1d49c01e52ddb7875b4b"
                            }
                        }
                    ]
                },
                {
                    "@id": "kb:raster-picture-facet-bf5ef8f5-49b2-4c65-9b59-4965dd109532",
                    "@type": "observable:RasterPictureFacet",
                    "observable:pictureType": "jpg",
                    "observable:pictureHeight": 12345,
                    "observable:pictureWidth": 12345,
                    "observable:bitsPerPixel": 2
                },
}
```

UCO utilizes a facet-based approach for characterizing observable objects to support both generic duck typing as well as type specific object specification without biasing toward one over the other.

&nbsp;


# 6 Relationships

Relationships are asserted associations between objects. The are the edges in the domain graph between object nodes.
In the simplest form such relationships can be expressed in ontologies such as UCO as Object Properties where the relationship is expressed as a property of one object, the identifier of the property is the type of relationship and the value of the property is the other object.

This works well when the relationship itself is an inherent part of one object and requires no further characterization.
For example, consider an email message and the relationship to an email address that it is addressed to. This relationship is inherent to the email message (it does not really have meaning outside of that email message) and it requires no further characterization. As such it can be expressed with a simple ```observable:to``` object property on the ```observable:EmailMessage``` object.

&nbsp;


![ObjectProperty Relationship example](../relationship-example-simple-object-property.drawio.png "ObjectProperty Relationship example")

&nbsp;

Such object properties are simple to express and simple to query or navigate in the overall graph.

Unfortunately, not all relationships are so simple. 

Many relationships may be relevant outside of either of the related objects and many relationships require further characterization beyond a simple association. 

An asserted relationship that has relevance outside of either of the related objects is inherently a conceptual object itself with a need for unique identification and the ability to be referenced by other objects or even be part of a separate asserted relationship between it and other objects (relationships about relationships). Unique identification is also required to support the ability to assert multiple separate instances of the same type of relationship between the same objects asserted by different parties or at different times or with differing additional characterizing adornment.

One of the most commonly needed relationship characterizations beyond basic metadata (who created it, when it was created, when it was modified, etc) is to support temporality of the asserted relationship. In other words, asserting when the relationship is asserted to be true. In UCO this would be expressed with the ```core:startTime``` and ```core:endTime``` properties. Consider for example, a relationship between a Domain Name and an IP Address such that the Domain Name "Resolved_To" the IP Address at some specific time. Another example of such relationship characterization would be one object "Contained_Within" another object and the need to express the location of the contained object within the containing object. The location is not a property of either the contained or the containing object but rather of the "Contained_Within" relationship between them.

Simple object properties do not have the capability to support unique identification or additional adornment of relationships. Basic internal RDF reification that treats the object property as a metagraph allowing additional property adornment partly supports the additional adornment requirement but is fairly deep in the weeds of RDF and does not support unique identification.

UCO takes an alternate approach of external reification to express relationships in a way that supports core elements of a relationship (```core:source``` (the originating object of the relationship), ```core:target``` (the target object of the relationship), and ```core:kindOfRelationship``` (the kind of relationship from the source to the target)), the unique identification requirement and the additional adornment requirement. It does this with with a domain object (subclass of ```core:UcoObject```) class called ```core:Relationship```.

A simple graph example of this could look something like:

&nbsp;


![Relationship object example](../relationship-example-simple-relationship-object.drawio.png "Relationship object example")

&nbsp;

Another example of a Relationship object but as JSON-LD could look something like:

```json
{
	  "@id": "kb:device-linkage-a1dbff0e-974b-4295-b035-e1bc3271945d",
	  "@type": "core:Relationship",
	  "core:source": ["kb:device1-24d20c80-f035-40ae-88dd-fc66f70180f6"],
	  "core:target": "kb:device2-eee670c6-01d4-4e42-bb6b-ebeca149b168",
	  "core:kindOfRelationship": "Referenced_Within",
	  "core:isDirectional": true
}
```
&nbsp;

And another graph example showing the referencing of a Relationship object as a unique object could look something like:

![Reference to Relationship object example](../relationship-example-reference-to-relationship-object.drawio.png "Reference to Relationship object example")

Another fundamental question to consider is regarding the appropriate cardinality of either end of such a Relationship object. The most simple scenario is a relationship from one object to one other object. This scenario keeps things nice and clean and unambiguous. However, there are some use cases that may desire to specify more than one object on either end of the relationship. There are really four potential variants: 1-to-1, n-to-1, 1-to-n, and n-to-n. One motivation for desiring a cardinality greater than one on either end of the relationship is to act as a compact way to express multiple relationships that share a ```core:kindOfRelationship``` and either a common ```core:source``` or ```core:target```. Another motivation for desiring a cardinality greater than one on either end of the relationship is to specify a relationship to or from a set of objects as an aggregated whole. Both or these are valid and useful motivations but open cardinality on either or both ends of a relationship brings significant potential complexity and the inability to distinguish which of the motivations was in play for a given relationship without the additional complexity of further contextual properties. The current decision within UCO is that limiting to only 1-to-1 is inadequate but opening to n-to-n is too complex and so a compromise of n-to-1 is currently defined. This is not a decision set in stone and is open to future potential changes due to identified needs.


Relationship objects are more complex than a simple object property but they support a broad diversity of use cases that object properties do not. Each option has its own strengths and weaknesses. Object properties are simple to express and simple to query or navigate in the overall graph yet do not support full relationship requirements and require design-time definition as properties within the ontology. Relationship objects are more complex to express and to query in the graph but offer significantly more capability for more involved required use cases and support more flexible ad-hoc and user-level expression of kinds of relationships (through a string-based ```core:kindOfRelationship``` property) that is necessary for the broad scope of UCO targeted use. Vocabularies of common kinds of relationships are useful for improved consistency and interoperability but such vocabularies whether defined as flexible strings or explicitly rigid object properties can never be presumed to be complete given the scope and evolving nature of the cyber domain (see #8 below for discussion of the fundamental requirement for user-level extensibility for vocabularies including for kinds of relationships).

Given the tradeoffs with the two options, each time a kind of relationship is desired to be expressed a choice must be made on which option to choose. There really is not an absolute black and white heuristic for this that applies in all situations but the general rule of thumb recommended by UCO is that if a relationship is inherent and immutable to its source object then it is most appropriate to utilize the simple object property option. Otherwise, it is more appropriate to utilize a Relationship object.

&nbsp;


# 7 Content Validation

UCO instance content validation supported by the inclusion of [W3C Shapes Constraint Language (SHACL)](https://www.w3.org/TR/shacl/) shapes integrated within the UCO RDF/OWL ontology specification. Each class in the RDF/OWL specification has a defined SHACL node shape with appropriate SHACL property shapes. Each property shape can assert constraints for that property on that class including type or class, cardinality, value constraints, etc. Each SHACL node shape provides a basis for syntactic and semantic validation of instance object content based on its associated/targeted class.

Example:

	Method of travel = vehicle (constraint)

	In a json schema the value in the method of travel must = vehicle

	With SHACL you can validate on vehicle, car, or airplane because they are all semantically vehicles

For a concrete UCO example, the nodeshape for ```core:ConfidenceFacet``` below specifies that any instance object of the ```core:ConfidenceFacet``` class must have exactly one instance of the ```core:confidence``` property of type ```xsd:nonNegativeInteger```:

```
core:ConfidenceFacet
	a
		owl:Class ,
		sh:NodeShape
		;
	rdfs:subClassOf core:Facet ;
	rdfs:label "ConfidenceFacet"@en ;
	rdfs:comment "A confidence facet is a grouping of characteristics unique to an asserted level of certainty in the accuracy of some information."@en ;
	sh:property [
		sh:datatype xsd:nonNegativeInteger ;
		sh:maxCount "1"^^xsd:integer ;
		sh:minCount "1"^^xsd:integer ;
		sh:nodeKind sh:Literal ;
		sh:path core:confidence ;
	] ;
	sh:targetClass core:ConfidenceFacet ;
	.
```

Actual validation execution against a graph of UCO content is performed using a SHACL validation engine. The default suggested SHACL validation engine for UCO is [pySHACL](https://github.com/RDFLib/pySHACL).

&nbsp;


# 8 Ontological Properties, Values and Vocabularies

### Ontology properties characterize a particular instance of a concept (individual) either by asserting relationships to other instances of a concept (individual) or by expressing direct attributes of the instance of a concept (individual)

* Object properties (discussed in section #6 above) assert a relationship between one instance of a concept (individual) and another instance of a concept (individual)
	* They link individuals to individuals
* Datatype properties characterize attributes of a particular instance of a concept
		* They link individuals to data values.
	* Reducing the values of characterizing attributes to individuals adds semantic rigor to the ontology but not all data value attributes of an individual are appropriate to define as individuals themselves. Doing so in many cases may add so much rigor that the underlying ontology loses its practical utility.

### UCO foundational principles relevant to topic

There are several foundational principles of UCO (defined in the Cyber Domain Ontology Technical Charter and restated in section 1 of this document above) that are relevant to design decisions regarding ontology properties and the specification and use of vocabularies.

* Required focus on generalized support
	* (Technical Charter 1.b.ii and #2 in section 1 of this document)
		* UCO concept semantics, structure and constraints at both a design and implementation level must always support broad applicability across the cyber domain and not be biased to any particular one or more application domains. Maintaining broad applicability may involve compromises from optimal solutions for any single application domain in order to support the strategic objective for the overall ecosystem initiative.
* Inherency of incomplete understanding and conceptual coverage requiring both design-level and user-level practical extensibility and flexibility
	* (Technical Charter 1.b.iii and #3 in section 1 of this document)
		* Due to the inherency of incomplete understanding and conceptual coverage at any point in time, the inexorable evolution of domain needs over time, and the uniquely specialized needs of adopters, UCO must support practical extensibility at both an explicit design level and an implicit user level. 
			* At an explicit design-level, this would include the potential for adopters to define relevant class, property, datatype or vocabulary extensions to UCO to support their needs as long as they are not in conflict with existing UCO definitions and structures. If relevant to other adopters and multiple application domains these extensions may be considered for future inclusion in UCO. 
			* At an implicit user-level, this would include classes asserting open shapes (to allow custom properties to be added at time of use) and defined vocabularies to be open to provide suggested values for consistent normalization but also allow values outside the predefined set. Validation should flag such customizations as warnings but not as errors.
* Balance between top-down and bottom-up ontological rigor with clear decisive bias toward practicality
	* (Technical Charter 1.b.iv and #4 in section 1 of this document)
		* UCO must seek a balance between top-down and bottom-up ontological rigor with a clear decisive bias toward practicality and flexibility.

### Targeted stakeholders relevant to the topic

| CDO Stakeholders | Objective | Focus | Level of domain knowledge | Level of ontology knowledge | Primary interface with Ontology |
| ---------------- | --------- | ----- | ------------------------- | --------------------------- | ------------------------------- |
| UCO ontologists | Specify general ontology foundation to support consistency of data specification and use across cyber application domains | Ontology across domains | Moderate | High | RDF/OWL/SHACL |
| Application domain (e.g., CASE) ontologists | Specify application domain specific ontology extension of UCO to support application domain adopters | Domain then Ontology | High | High | RDF/OWL/SHACL |
| CDO Adopters | Leverage defined ontology for consistency and interoperability in support of their application domain mission | Domain using defined ontology | High | Low | Human documentation autogenerated from RDF/OWL/SHACL |
| * Application tools | Leverage defined ontology to provide application domain mission capabilities to Users | Support domain users using serialization of ontology | High | Low | Human documentation autogenerated from RDF/OWL/SHACL |
| * Analysis tools | Leverage defined ontology to provide application domain mission capabilities to Users | Support domain users using deserialization of ontology | High | Low | Human documentation autogenerated from RDF/OWL/SHACL |
| CDO Users | Carry out domain mission as simply as possible | Domain | High | Low to none | Application tools and analytics |

 

### One very common type of datatype property value in ontologies is textual (string-based) properties. Textual (string-based) properties provide a human language characterization of a particular attribute or aspect of an instance of a concept (individual).

Ontology textual (string-based) properties typically have one of three closure designs all of which are relevant to and required by UCO: closed, fully open, and open with suggested valid values (vocabularies).

### Closed

The intent of this design is to support specification of relevant property values where the valid set of potential values is explicitly bound and defined by some external authoritative source. These can be thought of as closed value enumerations rather than open vocabularies. A property bound to such an enumeration may only take a value explicitly in the enumeration and any other value is inherently invalid. Such properties are relatively rare compared to the other two closure designs.

* UCO supports this design using restricted Datatypes using owl:oneOf and rdf:List to assert that ONLY values from the defined value space are valid.
* An example of this design is observable:WindowsServiceStartType.

					observable:WindowsServiceStartType
						a rdfs:Datatype ;
						owl:equivalentClass [
							a rdfs:Datatype ;
							owl:oneOf [
								a rdf:List ;
								rdf:first "service_auto_start" ;
								rdf:rest [
									a rdf:List ;
									rdf:first "service_boot_start" ;
									rdf:rest [
										a rdf:List ;
										rdf:first "service_demand_start" ;
										rdf:rest [
											a rdf:List ;
											rdf:first "service_disabled" ;
											rdf:rest [
												a rdf:List ;
												rdf:first "service_system_alert" ;
												rdf:rest rdf:nil ;
											] ;
										] ;
									] ;
								] ;
							] ;
						] ;
						.


Validation

* UCO utilizes SHACL property shape constraints asserting the datatype for the property aligned to its appropriate enumeration datatype and its value in that datatype.

### Fully open

The intent of this design is to give the adopter the ability to define any value they want. Full open property values require a range property definition if possible.

UCO supports this design using a range of xsd:string.

An example of this design is the core:description property

					core:description 
						a owl:DatatypeProperty ; 
						rdfs:label "description"@en ; 
						rdfs:comment "A description of a particular concept characterization."@en ; 
						rdfs:range xsd:string ;
.

Validation

 * UCO utilizes SHACL property shape constraints asserting the datatype for the property as xsd:string and no further constraints on value.

### Open with suggested valid values (Vocabularies)

The intent of this design is to support a user specifying a relevant property value while providing hints or guiderails for the adopter through the specification of an open vocabulary of common values. Where possible and appropriate one of the values from the vocabulary should be used but where it is not possible or appropriate any other string may be used. Utilizing explicitly identified values from the vocabulary yields improved consistency and interoperability. The open nature of the vocabulary allowing non-defined values to be used when the vocabulary does not provide an appropriate value ensures that the ontology remains practically useful given the reality of the inherency of incomplete understanding and conceptual coverage at any point in time, the inexorable evolution of domain needs over time, and the uniquely specialized needs of adopters outlined in UCO foundational principle (Technical Charter 1.b.iii and #3 in section 1 of this document).

The UCO ontology never presumes that vocabularies are ever complete. We do not prescribe the sole use of a closed vocabulary as it is not consistent with the natural maturation of cyber domain discourse. Our experience tells us that the sole use of a closed vocabulary limits the long-term usefulness of a semantic model as new concepts are developed in the cyber domain discourse. Considering that the cyber domain concepts are still evolving rapidly, we designed UCO to be as flexible for adopters as possible where we provide coverage of well known concepts, where we have adopted well established concepts from other communities, and where the adopter can provide their own vocabulary for unsupported concepts.

We want to preserve the ability of UCO adopters to extend our design by using new ad-hoc values and by adding new property vocabularies with definitions. We realize that the UCO ontology is not able to pre-identify every concept and semantic understanding across the cyber domain.


UCO supports this open with suggested valid values (vocabularies) design using explicitly defined datatype restrictions on xsd:string specifying sets of valid string values and through specification of the property range as an owl:unionOf xsd:string and the vocabulary datatype.

**The following considerations are central to this design approach in UCO**

* Vocabularies are intended to be hints and guiderails for improved consistency. They are not intended to be preventatively restrictive.
	* Vocabularies are inherently presumed to be incomplete and in-progress in accordance with UCO foundational principle (Technical Charter 1.b.iii and #3 in section 1 of this document).
		* At any point in time, a given vocabulary is unlikely to be fully complete for the general state of the practice.
		* The cyber domain is rapidly evolving and as such the leading edge of state of the practice will also be ahead of any formal vocabulary definition within the ontology.
		* There will be specific subdomain communities within the relevant scope of an open vocabulary property that will require the use of values specialized to their particular context and not necessary relevant for the broader general scope of a vocabulary defined in the ontology.
	* Vocabularies are typically tied to some semantic scope for a given property(ies).
		* There may be a single broad vocabulary for the property or multiple vocabularies for varying uses of the property.
	* Values should be added to vocabularies where they are believed to have common use relevant to the property.
	* Just because a value does not currently exist in a vocabulary does not mean you cannot use it for a string property.
		* This is especially true for broadly applicable properties such as core:kindOfRelationship and action:Action.core:name
	* Vocabulary extension typically follows a common evolution flow
		* Point in time value-based specification of custom values outside of current vocabulary by user
		* Formal addition of new custom values to defined vocabulary by adopter as localized extension
		* Formal addition of new custom value to vocabulary by UCO or application domain ontology as global extension
			* Adopters who have use cases that present new vocabulary concepts are asked to submit those concepts as a change proposal to the UCO Ontology Committee. The Committee reviews new vocabulary, defines the common semantic understanding, and puts the vocabulary proposal through the review process for possible addition. UCO tries to express the semantics of concepts for each of the community approved use cases in a flexible way via a bottom-up-middle ontology engineering approach. UCO intends to be real-world example driven and not try to apply top-down design approaches based on ontological rigor or advanced capabilities independent of specific real-world need or at the expense of real-world practicality.

**An example of this design is action:actionStatus (vocabulary:ActionStatusTypeVocab)**

					action:actionStatus
						a owl:DatatypeProperty ;
						rdfs:label "actionStatus"@en ;
						rdfs:comment "The current state of the action."@en ;
						rdfs:range vocabulary:ActionStatusTypeVocab ;
						.
					
					vocabulary:ActionStatusTypeVocab
						a rdfs:Datatype ;
						rdfs:subClassOf rdfs:Resource ;
						rdfs:label "Action Status Type Vocabulary"@en-US ;
						rdfs:comment "Defines an open-vocabulary of action status types."@en-US ;
						owl:oneOf (
							"Complete/Finish"^^vocabulary:ActionStatusTypeVocab
							"Error"^^vocabulary:ActionStatusTypeVocab
							"Fail"^^vocabulary:ActionStatusTypeVocab
							"Ongoing"^^vocabulary:ActionStatusTypeVocab
							"Pending"^^vocabulary:ActionStatusTypeVocab
							"Success"^^vocabulary:ActionStatusTypeVocab
							"Unknown"^^vocabulary:ActionStatusTypeVocab
						) ;
						.


**Properties utilizing vocabularies are typically one of two cases**

* Properties conveying some sort of classification concept
	* An example of this would be observable:deviceType
	* Taxonometric structures of "type" for a concept (class) such as observable:deviceType are not adequately or correctly modeled solely as simple property strings or a simple SKOS taxonomy.
	* Such taxonomies are more effectively and correctly modeled using subclass relationships within the UcoObject class taxonomy
		* For example, the observable:deviceType property on the observable:DeviceFacet class is very intentionally meant to be a mechanism to enable general assertion of a type of device not currently defined in the ontology.
		* A device type taxonomy should be specified as a subclass hierarchy under the Device class which is a subclass of observable:ObservableObject. This taxonomy already exists but is currently very limited. Each subclass is this hierarchy would also then assert a SHACL property shape on the string-based field (observable:deviceType) on that class constraining its value to the vocabulary value corresponding to the particular subclass.
		* This approach provides:
			* Clear definitions for terms
			* Inferencing on hierarchy between terms
			* Ability to define/express term-specific properties on individual subclasses consistently with the mechanism used for the overall ontology
			* Avoids confusion and conflation between an SKOS taxonomy and the formal UCO class taxonomy
			* General extensibility for device types not defined in the observable:Device subclass taxonomy
* Properties conveying some non-classification concept value
	* An example of this would be action:actionStatus (vocabulary:ActionStatusTypeVocab)
	* The large majority of vocabularies (e.g. vocabulary:ActionArgumentNameVocab, vocabulary:ActionTypeVocab, etc) are not hierarchical in nature and are not "class" in nature and as such:
		* Do not benefit from hierarchy inferencing
		* Would not make sense to force into an artificial hierarchy
		* Would lead to creation of impractical abstraction values that would likely cause confusion in properties utilizing such vocabularies
		* Would not simply adhere to a mutually-exclusive taxonomy. Many would end up being graphs with multiple path derivation

**Special Case: core:kindOfRelationship and associated vocabularies**

* core:kindOfRelationship is a foundational property for UCO and serves to capture the vast range of potential relationships between the full range of UCO objects and as such requires careful handling for associating any vocabularies of values.
	* Vocabularies should never be asserted on the general core:kindOfRelationship on core:Relationship as it is the general mechanism for asserting all kinds of relationships. Making such constraining assertions would almost certainly generate massive amounts of validation noise for most UCO uses to the point of likely making validation impractical for use.
	* If particular vocabularies of relationship types are desired  for particular contexts then first a subclass of core:Relationship should be defined for that context and then the desired contextual vocabulary can be associated with core:kindOfRelationship on that subclass. Using SHACL this approach requires that no specific datatype (xsd:string) be asserted in property shapes for core:kindOfRelationship on core:Relationship to avoid conflicting type constraints. This gives the value of contextual alignment without overly restricting uses outside of that context.
		* For example, an observable:ObservableObjectRelationship class could be defined as a subclass of observable:ObservableRelationship and then the vocabulary:ObservableObjectRelationshipVocab could be associated with the core:kindOfRelationship property on observable:ObservableObjectRelationship using a SHACL property shape.
		* Similarly, an action:ActionRelationship class could be defined as a subclass of core:Relationship and then the vocabulary:ActionRelationshipTypeVocab could be associated with the core:kindOfRelationship property on action:ActionRelationship using a SHACL property shape.

**Validation**

* UCO utilizes SHACL property shape constraints asserting that either the datatype for the property is the associated vocabulary datatype and the value of the property is in the vocabulary datatype range OR the datatype for the property is xsd:string and the value of the property is NOT in the vocabulary datatype range. In the latter case the validator will generate an info message informing that a value outside the vocabulary was used.

**Evaluation of current approach**

* Pros
	* Does support specification of suggested valid values for textual (string-based) properties in the form of vocabularies
	* Does support both design-level and user-level practical extensibility
	* Does support validation
* Cons
	* Does not provide explicit definition of the vocabulary terms
	* Does not support implicit semantic inferencing
* Conclusion
	* Current approach could benefit from ability to provide explicit definition of the vocabulary terms but meets requirements for UCO and adheres to foundational principles.

**Potential alternative design approaches**

* Closed enumerations for all vocabularies
	* This approach would very clearly block practical use and evolution of the vocabularies and violates UCO foundational principle (Technical Charter 1.b.iii and #3 in section 1 of this document).
* Define vocabulary entries as explicit individuals using something like the Simple Knowledge Organization System (SKOS)
	* SKOS is intended for explicitly specifying knowledge organization systems such as thesauri, taxonomies, classification schemes and subject heading systems by identifying and relating conceptual resources (concepts, not necessarily attribute values).
		* SKOS can provide significant value in some situations but is not intended to solve all problems.
		* SKOS does not effectively replace OWL datatype values nor does it replace OWL class hierarchies.
		* Some players have proposed potentially replacing all UCO vocabularies with explicit SKOS concept taxonomies of individuals
	* Evaluation of alternative approach
		* Advantages of SKOS approach in relation to vocabularies
			* Can explicitly specify definitions of vocabulary terms
			* Can explicitly specify hierarchy of vocabulary terms
			* Can support direct inferencing of hierarchy between vocabulary terms
		* Disadvantages of SKOS approach in relation to vocabularies
			* End users cannot convey custom values without requiring ontological design knowledge,  full understanding of existing hierarchy, and a way to explicitly define and convey design-level ontology changes to specify formal structured definitions.
				* This violates UCO foundational principle (Technical Charter 1.b.iii and #3 in section 1 of this document).
				* It also breaks down the primary entry point for the vocabulary extension typical evolution flow leading to slower and less effective evolution of vocabularies to support real-world usage contexts
			* Any content shared externally leveraging custom values would require that any custom design-level SKOS conceptual concepts be also shared otherwise any consumers of that content would have properties with IRIs that they could not resolve. This would lead to non-useful content and also would not expose custom values to external parties such that they may consider their value and whether to use them. String-based values are inherently shareable and easily considered by any consumers.
			* Size and complexity of ontology becomes significantly larger
				* This is likely to significantly affect inertia of adoption.
				* This is likely to significantly increase the effort to effectively manage and mature the ontology
			* For almost any concept, such taxonomies will never be complete and would likely not have a common consensus of "correct" across all subdomains and/or use perspectives. Textual vocabulary values inherently imply less perceived rigor than formal taxonomies and thereby mitigate somewhat misinterpretations of perceived completeness, rigor and consensus.
			* There is significant risk of homonymic overlap between terms in differing vocabularies focused on differing contexts.
				* Some terms can have many different meanings depending on context
				* Examples
					* "Lead" as an action verb in an action name vocabulary
					* "Lead" as a role in a role vocabulary
					* "Lead" as a material in a physical material vocabulary
					* "Lead" as a clue in an investigation
				* To utilize a formal SKOS approach would require some mechanism to help disambiguate such overlapping terms without unduly affecting them from their native domain use.
		* The vast majority of data solutions existing today are not based in formal semantic rigor and effectively utilize string-based values for concept property characterization. With this approach any user who understands the serialization can express what they need to without requiring any formal design-level knowledge.
		* Formal semantic ontology based approaches, while promising and rapidly evolving, are still relatively rare and most of them that are not tightly focused on one very specific domain or usage context do not fully rely solely on defined individuals. An individuals-focused approach yields value in ease of semantic inferencing but also brings with it significant prohibitive constraints on flexibility and extensibility at a user practicality level, especially for UCO as an intentionally broad middle ontology in the very diverse and rapidly evolving cyber domain.
			* This IS an ontology problem.
			* It is NOT simply an application problem.
			* An application is implemented conformant to a given release version of the ontology including its vocabulary definitions. An application can provide an interface that lets a user specify a custom string term but that term cannot be expressed, conveyed, persisted or exchanged in the underlying data model (ontology) without formally extending the ontology with design-level ontological formal definition of a new individual appropriately placed within the existing hierarchy. Adhering to UCO foundational principle (Technical Charter 1.b.iii and #3 in section 1 of this document) for user-level extensibility cannot be effectively addressed solely at the application level. It must be addressed at the ontology design level.
	* Determination/Conclusion
		* A purely individuals-based approach to vocabularies for textual (string-based) properties is not effective or practical for the targeted usage for UCO and violates UCO foundational principles (Technical Charter 1.b.iii.1 & Technical Charter 1.b.iii.2; #3 in section 1 of this document)
		* There is a potential for a hybrid approach using SKOS to define (and relate where appropriate) terms but still use string-based properties for practical extensibility. The preferred label on the SKOS concepts could also be defined to align to the string values as defined in current vocabulary definitions. Additional OWL axioms could be defined to formalize this alignment and support inferencing.
			* This would not avoid the size and complexity concerns or the practicality concerns for community management effort or consensus. It would also not support first order ObjectProperty based inferencing.
			* It would however yield the value of explicitly defining known terms and specifying known hierarchy and would maintain the required flexibility and extensibility for user-defined custom values while still supporting a slightly more complex inferencing.
			* Addressing the homonymic overlap risk could partially but not totally be mitigated by utilizing an approach where there is a root of an SKOS vocabulary taxonomy for each vocabulary context
			* If such a hybrid approach were to be pursued, it is highly recommended that all SKOS content and related axioms are defined and stored in a namespace separate from the vocabularies. This would simplify understandability for adopters and would enable adopters wishing to focus on a simple string-based approach to do so and adopters wishing to focus on a more complex individual-based approach to do so.




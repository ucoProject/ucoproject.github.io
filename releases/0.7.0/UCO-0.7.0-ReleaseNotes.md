Ontology Committee : UCO Version 0.7.0 Release Notes
====================================================

### Focus:

UCO 0.7.0 is primarily focused on the conversion of UCO ontologies to leverage the Shapes Constraint Language (SHACL) rather than domain assertions and owl property restrictions to define class shapes. In addition, it added a continuous integration (CI) method for testing and verifying the ontology and it corrects several minor issues and bugs.

#### Focus Exceptions:

* * *

### Change Proposals Addressed in this Release

*   \[CP-5\] [Refactor and improve contacts](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/329089025/UCO+CP-5+Refactor+and+improve+contacts)
    
*   \[CP-23\] [Convert current property restrictions and domain assertions to SHACL shapes](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/984678401/UCO+CP-23+Convert+current+property+restrictions+and+domain+assertions+to+SHACL+shapes)
    
*   \[CP-38\] [Change NTFSFileSystemFacet to NTFSFileFacet](https://unifiedcyberontology.atlassian.net/wiki/pages/resumedraft.action?draftId=1292369921)
    
*   \[CP-39\] [Establish unit tests and Continuous Integration for ontology repository](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1292632067/UCO+CP-39+Establish+unit+tests+and+Continuous+Integration+for+ontology+repository)
    
*   \[CP-46\] [Change range of observable:partitionID from xsd:integer to xsd:string within DiskPartitionFacet](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1431797761/UCO+CP-46+Change+range+of+observable%3ApartitionID+from+xsd%3Ainteger+to+xsd%3Astring+within+DiskPartitionFacet)
    
*   \[CP-48\] [Correct RDFS concept IRI typos introduced in UCO 0.6.0](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1433763841/UCO+CP-48+Correct+RDFS+concept+IRI+typos+introduced+in+UCO+0.6.0)
    
*   \[CP-52\] [Treat "nameserver" as two-word term](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1539538945)
    
*   \[CP-53\] [Fix URI typo in core:ExternalReference and observable:OnlineServiceFacet](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1608122369/UCO+CP-53+Fix+URI+typo+in+core%3AExternalReference+and+observable%3AOnlineServiceFacet)
    
*   \[CP-54\] [Add clarifying comment to use of observable:sizeInBytes on observable:FileFacet](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1620574209/UCO+CP-54+Add+clarifying+comment+to+use+of+observable%3AsizeInBytes+on+observable%3AFileFacet)
    
*   \[CP-55\] [Change definition of core:specVersion to include subontologies](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1620803608/UCO+CP-55+Change+definition+of+core%3AspecVersion+to+include+subontologies)
    
*   \[CP-57\] [Change name of identity:CountriesOfResidence to conform to naming standard](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1620836376/UCO+CP-57+Change+name+of+identity%3ACountriesOfResidence+to+conform+to+naming+standard)
    
*   \[CP-58\] [Modify range of observable:clockSetting from xsd:string to xsd:dateTime](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1620836389/UCO+CP-58+Modify+range+of+observable%3AclockSetting+from+xsd%3Astring+to+xsd%3AdateTime)
    
*   \[CP-59\] [Modify cardinality of observable:hasChanged on observable:ObservableObject from 1 to 0..1](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1620836402/UCO+CP-59+Modify+cardinality+of+observable%3AhasChanged+on+observable%3AObservableObject+from+1+to+0..1)
    
*   \[CP-60\] [Remove duplicate definitions from some properties](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1620836435/UCO+CP-60+Remove+duplicate+definitions+from+some+properties)
    
*   \[CP-62\] [Correct misuse of identity:Identity and marking:MarkingDefinition within the core namespace](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1647673350/UCO+CP-62+Correct+misuse+of+identity%3AIdentity+and+marking%3AMarkingDefinition+within+the+core+namespace)
    
*   \[CP-63\] [Remove "minimum" restriction from core:id](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1707474947)
    
*   \[CP-64\] [Remove observable:faxNumber](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1730641923/UCO+CP-64+Remove+observable%3AfaxNumber)
    
*   \[CP-65\] [Fix typo in observable:profilelanguage](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1731657729/UCO+CP-65+Fix+typo+in+observable%3Aprofilelanguage)
    
*   \[CP-66\] [Remove core:role](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1731854350/UCO+CP-66+Remove+core%3Arole)
    
*   \[CP-67\] [observable:region\_end\_address is a typo within obervable-da.ttl](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1732050965)
    
*   \[CP-69\] [Fix several typos within observable.ttl prior to SHACL release](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1832845313/UCO+CP-69+Fix+several+typos+within+observable.ttl+prior+to+SHACL+release)
    
*   \[CP-71\] [Set ontology Continuous Integration to use Java 8](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1847394305/UCO+CP-71+Set+ontology+Continuous+Integration+to+use+Java+8)
    
*   \[CP-72\] [Remove xsd:string values from sh:datatype on property shapes for observable:mockLocationsAllowed and observable:phoneActivationTime](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1870364673/UCO+CP-72%3A+Remove+xsd%3Astring+values+from+sh%3Adatatype+on+property+shapes+for+observable%3AmockLocationsAllowed+and+observable%3AphoneActivationTime)
    
*   \[CP-73\] [observable:status property is being used in multiple classes with multiple datatypes](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1870626819/UCO+CP-73%3A+observable%3Astatus+property+is+being+used+in+multiple+classes+with+multiple+datatypes)
    
*   \[CP-74\] [observable:priority is used across multiple context with multiple datatypes](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1871020033/UCO+CP-74%3A+observable%3Apriority+is+used+across+multiple+context+with+multiple+datatypes)
    
*   \[CP-75\] [Remove xsd:float from observable:WindowsPESection](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1870725131/UCO+CP-75%3A+Remove+xsd%3Afloat+from+observable%3AWindowsPESection)
    
*   \[CP-76\] [Range of observable:owner should only be core:UcoObject](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1870364710/UCO+CP-76%3A+Range+of+observable%3Aowner+should+only+be+core%3AUcoObject)
    
*   \[CP-77\] [types:entry has multiple contexts with multiple datatypes](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1870725146/UCO+CP-77%3A+types%3Aentry+has+multiple+contexts+with+multiple+datatypes)
    
*   \[CP-78\] [observable:listedCount was not created during the implementation of CP-7](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1872199683/UCO+CP-78%3A+observable%3AlistedCount+was+not+created+during+the+implementation+of+CP-7)
    
*   \[CP-79\] [Add test for sh:datatype count validity](https://unifiedcyberontology.atlassian.net/wiki/spaces/OC/pages/1875116033)
    

* * *

### Changes (these are changes to ontologies, classes or properties in the preexisting ontology)

#### Development Changes (These are changes to ontology development practice, and are not necessarily changes to ontology data.)

*   UCO now runs a Continuous Integration test suite as part of its ontology pull request review \[CP-39\]
    
*   Continuous Integration tests now include SHACL-specific tests:
    
    *   Validation of passing and expected-failing example data \[CP-23\]
        
    *   Review of property-shape compatibility between subclasses and superclasses \[CP-23\]
        
    *   Review of property shape datatype constraint validity \[CP-79\]
        

#### Breaking Changes (These are changes to ontologies, classes or properties in the preexisting ontology that make the new release non-backward-compatible.)

*   all namespaces: converted the entire UCO ontology to SHACL \[CP-23\]
    
*   all namespaces: UCO's SHACL conversion converted OWL qualified cardinality statements (e.g. owl:maxQualifiedCardinality) to unqualified SHACL minima and maxima (e.g. sh:max). \[CP-23\]
    
*   uco-identity: modified the subclass of identity:Identity from core:UcoObject to core:IdentityAbstraction \[CP-62\]
    
*   uco-marking: modified the subclass of marking:MarkingDefinition from core:UcoObject to core:MarkingDefinitionAbstraction \[CP-62\]
    
*   uco-observable: modified observable:nameserver to be observable:nameServer \[CP-52\]
    
*   uco-observable: modified observable:NTFSFileSystemFacet to be observable:NTFSFileFacet \[CP-38\]
    
    *   modified the rdfs:label and rdfs:comment to match the change
        
*   uco-identity: renamed identity:CountriesOfResidenceFacet to identity:CountryOfResidenceFacet \[CP-57\]
    
    *   modified the rdfs:label and rdfs:comment to match the change
        
*   uco-observable: renamed observable:region\_end\_address to observable:regionEndAddress (within the obsolete observable-da.ttl file) \[CP-67\]
    
*   uco-observable: renamed observable:NetworkConnetion to observable:NetworkConnection \[CP-69\]
    
*   uco-observable: renamed all instances of core:DigitalAddressFacet to observable:DigitalAddressFacet \[CP-69\]
    
*   uco-observable: renamed all instances of core:IPAddressFacet to observable:IPAdressFacet \[CP-69\]
    
*   uco-observable: renamed all instances of core:MACAddressFacet to observable:MACAddressFacet \[CP-69\]
    
*   uco-observable: modified the rdfs:subClassOf observable:SymbolicLink to be observable:FileSystemObject \[CP-69\]
    
*   uco-observable: modified the range of observable:partitionID from xsd:integer to xsd:string \[CP-46\]
    
*   uco-observable: modified the range of observable:clockSetting from xsd:string to xsd:dateTime \[CP-58\]
    
*   uco-core: modified the range of core:createdBy from identity:Identity to core:IdentityAbstraction \[CP-62\]
    
*   uco-core: modified the range of core:objectMarking from marking:MarkingDefinition to core:MarkingDefinitionAbstraction \[CP-62\]
    

#### Range Changes (These are changes to the “range” of a property that are not breaking changes: typically these are broadening in the scope of the range.)

*   uco-observable: modified the range of observable:mockLocationsAllowed to only include xsd:boolean \[CP-72\]
    
*   uco-observable: modified the range of observable:phoneActivationTime to only include xsd:dateTime \[CP-72\]
    
*   uco-observable: modified the range of observable:status to be an owl:unionOf xsd:string, vocabulary:TaskStatusVocab and vocabulary:WhoisStatusTypeVocab \[CP-73\]
    
*   uco-observable: modified the range of the observable:status property restriction on observable:WindowsTaskFacet to only include vocabulary:TaskStatusVocab \[CP-73\]
    
*   uco-observable: modified the range of the observable:status property restriction on observable:ProcessFacet to only include xsd:string \[CP-73\]
    
*   uco-observable: modified the range of observable:priority to be an owl:unionOf xsd:string, xsd:integer, and vocabulary:TaskPriorityVocab \[CP-74\]
    
*   uco-observable: modified the range of the observable:priority property restriction on observable:WindowsTaskFacet to only include vocabulary:TaskPriorityVocab \[CP-74\]
    
*   uco-observable: modified the range of the observable:priority property restriction on observable:WindowsThreadFacet to only include xsd:integer \[CP-74\]
    
*   uco-observable: modified the range of observable:WindowsPESection to only include xsd:double \[CP-75\]
    
*   uco-observable: modified the range of observable:owner to only include core:UcoObject \[CP-76\]
    
    *   updated all classes where observable:owner was used as a property restriction
        
        *   observable:AccountFacet
            
        *   observable:CalendarEntryFacet
            
        *   observable:CalendarFacet
            
        *   observable:FilePermissionsFacet
            
*   uco-types: modified the range of types:entry to be an owl:unionOf types:ControlledDictionaryEntry and types:DictionaryEntry \[CP-77\]
    
*   uco-types: modified the range of the types:entry property restriction on types:ControlledDictionaryEntry to only include types:ControlledDictionaryEntry \[CP-77\]
    

#### Changes (These are changes to the preexisting ontology that are not breaking or range changes.)

*   uco-observable: modified name of property restriction for observable:ContactAddress from observable:observable:geolocationAddress to observable:geolocationAddress \[CP-5\]
    
*   uco-observable: modified names of property restrictions for observable:ContactAffiliation \[CP-5\]
    
    *   from observable:observable:organizationDepartment to observable:organizationDepartment
        
    *   from observable:observable:organizationPosition to observable:organizationPosition
        
    *   from observable:observable:organizationLocatoin to observable:organizationLocation
        
    *   from observable:observable:contactEmail to observable:contactEmail
        
    *   from observable:observable:contactMessaging to observable:contactMessaging
        
    *   from observable:observable:contactPhone to observable:contactPhone
        
    *   from observable:observable:contactProfile to observable:contactProfile
        
    *   from observable:observable:contactURL to observable:contactURL
        
*   uco-observable: modified name of property restriction for observable:ContactEmail from observable:observable:emailAddress to observable:emailAddress \[CP-5\]
    
*   uco-observable: modified name of property restriction for observable:ContactListFacet from observable:observable:sourceApplication to observable:sourceApplication \[CP-5\]
    
*   uco-observable: modified names of property restrictions for observable:ContactMessaging \[CP-5\]
    
    *   from observable:observable:contactAddress to observable:contactAddress
        
    *   from observable:observable:contactMessagingPlatform to observable:contactMessagingPlatform
        
*   uco-observable: modified name of property restriction for observable:ContactPhone from observable:observable:contactPhoneNumber to observable:contactPhoneNumber \[CP-5\]
    
*   uco-observable: modified name of property restriction for observable:ContactSIP from observable:observable:sipAddress to observable:sipAddress \[CP-5\]
    
*   uco-observable: modified name of property restriction for observable:ContactURL from observable:observable:url to observable:url \[CP-5\]
    
*   uco-core: modified the cardinality of the core:id property restriction on core:UcoObject from exactly 1 to at most 1 \[CP-63\]
    
*   uco-core: modified owl:onClass for the core:createdBy property restriction on core:UcoObject to be core:IdentityAbstraction \[CP-63\]
    
*   uco-observable: renamed observable:profilelanguage to observable:profileLanguage \[CP-65\]
    
*   uco-core: changed the URI’s within the property restrictions for core:ExternalReference to use namespace prefixes (i.e., “core:{property}”) \[CP-53\]
    
    *   owl:onProperty <[https://unifiedcyberontology/ontology/uco/core#definingContext](https://unifiedcyberontology/ontology/uco/core#definingContext)\> became owl:onProperty core:definingContext
        
    *   owl:onProperty <[https://unifiedcyberontology/ontology/uco/core#externalIdentifier](https://unifiedcyberontology/ontology/uco/core#externalIdentifier)\> became owl:onProperty core:externalIdentifier
        
    *   owl:onProperty <[https://unifiedcyberontology/ontology/uco/core#referenceURL](https://unifiedcyberontology/ontology/uco/core#referenceURL)\> became own:onProperty core:referenceURL
        
*   uco-observable: changed the URI’s within the property restrictions for observable:OnlineService to use namespace prefixes (i.e., “observable:{property}”) \[CP-53\]
    
    *   owl:onProperty <[https://unifiedcyberontlogy/ontology/uco/observable#inetLocation](https://unifiedcyberontlogy/ontology/uco/observable#inetLocation)\> became owl:onProperty observable:inetLocation
        
    *   owl:onProperty <[https://unifiedcyberontology/ontology/uco/observable#location](https://unifiedcyberontology/ontology/uco/observable#location)\> became owl:onProperty observable:location
        
*   uco-observable: fixed typos within the rdfs:subClassOf statement of a few class objects \[CP-48\]
    
    *   observable:GeoLocationEntry: subclass now reads rdfs:subClassOf observable:ObservableObject
        
    *   observable:OnlineService: subclass now reads rdfs:subClassOf observable:ObservableObject
        
    *   observable:Snapshot: subclass now reads rdfs:subClassOf observable:ObservableObject
        
*   uco-observable: modified the cardinality for observable:hasChanged from exactly 1 to at most 1 \[CP-59\]
    

### Deprecations/Deletions (These are classes or properties that were deprecated from the ontology.)

*   all namespaces: removed all domain assertion files (\*-da.ttl) with the implementation of SHACL \[CP-23\]
    
*   all namespaces: removed all owl:restriction property constraints on files and replaced with SHACL property shapes \[CP-23\]
    
*   uco-core: removed reference to identity:Identity \[CP-62\]
    
*   uco-core: removed reference to marking:MarkingDefinition \[CP-62\]
    
*   uco-observable: removed observable:faxNumber \[CP-64\]
    
*   uco-core: removed core:role \[CP-66\]
    

### Additions

#### Class Additions (These are classes that were added.)

*   uco-core: added the class core:IdentityAbstraction as a subclass of core:UcoObject \[CP-62\]
    
*   uco-core: added the class core:MarkingDefinitionAbstraction as a subclass of core:UcoObject \[CP-62\]
    

#### Property Additions (These are properties that were added.)

*   uco-observable: added the property observable:listedCount with a range of xsd:integer \[CP-78\]
    
    *   observable:listedCount is included as a property restriction on observable:TwitterProfileFacet
        

### Vocabulary Additions/Changes (These are any vocabularies that were added or modified.)

### Annotation Changes

*   uco-core: changed rdfs:comment for core:object to read “Specifies one or more UcoObjects.” \[CP-60\]
    
*   uco-observable: changed rdfs:comment for observable:owner to read “Specifies the owner of an Observable Object.” \[CP-60\]
    
*   uco-observable: changed rdfs:comment for observable:password to read “Specifies an authentication password.” \[CP-60\]
    
*   uco-core: modified the rdfs:comment for core:specVersion to read “The version of UCO ontology or subontology specification used to characterize a concept.” \[CP-55\]
    
*   uco-observable: added an rdfs:comment to observable:sizeInBytes within the property restriction of observable:FileFacet \[CP-54\]
    
    *   the rdfs:comment now reads “When used to characterize a file the sizeInBytes property conveys the recorded size of a file in a file system.”
        

* * *

### Known Issues

*   Any UCO instance content asserting not only a value for the core:kindOfRelationship property on a core:Relationship object but also asserting a specific vocabulary datatype for it will generate a SHACL validation error as the sh:datatype constraint in the ontology is defined as xsd:string due to the intentional general nature of the core:kindOfRelationship property. This is “correct” behavior though unsatisfying from a validation perspective for adopters wishing to be very specific in their content. There is potential for future adjustments to the SHACL to maintain “correct” validation but also to make it a little more satisfying for explicitly specific adopters.
    
*   Validation for any graph of UCO content containing references (ObjectProperties) to objects (by object ID) where the objects themselves are not explicitly defined in the graph (e.g., references to externally defined content such as linked data or previously defined but not repeated content) will generate SHACL class validation errors given that the graph does not contain enough information for the validator to determine the asserted class of the object by its ID alone. Further investigation, discussion and consideration will be required to determine how this issue will be addressed in future versions of UCO.
    

Document generated by Confluence on Aug 18, 2021 18:14

[Atlassian](http://www.atlassian.com/)

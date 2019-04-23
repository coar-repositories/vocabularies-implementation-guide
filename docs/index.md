# Vocabularies Implementation Guide

## Introduction

The use of controlled vocabularies for bibliographic metadata "ensures that everyone is using the same word to mean the same thing". The continuous review update and maintenance of the COAR Controlled Vocabularies and their adoption by the most commonly used open repository software is a way to enhance the interoperability across repositories and with other related systems such as harvesters, CRIS systems, data repositories and publishers.

## COAR Controlled Vocabularies 

COAR actively works towards the alignment of repository networks and other systems via technical and semantic interoperability, as well as common approaches to policy and services. In 2014, COAR established the Interest Group "Controlled Vocabularies for Repository Assets" to develop a set of controlled vocabularies for the bibliographic metadata elements used in records describing research outputs.

The <a https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/ >COAR Controlled Vocabularies</a> are governed and maintained by the Editorial Board. In order to define the controlled vocabularies, the Editorial Board analyses existing vocabularies and dictionaries and will use the most appropriate existing terms whenever possible. In the case where there are gaps, new terms are defined by the group.

The COAR Controlled Vocabularies are described in SKOS. In SKOS, concepts are identified using URIs, labels to the concepts are uniquely offered in multiple languages, notes allow for description, as well as different annotations and concepts from other vocabularies can be linked. Workflow and web-based editorial processes are managed on VocBench. 

The URL prefix http://purl.org/coar is reserved as the namespace for the concepts of the COAR Controlled Vocabularies. <a https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/controlled-vocabularies-faq/ >FAQs</a> for COAR Controlled Vocabularies are available.

### Resource type vocabulary

The <a https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/deliverables/ >Resource Type vocabulary</a> defines concepts to identify the genre of a resource. The Resource Type vocabulary builds on and extends the controlled list of publication types defined in info:eu-repo/semantics. 
<ul>
 <li>50 concepts supported
 <li>Labels available in (currently) 14 languages including Arabic, Catalan, Chinese, Czech, Dutch, English, French, German, Italian, Portuguese, Russian, Spanish, Japanese, Turkish.
 <li>Concepts are assigned permanent identifiers (URIs)
 <li>Hierarchical structure
 <li>Mappings ('matches') to terms of other controlled vocabularies
 <li>Published under CC-BY 4.0
</ul>
Current version of the vocabulary is <a http://vocabularies.coar-repositories.org/documentation/resource_types/2.0.draft/ >Resource Type Vocabulary v.2.0 Draft</a> (May 2018) and github files for <a https://github.com/coar-repositories/vocabularies/tree/master/resource_types >SKOS-XL RDF</a> and changelog are available at the given links.

### Access rights

<a https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/access-rights-vocabulary/> The Access Rights vocabulary</a> defines concepts to declare the access status of a resource. Multilingual labels regard regional distinctions in language and term. It builds on access rights defined in info:eu-repo/semantics 

<ul>
 <li>4 concepts supported
 <li>Labels available in (currently) 6 languages including English, Spanish, Turkish, French, Japanese, German. 
 <li>Concepts are assigned permanent identifiers (URIs)
 <li>Hierarchical structure
 <li>Mappings ('matches') to terms of other controlled vocabularies
 <li>Published under CC-BY 4.0
</ul>

Current version of the vocabulary is <a http://vocabularies.coar-repositories.org/documentation/access_rights/  >Access Rights Vocabulary v.1.0</a>  (January 2019) and github files for <a https://github.com/coar-repositories/vocabularies/tree/master/access_rights >SKOS-XL RDF</a> and changelog are available at the given link.

### Version types

<a https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/version-type-vocabulary >The Version Type vocabulary</a> defines concepts to declare the version of a resource. Multilingual labels regard regional distinctions in language and term. The concepts are adopted from the "<a https://www.niso.org/publications/niso-rp-8-2008-jav >Journal Article Versions (JAV): Recommendations of the NISO/ALPSP JAV Technical Working Group</a>". 

Current version of the vocabulary is <a http://vocabularies.coar-repositories.org/documentation/version_types/ >Version Type Vocabulary v.1 Draft</a> (July 2018) and github files for <a https://github.com/coar-repositories/vocabularies/tree/master/version_types/snapshot >SKOS-XL RDF</a> and changelog  are available at the given link.

## Implementing Controlled Vocabularies
### Mapping vocabularies

To implement vocabularies locally, you may need to map the other terms of locally used vocabularies with COAR Controlled Vocabularies concepts. 
 
Please note that it is not mandatory to use the whole set of concepts in COAR Vocabularies. COAR Vocabularies are offered in a hierarchical structure and depending on the needs of the repository, you may decide not to use some of the concepts and/or labels. See an example of mapping table below: 

Terms in info:eu-repo/semantics | Terms in RepositóriUM types | Concept label in COAR Vocabularies | Concept URI
------------ | ------------- | ------------ | ------------
article      | article  | Journal article | http://purl.org/coar/resource_type/c_6501
bachelorThesis | bachelorThesis  | bachelor thesis | http://purl.org/coar/resource_type/c_7a1f
bookPart | bookPart  | book part | http://purl.org/coar/resource_type/c_3248

### Implementing controlled vocabularies in DSpace and DSpace-CRIS

COAR vocabularies can be implemented in repositories operating on DSpace by customising input forms or using the Dspace software functionality. 












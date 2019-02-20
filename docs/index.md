# Vocabularies Implementation Guide

## Introduction

The use of controlled vocabularies for bibliographic metadata "ensures that everyone is using the same word to mean the same thing". The continuous review update and maintenance of the COAR Controlled Vocabularies and their adoption by the most commonly used open repository software is a way to enhance the interoperability across repositories and with other related systems such as harvesters, CRIS systems, data repositories and publishers.

## COAR Controlled Vocabularies 

COAR actively works towards the alignment of repository networks and other systems via technical and semantic interoperability, as well as common approaches to policy and services. In 2014, COAR established the Interest Group "Controlled Vocabularies for Repository Assets" to develop a set of controlled vocabularies for the bibliographic metadata elements used in records describing research outputs.

The COAR Controlled Vocabularies are governed and maintained by the Editorial Board. In order to define the controlled vocabularies, the Editorial Board analyzes existing vocabularies and dictionaries and will use the most appropriate existing terms whenever possible. In the case where there are gaps, new terms are defined by the group.

The COAR Controlled Vocabularies are described in SKOS. In SKOS, concepts are identified using URIs, labels to the concepts are uniquely offered in multiple languages, notes allow for description, as well as different annotations and concepts from other vocabularies can be linked. Workflow and web-based editorial processes are managed on VocBench. 

The URL prefix http://purl.org/coar is reserved as the namespace for the concepts of the COAR Controlled Vocabularies. FAQs  for COAR Controlled Vocabularies is available.

### Resource type vocabulary

The Resource Type vocabulary defines concepts to identify the genre of a resource. The Resource Type vocabulary builds on and extends the controlled list of publication types defined in info:eu-repo/semantics. 
<ul>
 <li>50 concepts supported
 <li>Labels available in (currently) 14 languages including Arabic, Catalan, Chinese, Czech, Dutch, English, French, German, Italian, Portuguese, Russian, Spanish, Japanese, Turkish.
 <li>Concepts are assigned permanent identifiers (URIs)
 <li>Hierarchical structure
 <li>Mappings ('matches') to terms of other controlled vocabularies
 <li>Published under CC-BY 4.0
</ul>
Current version of the vocabulary is Resource Type Vocabulary v.2.0 Draft (May 2018)  and github files for SKOS-XL RDF and changelog are available at the given links.

### Access rights

The Access Rights vocabulary[6] defines concepts to declare the access status of a resource. Multilingual labels regard regional distinctions in language and term. It builds on access rights defined in info:eu-repo/semantics 

<ul>
 <li>4 concepts supported
 <li>Labels available in (currently) 6 languages including English, Spanish, Turkish, French, Japanese, German. 
 <li>Concepts are assigned permanent identifiers (URIs)
 <li>Hierarchical structure
 <li>Mappings ('matches') to terms of other controlled vocabularies
 <li>Published under CC-BY 4.0
</ul>

Current version of the vocabulary is Access Rights Vocabulary v.1.0 (January 2019)[7] and github files for SKOS-XL RDF and changelog  are available at the given link.

### Version types

The Version Type vocabulary[8] defines concepts to declare the version of a resource. Multilingual labels regard regional distinctions in language and term. The concepts are adopted from the "Journal Article Versions (JAV): Recommendations of the NISO/ALPSP JAV Technical Working Group". 

Current version of the vocabulary is Version Type Vocabulary v.1 Draft (July 2018)[10] and github files for SKOS-XL RDF and changelog  are available at the given link.

<hr />
<p>[6] <a https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/access-rights-vocabulary/  >Access Rights vocabulary</a>.</p>
<p>[7] <a http://vocabularies.coar-repositories.org/documentation/access_rights/  >Controlled Vocabulary for Access Rights (Version 1.0)</a>.</p>
<p>[8] <a https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/version-type-vocabulary/  >Version type vocabulary</a>.</p>
<p>[9] <a https://www.niso.org/publications/niso-rp-8-2008-jav  >The NISO/ALPSP JAV Technical Working Group</a>.</p>
<p>[10] <a http://vocabularies.coar-repositories.org/documentation/version_types/ >Controlled Vocabulary for Version Types (Draft V1)</a>.</p>


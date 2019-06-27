# Vocabularies Implementation Guide

## **Introduction**

The use of controlled vocabularies for bibliographic metadata "ensures that everyone is using the same word to mean the same thing". The continuous review update and maintenance of the COAR Controlled Vocabularies and their adoption by the most commonly used open repository software is a way to enhance the interoperability across repositories and with other related systems such as harvesters, CRIS systems, data repositories and publishers.

## **COAR Controlled Vocabularies**

COAR actively works towards the alignment of repository networks and other systems via technical and semantic interoperability, as well as common approaches to policy and services. In 2014, COAR established the Interest Group "Controlled Vocabularies for Repository Assets" to develop a set of controlled vocabularies for the bibliographic metadata elements used in records describing research outputs.

The <a href="https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies">COAR Controlled Vocabularies</a> are governed and maintained by the Editorial Board. In order to define the controlled vocabularies, the Editorial Board analyses existing vocabularies and dictionaries and will use the most appropriate existing terms whenever possible. In the case where there are gaps, new terms are defined by the group.

The COAR Controlled Vocabularies are described in SKOS. In SKOS, concepts are identified using URIs, labels to the concepts are uniquely offered in multiple languages, notes allow for description, as well as different annotations and concepts from other vocabularies can be linked. Workflow and web-based editorial processes are managed on VocBench.

The URL prefix http://purl.org/coar is reserved as the namespace for the concepts of the COAR Controlled Vocabularies. <a href="https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/controlled-vocabularies-faq">FAQs</a> for COAR Controlled Vocabularies are available.

### **Resource type vocabulary**

The <a href="https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/deliverables">Resource Type vocabulary</a> defines concepts to identify the genre of a resource. The Resource Type vocabulary builds on and extends the controlled list of publication types defined in info:eu-repo/semantics.
<ul>
 <li>50 concepts supported
 <li>Labels available in (currently) 14 languages including Arabic, Catalan, Chinese, Czech, Dutch, English, French, German, Italian, Portuguese, Russian, Spanish, Japanese, Turkish.
 <li>Concepts are assigned permanent identifiers (URIs)
 <li>Hierarchical structure
 <li>Mappings ('matches') to terms of other controlled vocabularies
 <li>Published under CC-BY 4.0
</ul>
Current version of the vocabulary is <a href="http://vocabularies.coar-repositories.org/documentation/resource_types/2.0.draft">Resource Type Vocabulary v.2.0 Draft</a> (May 2018) and github files for <a href="https://github.com/coar-repositories/vocabularies/tree/master/resource_types">SKOS-XL RDF</a> and changelog are available at the given links.

### **Access rights**

<a href="https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/access-rights-vocabulary"> The Access Rights vocabulary</a> defines concepts to declare the access status of a resource. Multilingual labels regard regional distinctions in language and term. It builds on access rights defined in info:eu-repo/semantics

<ul>
 <li>4 concepts supported
 <li>Labels available in (currently) 6 languages including English, Spanish, Turkish, French, Japanese, German.
 <li>Concepts are assigned permanent identifiers (URIs)
 <li>Hierarchical structure
 <li>Mappings ('matches') to terms of other controlled vocabularies
 <li>Published under CC-BY 4.0
</ul>

Current version of the vocabulary is <a href="http://vocabularies.coar-repositories.org/documentation/access_rights">Access Rights Vocabulary v.1.0</a>  (January 2019) and github files for <a href="https://github.com/coar-repositories/vocabularies/tree/master/access_rights">SKOS-XL RDF</a> and changelog are available at the given link.

### **Version types**

<a href="https://www.coar-repositories.org/activities/repository-interoperability/coar-vocabularies/version-type-vocabulary">The Version Type vocabulary</a> defines concepts to declare the version of a resource. Multilingual labels regard regional distinctions in language and term. The concepts are adopted from the "<a href="https://www.niso.org/publications/niso-rp-8-2008-jav">Journal Article Versions (JAV): Recommendations of the NISO/ALPSP JAV Technical Working Group</a>".

Current version of the vocabulary is <a href="http://vocabularies.coar-repositories.org/documentation/version_types">Version Type Vocabulary v.1 Draft</a> (July 2018) and github files for <a href=" https://github.com/coar-repositories/vocabularies/tree/master/version_types/snapshot">SKOS-XL RDF</a> and changelog  are available at the given link.

## **Mapping vocabularies**

To implement vocabularies locally, you may need to map the other terms of locally used vocabularies with COAR Controlled Vocabularies concepts.

Please note that it is not mandatory to use the whole set of concepts in COAR Vocabularies. COAR Vocabularies are offered in a hierarchical structure and depending on the needs of the repository, you may decide not to use some of the concepts and/or labels. See an example of mapping table below:

Terms in info:eu-repo/semantics | Terms in RepositóriUM types | Concept label in COAR Vocabularies | Concept URI
------------ | ------------- | ------------ | ------------
article      | article  | Journal article | http://purl.org/coar/resource_type/c_6501
bachelorThesis | bachelorThesis  | bachelor thesis | http://purl.org/coar/resource_type/c_7a1f
bookPart | bookPart  | book part | http://purl.org/coar/resource_type/c_3248

## **Implementation in DSpace and DSpace-CRIS**

COAR vocabularies can be implemented in repositories operating on DSpace by customising input forms or using the Dspace software functionality.

[image to be added]

DSpace supports controlled vocabularies in search and submission process. Supported controlled vocabularies are expressed in a simple XML format ("DSpace node schema"). All information about a term is enclosed in a <node> element. Only the expression of a hierarchical relationship is allowed through the use of the <isComposedBy> sub element. By using <hasNote> a simple annotation mechanism becomes possible. Hierarchical Taxonomies and Controlled Vocabularies are well explained in <a href="https://wiki.duraspace.org/display/DSDOC5x/Authority+Control+of+Metadata+Values#AuthorityControlofMetadataValues-HierarchicalTaxonomiesandControlledVocabularies "> DuraSpace wiki</a> pages. <a href="http://dspace.2283337.n4.nabble.com/dspace-Patches-1833347-Controlled-Vocabulary-Add-on-update-Patch-for-DSpace-1-4-2-td3289431.html"> DSpace developer community forums</a> may also helpful for relevant update patches.

In DSpace, you have two options to implement COAR Controlled Vocabularies. Option 1 includes a dropdown list of the fields to allow the submitter to select one option. Option 2 uses the <a href="https://wiki.duraspace.org/pages/viewpage.action?pageId=19006518 ">internal controlled vocabularies functionality</a> in DSpace.

### **Option 1: Dropdown**

This option includes a dropdown list of the fields to allow the submitter to select one option. You may find the implementation steps below:

[image to be added]

1.Create a separate <form- definition> for each community per type inside the input-forms.xml file.

    <name-map collection-handle="1111/33333" form-name="book" />

2.Example of the field in input-forms.xml

    <field>
    <dc-schema>dc</dc-schema>
    <dc-element>type</dc-element>
    <dc-qualifier></dc-qualifier>
    <repeatable>false</repeatable>
    <label>Tipo</label>
    <input-type value-pairs- name="common_types">dropdown</input- type>
    <hint>xyz.</hint>
    <required></required>
    </field>

3.Provide a way to show (flat term) type name instead of URL eg. Show "software" instead of > http://purl.org/coar/resource_type/c_5ce6   


### **Option 2: Using Dspace Functionality**

This option uses the internal functionality of controlled vocabularies in Dspace to present the COAR types. Note that this prototype implementation is valid Dspace version 5 and above. You may find the implementation steps below:

[image to be added]

1.Insert provided coar-types.xml in ${DSpace_HOME}/dspace/config/controlled-vocabularies/

2.Switch in ${DSpace_HOME}/dspace/config/input-forms.xml at dc:type field and change input type for <input-type >onebox</input-type> and insert in the same field the tag <vocabulary closed="true">coar-types</vocabulary>, this tag forces the input to be only through the plugin.

3.Example of the field in input-forms.xml:

    <field>
    <dc-schema>dc</dc-schema>
    <dc-element>type</dc-element>
    <dc-qualifier></dc-qualifier>
    <repeatable>false</repeatable>
    <label>Type</label>
    <input-type>onebox</input-type>
    <hint>Select the type(s) of content of the item. </hint>
    <required></required>
    <vocabulary closed="true"> coar-types</ vocabulary>
    </field>

4.In dspace.cfg Edit the value to “true”:
    webui.controlledvocabulary.enable = true # allows the use of the controlled vocabularies add-on to allow the tree visualization mode;

5.Add the following lines:

      choices.plugin.dc.type = coar-types # field (dc.type) to use the plugin and name of file with the vocabularies;
      choices.presentation.dc.type = select # field presentation mode;
      vocabulary.plugin.coar.hierarchy.store = true # saves in database the tree hierarchy;
      vocabulary.plugin.coar.hierarchy.suggest = true # show selected type with its hierarchy;
      vocabulary.plugin.coar.delimiter = "::" # delimiter to use between different hierarchic levels;   

### **How to encode it?**

Text or figure to be added
Provide at least two values:
1. the concept URI - http://purl.org/coar/resource_type/c_6501
2. a label belongs to the concept


### **Changes required for each implementation**

The following table describes the changes in different levels on DSpace regarding each implementation. Repository managers can make all changes or just a basic implementation by changing only the submission process in one of the two options.

| Dspace | Option 1 – Dropdown | Option 2 – Software functionality
| ------ | ------------------- | -----------------------|
| Submission process | Change value pairs on the input-forms.xml | Use Controlled Vocabularies functionality
| Recorded info | Saves the codes (e.g:c_ecc8) | Saved the text string (e.g.:text:book)
| Item type display | Doesn’t require conversion. Recommended to modify COAR code to Driver types label | Use XOAI to map information (text strings to code)
| API | Rest output – nothing to do, the COAR code is exposed | Rest output – develop a mapping. Requires development in dspace-rest
| SWORD ingest | Analyse and modify existing mapping | Analyse and modify existing mapping

## **Implementation in Samvera (including Hyrax)**

Samvera (and some of its variants, including Hyrax and Haiku), is designed, 'out of the box' to be able to exploit the use of controlled vocabularies in both its data model and in its user interfaces for input (ingest), browsing and searching. This is facilitated by a component with the amusing name <a href="https://github.com/samvera/questioning_authority ">Questioning Authority (QA)</a>. There are, essentially, two ways to implement a controlled vocabulary in Samvera with QA - either to connect QA directly to a remote web service providing the vocabulary, or to copy the vocabulary into a file within the repository. The second of these two options is much simpler to configure, and the Samvera community has provided <a href="https://samvera.github.io/customize-metadata-controlled-vocabulary.html">clear documentation</a> about how to do this . It has the advantage of no reliance on any external resource once configured, but the disadvantage that the file must be manually updated if the vocabulary is revised.

The format of the file used by QA is very simple, essentially linking the URI of each term in the vocabulary to the label which will be used in the repository's user interface. The data model in Samvera is already a linked-data graph, so the URIs in the vocabulary are used directly by the repository in metadata records.

## **Repositories implemented COAR Controlled Vocabularies**

| Country | Institution | Software | Repository Name | Type of implementation
| ----------- | -------- | --------------- | ---------------------- | -------------|
| Portugal | University of Minho | DSpace | <a href="http://repositorium.sdum.uminho.pt">Repositorium</a> | Dropdown list
| Spain | Spanish National Research Council | DSpace | <a href="https://digital.csic.es">DIGITAL.CSIC</a> | DSpace functionality

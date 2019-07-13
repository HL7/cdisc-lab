---
title: Downloads
layout: default
active: downloads
---
<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}


<!-- end TOC -->

### Package File

The following package file contains an NPM Package used by many of the FHIR tools. It includes all the value sets, profiles, extensions, list of pages and urls in the IG, etc defined as part of this version of the Implementation Guides.:

- [Package](package.tgz)

### Documentation

A narrative, FHIR resource domain model, and FHIR to CDISC data mappings are provided to assist in transforming laboratory data in FHIR format to a CDISC-compliant structures and standards.

### Use Case 1: FHIR to CDISC LAB XML

For the September 2018 Connectathon, transformation code was written to query a sandbox FHIR server and convert the resulting FHIR file into the CDISC LAB XML standard format.  The code is written in Java and is available in github.  The FHIR to CDISC data mapping contains the path information that was used in the Java code. 
[Connectathon Code for Lab IG](http://github.com/jennindg/MDIT_FHIR_LDM/tree/connectathon2018/)  A sample data set has been developed to provide example data for testing.  

[Sample Data](LB test data for IG.htm)

Download the sample data spreadsheet [here.](LB test data for IG.xlsx)

#### Clinical Research Laboratory Data Narrative

Narratives, also known as scenarios, provide insight and context around the domain being discussed.  By walking the reader through a fictitious example, the narrative highlights concepts important for the mapping and modeling work, and provides details for the creation of the test data set.

[Lab Narrative](Lab Narrative for IG.htm)

Download the entire word document here: [Lab Narrative for IG.docx](Lab Narrative for IG.docx)

#### Clinical Research Laboratory Domain Model

The domain model provides a graphic representation of the relevant FHIR resources, attributes, and associations.

[Domain Model](assets/images/Lab IG UML Diagram.jpg)  

#### FHIR to CDISC Laboratory Data Mapping

The FHIR to CDISC mapping is useful for understanding how to relate FHIR resources and attributes to CDISC-compliant data structures and standards.  To ensure a more comprehensive solution, FHIR resources are compared (mapped) to three existing CDISC standards that are used in clinical research laboratory data exchange:  the CDISC LAB model, CDASH LB Domain variables, and SDTM LB variables.  

[Data Mapping](LAB_LB_FHIR_mapping_and_gaps_for_IG.htm)

Download the entire spreadsheet here:  [LAB_LB_FHIR_mapping_and_gaps_for_IG.xlsx](LAB_LB_FHIR_mapping_and_gaps_for_IG.xlsx)

### Use Case 2: FHIR to CDISC CDASH or SDTM

Since implementations of CDASH and SDTM data stores may vary by sponsor, please see the FHIR to CDISC data mapping document for field level equivalencies to use in processing FHIR lab data files.

[Data Mapping](LAB_LB_FHIR_mapping_and_gaps_for_IG.htm)

Download the entire spreadsheet here:  [LAB_LB_FHIR_mapping_and_gaps_for_IG.xlsx](LAB_LB_FHIR_mapping_and_gaps_for_IG.xlsx)

### IG Download

Download the entire implementation guide [here.](full-ig.zip)

<br/>

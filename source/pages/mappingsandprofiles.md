---
title: Mappings and Profiles
layout: default
active: profiles
---
<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}


<!-- end TOC -->

### FHIR to CDISC Laboratory Data Mapping

The FHIR to CDISC mapping is useful for understanding how to relate FHIR resources and attributes to CDISC-compliant data structures and standards.  To ensure a more comprehensive solution, FHIR resources are compared (mapped) to three existing CDISC standards that are used in clinical research laboratory data exchange:  the CDISC LAB model, CDASH LB Domain variables, and SDTM LB variables.  

Data Mapping:  [LAB_LB_FHIR_mapping_and_gaps_for_IG.xlsx](LAB_LB_FHIR_mapping_and_gaps_for_IG.xlsx)

<br/>

### Profiles

No profiles are applicable  for this implementation guide.

<br/>

### Extensions

* Observation: Observation to ResearchStudy linkage (workflow-researchStudy) associates lab results with a particular study [Observation to ResearchStudy](http://hl7.org/fhir/StructureDefinition/workflow-researchStudy) 
* Specimen: Cqf-relativeDateTime captures the collection relative to an event, such as administration of medication [Relative Collection](https://www.hl7.org/fhir/extension-cqf-relativedatetime.html) 
* Race: Patient race (us-core-race) [Race](http://www.hl7.org/fhir/us/core/StructureDefinition-us-core-race.html) 

<br/>

---
title: Implementation Guidance
layout: default
active: guidance
f: http://build.fhir.org/
---

{:.no_toc}

<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}

### Introduction  

The implementation guidance outlined in this page provides useful information for developers consuming laboratory data from FHIR.

<br/>

### Assumptions and Constraints  

1. Site should be able to provide study laboratory results via FHIR for the following queries:
	1. All lab data for a Study
	1. All lab data for a Research Subject participating in a Study
	1. Lab data produced within a time frame for a Study 
1. The starting point for the lab implementation guide instructions is the file of laboratory data in FHIR format
1. Observation.category.code should be set to 'laboratory' to assist in separating laboratory results from other observations
1. NOTE:  Personally identifiable information, such as race, patient initials, and birth date are included in the LAB XML standard and mapping, but should not be provided to sponsor companies without sufficient justification (e.g., required to perform patient reconciliation).

<br/>

### Gaps  

​Some attributes or variables within the CDISC standards do not have corresponding attributes within a FHIR resource.  In some circumstances, data are provided through an alternative method, such as a supplemental file or transmission agreement. Alternately, data may be derived through information provided in a different field and/or resource. Please see the data mapping document for gap and mitigation information.
<br/>

### Target State  

The desired future state includes implementation of two research resources (ResearchStudy and ResearchSubject) and enhancements to existing FHIR resources.  To support the future state, two core FHIR resources were modified and extended to support CDISC lab clinical research standards. 

#### R4 Resource Additions  
* Specimen: Specimen.collection CollectedPeriod, for specimens collected over a period of time (e.g., 24 hours)
* Specimen: Specimen.collection.fastingStatus, captures whether the subject has fasted prior to specimen collection
* Specimen: Specimen.condition, captures environmental or quality information about the specimen
* Specimen: Specimen.note extended to Organizations, supports laboratory comments that are not attributed to a specific person (e.g., produced by the instruments)
* Observation: Observation.interpretation cardinality modified to allow multiple interpretations

#### R4 Extensions and Profiles  
* Observation: Observation to ResearchStudy linkage (event-researchStudy), associated lab results with a particular study
* Specimen: Cqf-relativeDateTime, captures the collection relative to an event, such as administration of medication

<br/>

### Short-Term vs. Target State  

If clinical research and/or R4 resources have not been implemented in site systems, sites may by inclined to rely on prior versions of FHIR resources used in Patient Care (Observation and Patient) as a short-term solution for sharing laboratory data with sponsors.  Although this allows sites to share data through their current FHIR resources, limitations and risks should be considered.  

#### Short-Term Limitations  
The short-term solution excludes several resources and extensions which are useful for lab data:
1. ResearchStudy: includes status and investigator information
1. ResearchSubject: preferred over Patient because it masks the PII that the Patient resource may expose and enables a Sponsor to recreate the history of patient statuses/milestones
1. DiagnosticReport: helpful for understanding groups of tests performed (battery of tests)
1. Encounter: provides the visit date, which is preferred over inferring visit and specimen collection dates from observation date
1. Specimen: provides the context around the collection and quality of the specimen
1. Linkage between Observation and Study: useful in identifying results that have been collected for the research study, but support the study  

#### Short-Term Risks  
Risks of using the short-term solution:
* The short-term solution does not facilitate easy retrieval and use of the data.  Required fields, such as the study identifier or subject identifier would require additional effort to provide and maintain with the data set. 
* Use of the Patient resource, rather than Research Subject, may result in unintentional disclosure of PII or complexity in managing patient and/or subject identifiers.
* Use of the observation date (date on which the lab result was generated), rather than the specimen collection or encounter dates, could result in date being associated with the incorrect patient visit if results are not generated on the collection date.
* Without study information associated with the observations, the sponsor would need to ensure that a study identifier is associated with the FHIR data files. 

#### Implementation of Short-Term Solution  

Without the associations between a Research Subject, Patient, and Observation, implementers may seek alternative ways of representing these linkages.  One method is to use observation.subject to provide Research Subject and Research Study identifiers, rather than pointing to the Patient resource.  If observation.subject contains an identifier that is not an identifier for one of the reference resource types (Patient, Group, Device, or Location), use an identifier type to indicate the context of the identifier. For example, if observation.subject contains the Research Subject identifier, set the identifier type to 'Research Subject ID.'  Please note that this is not a desired long-term solution as it requires additional interpretation by the data consumer and is not compliant with the Observation FHIR resource definition.

<br/>

---
title: Clinical Research Sponsor Laboratory Semantics in FHIR Implementation Guide
layout: default
active: overview
---

<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}


<!-- end TOC -->

###  Background
To address the challenge of communicating across varying standards, the BR&R team partnered with clinical research sponsor organizations to understand the various standards for recording and submitting laboratory data.  Through this partnership, mappings were developed between the FHIR standard that is emerging in research, and the CDISC standards currently being used.

This implementation guide focuses on mapping laboratory data from FHIR to CDISC (See #4 below).

{% include img-portrait.html img="Lab Data Flow.jpg" caption="Figure 1: FHIR to CDISC Laboratory Data Flow" %}

The following items are **out-of-scope** for this implementation guide:
* Mapping individual laboratory test codes between coding systems (e.g., internal codes to LOINC) 
* Site data preparation and transformation, which is relevant to clinical research as a whole (broader than laboratory data).  Examples include: setting up the site FHIR server or defining credentials and security for accessing data from a site FHIR server
* Providing instructions for FHIR server permissions
* Implementation of patient data protection by the site

<br />

###  Purpose and Goals of the Project

The purpose of the FHIR to CDISC Laboratory Data Mapping project is to provide organizations with information on consuming data that have been supplied in a FHIR format, and transforming the data into the CDISC standards that are required for research sponsors. The project included the following deliverables:


#### Clinical Research Laboratory Data Narrative
Narratives, also known as scenarios, provide insight and context around the domain being discussed. By walking the reader through a fictitious example, the narrative highlights concepts important for the mapping and modeling work, and provides details for the creation of the test data set.

#### Clinical Research Laboratory Domain Model
The domain model provides a graphic representation of the relevant FHIR resources, attributes, and associations.  An broader clinical research domain model is available as part of the Biomedical Research Integrated Domain Group (BRIDG) deliverables.  The BRIDG model is supported by the HL7 BR&R working group, as its domain information model, and provides the semantic foundation to artifacts developed by BR&R.  The BRIDG model concepts, definitions, and relationships are leveraged in describing domains.  For more information, please see the BRIDG model web site [here](https://bridgmodel.nci.nih.gov/).

#### FHIR to CDISC Laboratory Data Mapping
The FHIR to CDISC mapping is useful for understanding how to relate FHIR resources and attributes to CDISC-compliant data structures and standards. To ensure a more comprehensive solution, FHIR resources are compared (mapped) to three existing CDISC standards that are used in clinical research laboratory data exchange: the CDISC LAB model, CDASH LB Domain variables, and SDTM LB variables.
To view the project deliverables, please see the [Downloads](downloads.html) page. 

<br />

### Project Data Standards

This section outlines the CDISC data standards that comprise the scope of data elements for this mapping guide.

| CDISC Standard  | Description of Standard |
:----------------|-------------------------------------------------------------:|
| Laboratory Data Model (LAB) | [LAB Description from CDISC](https://www.cdisc.org/standards/data-exchange/lab) |
| CDASH | [CDASH Description from CDISC](https://www.cdisc.org/standards/foundational/cdash) |
| SDTM | [SDTM Description from CDISC](https://www.cdisc.org/standards/foundational/sdtm) |

<br />

### Use Cases

The specification describes two use cases:

#### Use Case 1: FHIR to CDISC LAB XML

Use Case 1: FHIR to CDISC LAB XML
For the first use case, a clinical research sponsor organization that historically consumed data from a CDISC LAB XML format, receives a file in FHIR JSON/XML and converts it to the CDISC standard to allow ingestion of data into existing, CDISC-based systems. 

For the September 2018 Connectathon, transformation code was written to query a sandbox FHIR server and convert the resulting FHIR file into the CDISC LAB XML standard format. The code was written in Java and made available in GitHub. The FHIR to CDISC data mapping contains the path information that was used in the Java code. Source code, sample data, and mappings are available on the [Downloads](downloads.html) page.

#### Use Case 2: FHIR to CDISC CDASH or SDTM

In the second use case, a clinical research sponsor organization that historically consumed data in the CDISC CDASH format, receives a file in FHIR JSON/XML and converts it to the CDISC standard to allow ingestion of data into existing, CDISC-based systems.  The data are also converted to SDTM format, for reporting purposes. 

Since implementations of CDASH and SDTM data stores may vary by sponsor, please see the FHIR to CDISC data mapping document for field level equivalencies to use in processing FHIR lab data files. The data mapping is available on the [Downloads](downloads.html) page.  

<br />

### BRIDG
The Biomedical Research Integrated Domain Group (BRIDG) Model is a collaborative effort that includes stakeholders from the Clinical Data Interchange Standards Consortium (CDISC), the HL7 BRIDG Working Group, the International Organization for Standardization (ISO), the US National Cancer Institute (NCI), and the US Food and Drug Administration (FDA).  The goal of the BRIDG Model is to serve as a semantic model for basic, pre-clinical, clinical, and translational research and the associated regulatory artifacts.  [https://bridgmodel.nci.nih.gov/](https://bridgmodel.nci.nih.gov/)  

* Click on “Browse BRIDG Model 5.3.1” button towards the bottom of the screen.
* This will open a new webpage with BRIDG model in html version
* Click on package called – CDISC Views
* Click on diagram called “CDISC Lab Model v 1.0.1 (diagram will open)
* Click on “Download CDSIC Lab Model v 1.0.1 meta data model”
* You will be able to download the Excel report.  

<br />

### Dependencies
This implementation guide relies on the following specification:
* **[FHIR R4]({{site.data.fhir.path}})** - The 'current' official version of FHIR as of the time this implementation guide was published.  

This implementation guide defines additional constraints and usage expectations above and beyond the information found in the base specifications.

<br/>

---
title: CDISC Lab Semantics in FHIR Implementation Guide
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

The purpose of the FHIR to CDISC Laboratory Data Mapping project is to provide organizations with information on consuming data that have been supplied in a FHIR format, and tranforming the data into the CDISC standards that are required for research sponsors. 

<br />

###  CDL Project Data Standards

This section outlines the CDISC data standards that comprise the scope of data elements for this mapping guide.

| CDISC Standard  | Description of Standard |
:----------------|-------------------------------------------------------------:|
| Laboratory Data Model (LAB) | [LAB Description from CDISC](https://www.cdisc.org/standards/data-exchange/lab) |
| CDASH | [CDASH Description from CDISC](https://www.cdisc.org/standards/foundational/cdash) |
| SDTM | [SDTM Description from CDISC](https://www.cdisc.org/standards/foundational/sdtm) |

<br />

### Use Cases

The specification describes two use cases:
1. Sponsor converts FHIR JSON/XML file to CDISC LAB XML standard for consumption by Sponsor systems
1. Sponsor converts FHIR JSON/XML file to CDISC  CDASH or SDTM standard for consumption by Sponsor systems

<br />

### Dependencies
This implementation guide relies on the following specification:
* **[FHIR R4]({{site.data.fhir.path}})** - The 'current' official version of FHIR as of the time this implementation guide was published.  

This implementation guide defines additional constraints and usage expectations above and beyond the information found in these base specifications.

<br/>

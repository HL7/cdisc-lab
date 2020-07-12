---
title: Clinical Research Sponsor Laboratory Semantics in FHIR Implementation Guide
layout: default
active: home
---


<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}


<!-- end TOC -->


###  Introduction

Laboratory data play a key role in enabling sponsors and sites to monitor the safety and efficacy of treatment drugs administered to patients within a clinical trial.  Historically, lab specimens were collected and/or processed by a central laboratory.  To streamline this process and provide convenience to patients, many sites are offering laboratory services on-premises (aka local labs) for collection and processing of biological specimens. 

The use of local labs, where each lab may have distinct processes and data collection systems, introduces the need for a standardized structure for the exchange of laboratory data.  Without standard guidance to utilize in data transfer, data are inconsistently exchanged, in a variety of formats, increasing the burden on both the site and the research sponsor.  This may increase cost, complexity, and time lines for clinical trials.  FHIR provides an effective standard for sites and sponsors to utilize in exchanging clinical research laboratory data.  The end-to-end process includes site data storage, site data preparation/transformation, production of FHIR format files, transformation from FHIR to CDISC laboratory data standards, and consumption of data by sponsor systems. The diagram below illustrates this process at a high level. 

This implementation guide focuses on mapping laboratory data from FHIR to CDISC (See #4 below).

{% include img-portrait.html img="Lab Data Flow.jpg" caption="Figure 1: FHIR to CDISC Laboratory Data Flow" %}

The next section provides a road map for the reader to walk through the implementation guide.


###  Guidance to the readers

The following table will provide a road map to the reader to follow and absorb the content of the implementation guide.

| Topic to Read  | What it Contains and its relationship to the CDL IG | Where can I find the content? |
|:---------------|:------------------------------------------------|-------------------------------:|
| Overview | The artifact provides background on the FHIR to CDISC Laboratory Data Mapping project.| [Overview](overview.html)|
| Mappings and Profiles | The artifact defines the mappings, profiles, and extensions that make up the CDL FHIR IG.| [Mappings and Profiles](mappingsandprofiles.html)|
| Terminology | The artifact defines the required terminology for entities and variables within the CDL mapping.|[Terminology](terminology.html)|
| Capability Statements | The artifact defines the various capability statements (implementation requirements) for the CDL FHIR IG.| [Capability Statements](capstatements.html)|
| Implementation Guidance | The artifact contains guidance and examples that will help implementers of CDL FHIR IG.| [Implementation Guidance](guidance.html)|
| Dowloads | The artifact contains downloadable copies of the IG and mappings. | [Downloads](downloads.html)|
| History | The artifact contains a history of releases to the CDL IG. | [History](history.html)|

<br/>

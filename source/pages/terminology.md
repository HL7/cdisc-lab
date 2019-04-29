---
title: Vocabulary for the IG
layout: default
active: terminology
---

<!-- TOC  the css styling for this is \pages\assets\css\project.css under 'markdown-toc'-->

* Do not remove this line (it will not be displayed)
{:toc}


<!-- end TOC -->

#### Vocabulary Bindings

CDISC LB Domain Variable bindings are provided for situations where the site has agreed to provide CDASH or SDTM compliant content via FHIR, but the FHIR value set does not match CDISC controlled vocabulary.  

If the FHIR value set binding strength is:
1. Required, a FHIR to CDISC translation is provided
1. Extensible, and CDISC controlled vocabulary has terms that are not in the FHIR value set, use the CDISC controlled vocabulary
1. Preferred, use the CDISC controlled vocabulary 
1. Example, use the CDISC controlled vocabulary

The following LB Domain variables require translations or CDISC bindings:
* Fasting Status (CDASH and SDTM variable LBFAST) requires translation by the consumer, due to the required binding to FHIR terminology.  Translate 'F' to 'Y', 'NF' to 'N', and 'NG' to 'U'.
* Test Status (CDASH and SDTM variable LBSTAT) requires translation by the consumer, due to the required binding to FHIR terminology.  Translate 'Not Performed' to 'NOT DONE', 'Cancelled' to 'NOT DONE', and 'Completed' to a &lt;blank&gt;.
* Specimen Condition (CDASH variable LBSPCCND) is an extensible value set and does not contain all values for the CDISC controlled vocabulary set.  Bind to [NCI Specimen Condition](https://ncit.nci.nih.gov/ncitbrowser/ConceptReport.jsp?dictionary=NCI_Thesaurus&ns=ncit&code=C78733) for specimen condition terminology.
* Specimen Type (CDASH and SDTM variable LBSPEC) is an example value set.  Bind to [NCI Specimen Type](https://ncit.nci.nih.gov/ncitbrowser/ConceptReport.jsp?dictionary=NCI_Thesaurus&ns=ncit&code=C78734) for specimen type terminology. 
* Body Position during Specimen Collection (SDTM variable LBPOS) does not have a binding to a value set.  Bind to [NCI Body Position](https://ncit.nci.nih.gov/ncitbrowser/ConceptReport.jsp?dictionary=NCI_Thesaurus&ns=ncit&code=C71148) for body position terminology.
* Observation Code (SDTM variable LBTESTCD) is an example value set.  Bind to [NCI Lab Test Code](https://ncit.nci.nih.gov/ncitbrowser/ConceptReport.jsp?dictionary=NCI_Thesaurus&ns=ncit&code=C65047) for lab test code terminology.
* Observation Code (SDTM variable LBTEST) is an example value set.  Bind to [NCI Lab Test Name](https://ncit.nci.nih.gov/ncitbrowser/ConceptReport.jsp?dictionary=NCI_Thesaurus&ns=ncit&code=C67154) for lab test code terminology. 
* Observation Interpretation (SDTM variable LBNRIND) is an extensible value set.  Bind to [NCI Reference Range](https://ncit.nci.nih.gov/ncitbrowser/ConceptReport.jsp?dictionary=NCI_Thesaurus&ns=ncit&code=C78736) for reference range indicator terminology.
* Observation Units (SDTM variable LBORRESU) does not have binding to a value set.  Bind to [NCI UOM](https://ncit.nci.nih.gov/ncitbrowser/ConceptReport.jsp?dictionary=NCI_Thesaurus&ns=ncit&code=C71620) for unit of measure terminology. 
* Observation Method (SDTM variable LBMETHOD) is an example value set.  Bind to [NCI Method](https://ncit.nci.nih.gov/ncitbrowser/ConceptReport.jsp?dictionary=NCI_Thesaurus&ns=ncit&code=C85492) for method terminology. 
* Specimen Anatomical Location (SDTM variable LBLOC) is an example value set.  Bind to [NCI Location](https://ncit.nci.nih.gov/ncitbrowser/ConceptReport.jsp?dictionary=NCI_Thesaurus&ns=ncit&code=C74456) for location terminology.

<br/>

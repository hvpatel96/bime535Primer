---
layout: page
title: "CDS and CPOE"
---
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega@4"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-lite@2.6.0"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-embed@3"></script>
<div id="vis"></div>
<script type="text/javascript">
	var spec = {
	  "config": {"view": {"width": 400, "height": 300}},
	  "data": {"url": "pubs.json", "format": {"type": "json"}},
	  "mark": {"type": "line", "point": true},
	  "encoding": {
	    "href": {"type": "nominal", "field": "url"},
	    "tooltip": {"type": "quantitative", "field": "Number of publications"},
	    "x": {"type": "ordinal", "field": "Year"},
	    "y": {"type": "quantitative", "field": "Number of publications"}
	  },
	  "title": "Pubmed Central results for \"decision support\"",
	  "$schema": "https://vega.github.io/schema/vega-lite/v2.6.0.json"
	}
	var opt = {"renderer": "canvas", "actions": false};  /* Options for the embedding */
	vegaEmbed("#vis", spec, opt);
</script>

# What is CPOE and how does it relate to CDS?

A Computerized Provider Order Entry (CPOE) is a system in which clinicians place medical orders electronically and that order is directly transmitted to the recipient. It was conceived primarily for providing safety to medication orders and has now expanded its’ use for the ordering of tests, procedures and other consultations. Although it has benefit clinicians and patients, CPOE also has its’ own risks and unintended consequences of digitalizing a health care process especially if the system is poorly designed or has poor usability. Some of the unintended consequences can be the disruption of the clinician workflow, increasing the clinicians’ cognitive load, overdependence on technology, generation of new types of errors, alert fatigue, unfavorable changes in communication patterns between clinicians and patients, among others.
 
Historically, prescribing and administrating medications involves the following steps:
 
1. Ordering: Where the clinicians choose the appropriate medication, dose, and administration frequency.
2. Transcribing: Where the prescription must be read and understood by the recipient, especially if it is handwritten.
3. Dispensing: Where the pharmacist checks for allergies and drug-drug interactions before releasing the appropriate quantity of the medication.
4. Administration: Where the correct patient must receive the correct medication in the correct dosage at the right time. This step is usually done by nurses.
 
Similar steps are followed for prescribing laboratory or imaging orders. In all of these cases, the majority of errors occur in the ordering and transcribing steps due to a variety of reasons like poor handwriting, ambiguous abbreviations, incompleteness, or lack of knowledge. Using a CPOE prevents those errors by standardizing providers’ orders in a legible a complete format. In addition, it provides EHR integration and improves efficiency by saving time in order entry and retrieval. Since CPOE technology usually includes built-in CDS tools, it can check for a drug-drug interaction, allergies, and make suggestions for values of drug dosages, routes of administration and frequencies. Sophisticated CDS tools can even prevent omission of certain tests or procedures for a certain condition. Even though CPOE adds several benefits to the organization, it cannot prevent errors that occur during dispensing or administration stages or when clinicians bypass safety steps for entering and processing unsafe orders.

# What is the history of CDS?

Late-2000s brought the “To Err is Human” report (To Err Is Human, 2000), a publication from the Institute of Medicine (IOM) that 17 percent of deaths in the USA were found to be related to diagnostic errors and 10 percent to drug-related errors (“A Historical Look At The Evolution Of Clinical Decision Support,” n.d.). Additionally, the report shows the alarming statistic of 70 percent of patients’ adverse events were thought to be preventable. All of these errors, seen frivolously, cost a lot of money and time that could be invested in treating other patients.
 
At the same time, the Internet explosion brought technological advances and a knowledge explosion for retrieving high-quality information for patient or context-specific for delivering better care. The expansion of medical knowledge got to a point where no clinician was able to analyze findings and integrate it with current knowledge at the bedside for coming up with the correct diagnosis. It is not that the clinical judgment has become obsolete but that no-one was able to keep up with all the entire medical knowledge in their head. Major advances in communications, the eventual spread of the EHRs, breakthroughs in the ‘-omics’ area and the new products for treatment or prevention have uncovered enormous potential important findings that needed to be incorporated into the medical prognosis. It was the vast amount of new information made the necessity of creating a system that will help to cope with all the new information (Greenes, 2014).
 
The idea was not new, Luger et al. (2005) had already traced the early literature that talked about to what extent human intelligence and reasoning ability could be understood enough to be contained in a computer. He included the study of self-organizing systems, cybernetics and statistical methodology that allowed extraction and pattern recognition for imaging. With that precedent, the IOM follow-up with a report called “Bridging the Quality Chasm” that pointed out the frequency of nonoptimal patient care, variations in practice that resulted in inefficiencies, dangers, and inequalities. That same reported recognized the importance of IT systems centrality working with a CDS system for detecting inappropriate practices and monitoring and provide feedback on existing practices for reducing errors and achieve quality of care.
 
In recent years, stimulus for improving EHR adoption in the US and its’ “Meaningful Use” (MU), the Health Information Exchange (HIE), the HITECH act (2009) and other health standards helped to support the CDS use because it can be useful in overcoming fragmentation problems, reducing the pressure from doctors and decreasing the time needed to make a medical decision. CDS would also be useful in identifying opportunities for intervention, education or monitoring with the advantage of making the workflow and team coordination easier. 


References

A Historical Look At The Evolution Of Clinical Decision Support. (n.d.). Retrieved May 12, 2019, from https://www.healthitoutcomes.com/doc/a-historical-look-at-the-evolution-of-clinical-decision-support-0001
Greenes, R. A. (2014). A Brief History of Clinical Decision Support. In Clinical Decision Support (pp. 49–109). Elsevier. https://doi.org/10.1016/B978-0-12-398476-0.00002-6
To Err Is Human. (2000). Washington, D.C.: National Academies Press. https://doi.org/10.17226/9728
U.S. Department of Health and Human Services. (n.d.). Computerized Provider Order Entry. Retrieved from https://psnet.ahrq.gov/primers/primer/6/computerized-provider-order-entry
What is computerized provider order entry? | HealthIT.gov. (n.d.). Retrieved May 19, 2019, from https://www.healthit.gov/faq/what-computerized-provider-order-entry
Luger, G. F. (2005). Artificial intelligence: structures and strategies for complex problem solving. Pearson education.

# Additional questions:
What is Clinical Decision Support?
What are some current implementations of CDS?
Many Clinical Decision Support systems are currently in use across the country and the world. 
What successes and failures have current implementations seen?
What are the important issues, benefits, and lessons learned?
What are the challenges related to socio-cultural factors?


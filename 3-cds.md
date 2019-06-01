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

# What is CDS?

Clinical Decision Support (CDS) encompasses all tools, software and hardware, that provide clinicians, patients, and related healthcare individuals with intelligently curated knowledge and patient-specific information in order to improve the quality of care and overall well-being of the patient (HealthIT.gov). CDS often takes the form of computerized alerts, clinical guidelines, condition-specific knowledge sets, personalized patient reports, and diagnostic support. According to the AHRQ, there exist five “rights” of CDS that can be used as a framework for the development and assessment of clinical decision support systems (CDSS). 
<br/>
<br/>
> > “The CDS Five Rights model states that we can achieve CDS-supported improvements in desired healthcare outcomes if we communicate:
> > 1. The right information: evidence-based, suitable to guide action, pertinent to the circumstance
> > 2. To the right person: considering all members of the care team, including clinicians, patients, and their caretakers
> > 3. In the right CDS intervention format: such as an alert, order set, or reference information to answer a clinical question
> > 4. Through the right channel: for example, a clinical information system (CIS) such as an electronic medical record (EMR), personal health record (PHR), or a more general channel such as the Internet or a mobile device
> > 5. At the right time in workflow: for example, at time of decision/action/need"

<br/>
<br/>
When reading through the remainder of this chapter, keep this framework in mind and try to organize the information presented into the different components listed above. Some questions to consider are: (Try to think of others that relate back to the framework!)
* Did the system utilize the right information?
* Was the information delivered to the right person and during the right time in the care process?
* Was the intervention format appropriate? Can it be improved by integrating it within a better channel?

# What is the history of CDS?
The late-2000s brought the “To Err is Human” report (To Err Is Human, 2000), a publication from the Institute of Medicine (IOM) which reported that 17% of deaths in the US were found to be related to diagnostic errors, and 10% to drug-related errors (“A Historical Look At The Evolution Of Clinical Decision Support,” n.d.). Additionally, the report includes the alarming statistic that 70% of patients’ adverse events were thought to be preventable. All of these errors result in lost money and time that could be invested in treating other patients.
 
At the same time, the Internet explosion brought technological advances in retrieving high-quality information for patient or context-specific for delivering better care. The expansion of medical knowledge got to a point where no clinician was able to analyze findings and integrate it with current knowledge at the bedside for coming up with the correct diagnosis. It is not that the clinical judgment has become obsolete but that no-one was able to keep up with all the entire medical knowledge in their head. Major advances in communications, the eventual spread of the EHRs, breakthroughs in the ‘-omics’ area and the new products for treatment or prevention have uncovered enormous potential important findings that needed to be incorporated into the medical prognosis. It was the vast amount of new information made the necessity of creating a system that will help to cope with all the new information (Greenes, 2014).
 
The idea was not new, Luger et al. (2005) had already traced the early literature that talked about to what extent human intelligence and reasoning ability could be understood enough to be contained in a computer. He included the study of self-organizing systems, cybernetics and statistical methodology that allowed extraction and pattern recognition for imaging. With that precedent, the IOM follow-up with a report called “Bridging the Quality Chasm” that pointed out the frequency of nonoptimal patient care, variations in practice that resulted in inefficiencies, dangers, and inequalities. That same reported recognized the importance of IT systems centrality working with a CDS system for detecting inappropriate practices and monitoring and provide feedback on existing practices for reducing errors and achieve quality of care.
 
In recent years, stimulus for improving EHR adoption in the US and its’ “Meaningful Use” (MU), the Health Information Exchange (HIE), the HITECH act (2009) and other health standards helped to support the CDS use because it can be useful in overcoming fragmentation problems, reducing the pressure from doctors and decreasing the time needed to make a medical decision. CDS would also be useful in identifying opportunities for intervention, education or monitoring with the advantage of making the workflow and team coordination easier. 

# What are some current implementations of CDS?

Current clinical decision support systems come in a range of variations, such as built into commercial EHR systems, sold separately by CDS companies, or as systems developed and maintained by universities and hospitals themselves. 

Modern EHR systems come with many guard rails in place. Dose alerts are one example. The system may show dose alerts when clinicians are about to order medications that have contraindications for a patient (e.g. the patient is allergic to it) or have a dose that looks incorrect, overdosing or underdosing the patient. Later, when a nurse or other clinician prepares to give the ordered medication at the patient bedside, he or she first scans a barcode attached to the patient wrist band and then the medication through a barcode printed on the medication packaging. This process, called bar coded medication administration (BCMA), allows the system to verify that the correct medication is being given to the correct patient by retrieving the record belonging to the scanned patient and confirming the validity of the scanned medication for that patient. Drugs often sound similar and packages or pills often look similar, and this process can prevent clinicians from giving incorrect medications (The Leapfrog Group, 2018).

A second avenue through which clinical decision support is commonly given to healthcare professionals today is through third party decision support vendors, such as Medicalis and National Decision Support Company. These vendors often integrate with the EHR system directly, allowing the software to show custom alerts to users in response to specified triggers under specified conditions. Sometimes called Best Practice alerts, these often implement clinical guidelines and even maintain their own databases of information such as drug-drug interactions. An example of such an alert might be a suggestion that an overweight patient receive weight loss counseling a nutritionist. The inherent tradeoff with purchasing a library of clinical decision support specifications from the perspective of a healthcare organization is that some alerts may not be relevant to the particular patient community, or may be too broad or too specific for the particular healthcare organization’s preferences. Thus, hospitals still have to shop around for CDS services that meet their specific needs, and subsequently customize the system further, which is cost intensive (Rath, 2016). 

Healthcare organizations may also define their own Best Practice alerts using the same set of triggers and specification options. While this is more resource intensive than buying a ready-made library of such specifications from a CDS vendor, alerts can be fully customized; additionally, for some alerts, healthcare organizations will have no choice but to create them themselves, e.g. for hospital-specific initiatives.

Currently, however, each CDS vendor must work with the EHR vendors in order to integrate with their various software systems (Rath, 2016). CDS Hooks is a current effort by HL7 to standardize the process of triggering events from the EHR and allowing third party systems to respond to such events with clinical decision support information. This would allow the clinical decision support vendor market to diversify and reduce the barriers to implementing clinical decision support (HL7 CDS Hooks). While the tool is not fully mature yet, it is freely available for exploration on Github (CDS Hooks Github) and numerous tutorials are available, including one created by students in the Biomedical Informatics department at the University of Washington (UW FHIR CDS Hook Tutorial).

A more recently emerging form of CDS is predictive modeling of patients’ risk for adverse events. For this purpose, machine learning methods have been applied to build predictive models capable of determining patient risk in real time. Through the development of data-driven predictive models and their implementation in clinical settings, nurses, doctors, and other healthcare professionals can be alerted in real time if the model detects patients at risk for poor outcomes. Early detection can help with patient morbidity, mortality, and health care costs. Recently, several clinical challenges have been extensively modeled by such predictive models; for example, sepsis risk, 30-day hospital readmission risk, and appointment no-shows (Bresnick, 2018). Simple risk scores, like SIRS and SOFA for early detection of sepsis, exist and are often used in an attempt to identify patients at high risk, so interventions can be targeted early and effectively. These risk scores are often outperformed by machine learning models (e.g. Desautels, 2016); however, their parsimony may be desirable in some settings: the qSOFA score allows classification of patients merely by combining patient mental status, respiratory rate, and blood pressure (Burkhardt, 2018).

# What is CPOE and how does it relate to CDS?

A Computerized Provider Order Entry (CPOE) is a system in which clinicians place medical orders electronically and that order is directly transmitted to the recipient. It was conceived primarily for providing safety to medication orders and has now expanded its’ use for the ordering of tests, procedures and other consultations. Although it has benefit clinicians and patients, CPOE also has its’ own risks and unintended consequences of digitalizing a health care process especially if the system is poorly designed or has poor usability. Some of the unintended consequences can be the disruption of the clinician workflow, increasing the clinicians’ cognitive load, overdependence on technology, generation of new types of errors, alert fatigue, unfavorable changes in communication patterns between clinicians and patients, among others.
 
Historically, prescribing and administrating medications involves the following steps:
 
1. Ordering: Where the clinicians choose the appropriate medication, dose, and administration frequency.
2. Transcribing: Where the prescription must be read and understood by the recipient, especially if it is handwritten.
3. Dispensing: Where the pharmacist checks for allergies and drug-drug interactions before releasing the appropriate quantity of the medication.
4. Administering: Where the correct patient must receive the correct medication in the correct dosage at the right time. This step is usually done by nurses.
 
Similar steps are followed for prescribing laboratory or imaging orders. In all of these cases, the majority of errors occur in the ordering and transcribing steps due to a variety of reasons like poor handwriting, ambiguous abbreviations, incompleteness, or lack of knowledge. Using a CPOE prevents those errors by standardizing providers’ orders in a legible a complete format. In addition, it provides EHR integration and improves efficiency by saving time in order entry and retrieval. Since CPOE technology usually includes built-in CDS tools, it can check for a drug-drug interaction, allergies, and make suggestions for values of drug dosages, routes of administration and frequencies. Sophisticated CDS tools can even prevent omission of certain tests or procedures for a certain condition. Even though CPOE adds several benefits to the organization, it cannot prevent errors that occur during dispensing or administration stages or when clinicians bypass safety steps for entering and processing unsafe orders.



# References

A Historical Look At The Evolution Of Clinical Decision Support. (n.d.). Retrieved May 12, 2019, from https://www.healthitoutcomes.com/doc/a-historical-look-at-the-evolution-of-clinical-decision-support-0001

Greenes, R. A. (2014). A Brief History of Clinical Decision Support. In Clinical Decision Support (pp. 49–109). Elsevier. https://doi.org/10.1016/B978-0-12-398476-0.00002-6

To Err Is Human. (2000). Washington, D.C.: National Academies Press. https://doi.org/10.17226/9728
U.S. Department of Health and Human Services. (n.d.). Computerized Provider Order Entry. Retrieved from https://psnet.ahrq.gov/primers/primer/6/computerized-provider-order-entry

What is computerized provider order entry? \| HealthIT.gov. (n.d.). Retrieved May 19, 2019, from https://www.healthit.gov/faq/what-computerized-provider-order-entry

Luger, G. F. (2005). Artificial intelligence: structures and strategies for complex problem solving. Pearson education.

The Leapfrog Group. (2018) New Report on Bar Code Medication Administration Finds Virtually All Hospitals Have the Technology, but Lack Requirements to Deploy it Effectively. 

HL7. CDS Hooks. Retrieved from https://cds-hooks.hl7.org/

Rath, D. (2016, September 21). What Is CDS Hooks? An Interview with Josh Mandel About FHIR and Clinical Decision Support. Retrieved from https://www.hcinnovationgroup.com/interoperability-hie/blog/13027466/what-is-cds-hooks-an-interview-with-josh-mandel-about-fhir-and-clinical-decision-support

CDS Hooks. Github. Available at https://github.com/cds-hooks

UW FHIR CDS Hook Tutorial. Github. Available at https://github.com/uw-fhir/CDS-Hooks-Tutorial/blob/master/tutorial.md

Bresnick, J. (2018) 10 High-Value Use Cases for Predictive Analytics in Healthcare. Health IT Analytics.

Desautels, T., Calvert, J., Hoffman, J., Jay, M., Kerem, Y., Shieh, L., . . . Das, R. (2016). Prediction of Sepsis in the Intensive Care Unit With Minimal Electronic Health Record Data: A Machine Learning Approach. JMIR Medical Informatics, 4(3), E28.

Payne, T. H. (2018). EHR-related alert fatigue: minimal progress to date, but much more can be done. BMJ Quality & Safety. https://doi.org/10.1136/bmjqs-2017-007737

Rehr, C. A., Wong, A., Seger, D. L., & Bates, D. W. (2018). Determining Inappropriate Medication Alerts from "Inaccurate Warning" Overrides in the Intensive Care Unit. Applied clinical informatics, 9(2), 268–274. doi:10.1055/s-0038-1642608

Adapted from Burkhardt, Hannah. (2018) Machine Learning and Biomedical Informatics. BIME 530.


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
 
At the same time, the Internet explosion brought technological advances in retrieving high-quality, context-specific information for delivering better care to patients. The expansion of medical knowledge on the Internet reached a point where no single clinician's knowledge could compete with the flood of information at their fingertips, and it became unfeasible to integrate all medical knowledge on a topic with findings at the bedside. Major advances in communication technologies, widespread adoption of EHRs, breakthroughs in the ‘-omics’ disciplines, and new products for treatment or prevention have uncovered important medical findings that should be incorporated into routine medical care. This vast amount of new information has necessitated the creation of computer-based systems that can aid in the process of supplementing physicians' knowledge base and medical judgment with a wider knowledge base (Greenes, 2014).
 
However, the integration of CDS into routine healthcare is not a brand new field. For example, Luger et al. (2005) reviews early literature on the computability of human intelligence and reasoning abilities. It includes studies on self-organizing systems, cybernetics and statistical methodologies that specialize in concept extraction and pattern recognition for imaging data. With that precedent, the IOM followed up with a report called “Bridging the Quality Chasm” that pointed out frequent patterns of suboptimal patient care, variations in practice that result in inefficiencies, dangers to patients, and inequalities. That same report recognized the importance of integrating IT systems with CDS systems that detect inappropriate practices, and provide feedback on existing practices that could help reduce medical error and achieve a higher quality of care.
 
In recent years, the prevalence of the financial stimulus for improving EHR adoption in the US, the “Meaningful Use” (MU) clause, Health Information Exchange (HIE), the HITECH act (2009) and health information standards have helped support the emergence of CDS by highlighting its utility in overcoming fragmentation problems, relieving pressure on doctors, and decreasing the time needed to make crticial medical decisions. CDS may also be useful in identifying opportunities for team workflow coordination in implementing interventions, education and patient monitoring tasks. 

# What are some current implementations of CDS?

Current clinical decision support systems come in a range of variations, such as built into commercial EHR systems, sold separately by CDS companies, or as systems developed and maintained by universities and hospitals themselves. 

Modern EHR systems come with many guard rails in place. Dose alerts are one example. The system may show dose alerts when clinicians are about to order medications that have contraindications for a patient (e.g. the patient is allergic to the medication), or input a dose that looks incorrect and may lead to overdosing or underdosing the patient. Later, when a nurse or other clinician prepares to give the ordered medication at the patient's bedside, he or she first scans a barcode attached to the patient's wrist, as well as a barcode printed on the medication packaging. This process, called bar coded medication administration (BCMA), allows the system to verify that the correct medication is being given to the correct patient by retrieving the record belonging to the scanned patient and confirming the validity of the scanned medication for that patient. Drugs often sound similar and packages or pills often look similar, and this process can prevent clinicians from giving incorrect medications (The Leapfrog Group, 2018).

A second avenue through which clinical decision support tools are obtained by healthcare providers today is through third party decision support vendors, such as Medicalis and the National Decision Support Company. These vendors often integrate their CDS software with the EHR system directly, allowing the software to show custom alerts to users in response to specified triggers under specified conditions. Sometimes called Best Practice alerts, these warnings implement clinical guidelines and even search their own medical databases for information like drug-drug interactions. An example of such an alert might be a suggestion that an overweight patient schedule an appointment with a nutritionist who specializes in weight loss counseling. From the perspective of the healthcare organization, an inherent tradeoff of purchasing a library of clinical decision support specifications is that some alerts may not be relevant to the particular patient community, or may be too broad or too specific for the particular healthcare organization’s preferences. Thus, hospitals still have to shop around for CDS services that meet their specific needs and subsequently customize the system, which can be time consuming and cost intensive (Rath, 2016). 

Healthcare organizations may also define their own Best Practice alerts using self-defined sets of triggers and specification options. While this is more resource intensive than buying ready-made libraries of such specifications from a CDS vendor, alerts can be fully customized; additionally, for some alerts, healthcare organizations will have no choice but to create them themselves, e.g. for hospital-specific initiatives.

Currently, however, each CDS vendor must work with the EHR vendors in order to integrate with their own software systems (Rath, 2016). CDS Hooks is a current effort by HL7 to standardize the process of triggering events from the EHR and allowing third party systems to respond to such events with clinical decision support information. This would allow the clinical decision support vendor market to diversify and reduce the barriers to implementing a variety of clinical decision support tools (HL7 CDS Hooks). While the CDS Hooks tool is not fully mature yet, it is freely available for exploration on Github (CDS Hooks Github) and numerous tutorials are available, including one created by students in the Biomedical Informatics department at the University of Washington (UW FHIR CDS Hook Tutorial).

A more recently emerging form of CDS is predictive modeling of patients’ risk for adverse events. For this purpose, machine learning methods have been applied to build predictive models capable of determining patient risk in real time. Through the development of data-driven predictive models and their implementation in clinical settings, nurses, doctors, and other healthcare professionals can be alerted in real time if the model detects patients at risk for poor clinical outcomes. Early detection can help reduce patient morbidity, mortality, and health care costs. Recently, several clinical challenges have been extensively explored by such predictive models; for example, sepsis risk, 30-day hospital readmission risk, and appointment no-shows (Bresnick, 2018). Simple risk scores, like SIRS and SOFA for early detection of sepsis, exist and are often used in an attempt to identify patients at high risk, so interventions can be targeted early and effectively. These risk scores are often outperformed by machine learning models (e.g. Desautels, 2016); however, their parsimony may be desirable in some settings: the qSOFA score allows classification of patients merely by combining patient mental status, respiratory rate, and blood pressure (Burkhardt, 2018).

# What is CPOE and how does it relate to CDS?

Computerized Provider Order Entry (CPOE) is a system in which clinicians place medical orders electronically, and the order is directly transmitted to the recipient. It was conceived primarily for improving the safety of medication orders, but it is now also used to order lab tests and medical procedures, and request specialized consultations. Although it has benefitted clinicians and patients, CPOE also carries its own risks and unintended consequences. Digitalizing any health care process runs the risk of creating products that are poorly designed and/or have poor usability. Some of the unintended consequences can include disrupting the clinician workflow, increasing the clinicians’ cognitive load, increasing physicians' overdependence on technology, generating of new types of errors, causing alert fatigue, and causing unfavorable changes in communication patterns between clinicians and patients, among others issues.
 
Historically, prescribing and administering medications involves the following steps:
 
1. Ordering: The clinicians choose the appropriate medication, dose, and administration frequency.
2. Transcribing: The prescription must be read and understood by the recipient (i.e. pharmacist), especially if it is handwritten.
3. Dispensing: The pharmacist checks for allergies and drug-drug interactions before releasing the appropriate quantity of the medication.
4. Administering: The correct patient must receive the correct medication in the correct dosage at the right time. This step is usually done by nurses.
 
Similar steps are followed for prescribing laboratory or imaging orders. In all of these cases, the majority of errors occur in the ordering and transcribing steps due to a variety of reasons, like poor handwriting, ambiguous abbreviations, incompleteness, or lack of medical knowledge. Using CPOE helps prevent those errors by standardizing providers’ orders in a legible and complete format. In addition, it promotes EHR integration and improves efficiency by saving time during order entry and retrieval tasks. Since CPOE technology usually includes built-in CDS tools, it can check for drug-drug interactions and patient allergies, and make suggestions for values of drug dosages, routes of administration and frequencies. Sophisticated CDS tools can even prevent omission of certain tests or procedures for a certain condition. Even though CPOE provides several benefits to the organization, it cannot prevent errors that occur during actual dispensing or administration stages, or prevent clinicians from intentionally bypassing safety alerts.

# What are some important issues, benefits, and lessons learned from CDS?

A major problem with any kind of clinical decision support is that of alert fatigue. Clinicians may receive over 100 alerts in a single work day (Payne, 2018). Many of these alerts are not applicable for various reasons - e.g. a pregnancy warning may not be applicable to a male patient, or a drug sensitivity warning may show repeatedly even after the potential sensitivity has been determined to be a non-issue. Being exposed to such inaccurate alerts repeatedly may erode healthcare professionals’ trust in CDS alerts, which in turn may cause them to disregard applicable high impact alerts later on. Efforts have been made to identify why certain alerts are dismissed without being addressed, and whether or not the dismissal is appropriate; for example, Rehr et al. (2018) found that, while some alerts were being overridden inappropriately, there were also many appropriate overrides due to reasons such as prior tolerance and inaccurate ingredient matches.

Other challenges of clinical decision support systems include: incomplete medical knowledge bases, difficulties in converting evidence-derived information into a computable format, problems with project planning and management during the design and implementation phases of CDS integration, and financial disincentives justifying the use of CDS in smaller practices (AHRQ 2010). In regards to the first two challenges, the corpus of medical knowledge is a constantly evolving text with anecdotal rules of thumb mixed together with research-backed evidence and methodologies. One of the greatest challenges hindering the progression of CDS is the question of extracting useful and up to date information quickly and providing that to the user in a readable format. Some CDS systems are built on existing knowledge bases and utilize ontologies (or established terminologies) for organization, but even these change from year to year and must be updated often to incorporate changes in medical thought and research. On top of that, not all knowledge is easily converted into code. Due to the probabilistic nature of diagnoses and medical interactions, it is often difficult to accurately represent information without sacrificing time, efficiency, and output readability.  Without a computable, “learning” knowledge base, it is difficult to build a truly adaptive CDS.

# What are some of the socio-cultural challenges of CDS implementation and acceptance?

Although the technical challenges of CDS may become less of a barrier to implementation as structured medical knowledge bases continue to evolve and as computerized data processing and interpretation techniques become more advanced, the human factors of healthcare will continue to influence whether these support systems will have their intended effects on clinical outcomes. Clinical decision-making is not solely based on a healthcare provider’s medical training, knowledge base or past medical experiences--in fact, it is very commonly influenced by non-clinical factors pertaining to the patient and/or the provider.

This phenomenon was reviewed in Hajjaj et al. (2010), which outlines just a handful of the various patient-specific factors (i.e. patient income level, race/ethnicity, gender, age, attitude, preferences, etc.) and physician-specific factors (i.e. personal characteristics, age, gender, workload, professional community, etc.) that affect clinical decision-making. Granted, several of these factors occupy a “fuzzy” space between the clinical and non-clinical realms, and factors like patient gender, age and preferences are often critical pieces of information to consider when making patient-centered clinical decisions. However, these factors begin to move beyond the purely evidence-based, clinical realm when they are framed in contexts that are not conducive to effective patient treatment. For example, patient gender would be an important factor to consider when ordering a mammogram for a patient, but a physician’s perception of how well a patient might adhere to a particular treatment regimen based on their gender would not be within the realm of evidence-based medicine. The Hajjaj et al. article acknowledges that the line between personalized evidence-based medicine and biased decision-making (whether conscious or unconscious) is quite fuzzy and complex, but this very complexity has significant implications for the role of CDS in the healthcare workflow.

Even if we could eventually assume that all alerts fired by CDS systems were 100% evidence-based and important to respond to, there is no guarantee that those alerts will be heeded by healthcare providers due to confounding factors other than medical knowledge or experience. This issue was demonstrated in practice by Bauer et al. (2016), who analyzed nearly 3 years-worth of data generated by the Child Health Improvement through Computer Automation (CHICA) CDS system. This system generates personalized physician reminders and discussion handouts for short pediatric office visits, and each of these reminders and suggested discussion points is referred to as a CDS “prompt.” Bauer et al. found that physicians responded to prompts significantly more often if the prompt was rated as “easy” to discuss, as determined by a group of 16 general pediatricians. They also found that several patient characteristics (i.e. age, race/ethnicity), guardian characteristics (i.e. preferred language) and clinician characteristics (i.e. gender) significantly influenced whether a clinician responded to the prompts or not. These results raise the question of whether these types of interventions can positively impact clinical care when applied across diverse patient and clinician populations, or whether CDS interventions must be accompanied by rigorous socio-cultural and bias recognition training in order to be effective.

However, it is also possible that CDS systems could help mitigate some of the non-clinical factors that influence clinical decision-making. In fact, many of the successes of recent CDS systems are attributed to encouraging physician adherence to evidence-based practice guidelines (Murphy 2014) which, as highlighted in the Hajjaj et al. review, are often complicated by non-clinical patient and clinician characteristics. The degree to which a clinician is willing and able to counteract their inherent biases and yield to the “objective” will of CDS systems is the ultimate determinant of whether these systems will significantly impact clinical care.




# References

Adapted from Burkhardt, Hannah. (2018) Machine Learning and Biomedical Informatics. BIME 530.

A Historical Look At The Evolution Of Clinical Decision Support. (n.d.). Retrieved May 12, 2019, from https://www.healthitoutcomes.com/doc/a-historical-look-at-the-evolution-of-clinical-decision-support-0001

Bauer, N.S. et al. (2016). Experience with decision support system and comfort with topic predict clinicians’ responses to alerts and reminders. 

Bresnick, J. (2018) 10 High-Value Use Cases for Predictive Analytics in Healthcare. Health IT Analytics.

CDS Hooks. Github. Available at https://github.com/cds-hooks

Desautels, T., Calvert, J., Hoffman, J., Jay, M., Kerem, Y., Shieh, L., . . . Das, R. (2016). Prediction of Sepsis in the Intensive Care Unit With Minimal Electronic Health Record Data: A Machine Learning Approach. JMIR Medical Informatics, 4(3), E28.

Greenes, R. A. (2014). A Brief History of Clinical Decision Support. In Clinical Decision Support (pp. 49–109). Elsevier. https://doi.org/10.1016/B978-0-12-398476-0.00002-6

Hajjaj, F.M. et al. (2010). Non-clinical influences on clinical decision decision-making: a major challenge to evidence-based practice. Journal of the Royal Society of Medicine, 103(5): 178-187. doi: 10.1258/jrsm.2010.100104

HL7. CDS Hooks. Retrieved from https://cds-hooks.hl7.org/

Luger, G. F. (2005). Artificial intelligence: structures and strategies for complex problem solving. Pearson education.

Murphy, E.V. (2014). Clinical Decision Support: Effectiveness in Improving Quality Processes and Clinical Outcomes and Factors That May Influence Success. Yale J Biol Med 87(2): 187-197.

Payne, T. H. (2018). EHR-related alert fatigue: minimal progress to date, but much more can be done. BMJ Quality & Safety. https://doi.org/10.1136/bmjqs-2017-007737

Rath, D. (2016, September 21). What Is CDS Hooks? An Interview with Josh Mandel About FHIR and Clinical Decision Support. Retrieved from https://www.hcinnovationgroup.com/interoperability-hie/blog/13027466/what-is-cds-hooks-an-interview-with-josh-mandel-about-fhir-and-clinical-decision-support

Rehr, C. A., Wong, A., Seger, D. L., & Bates, D. W. (2018). Determining Inappropriate Medication Alerts from "Inaccurate Warning" Overrides in the Intensive Care Unit. Applied clinical informatics, 9(2), 268–274. doi:10.1055/s-0038-1642608

The Leapfrog Group. (2018) New Report on Bar Code Medication Administration Finds Virtually All Hospitals Have the Technology, but Lack Requirements to Deploy it Effectively.

To Err Is Human. (2000). Washington, D.C.: National Academies Press. https://doi.org/10.17226/9728
U.S. Department of Health and Human Services. (n.d.). Computerized Provider Order Entry. Retrieved from https://psnet.ahrq.gov/primers/primer/6/computerized-provider-order-entry

UW FHIR CDS Hook Tutorial. Github. Available at https://github.com/uw-fhir/CDS-Hooks-Tutorial/blob/master/tutorial.md

What is computerized provider order entry? \| HealthIT.gov. (n.d.). Retrieved May 19, 2019, from https://www.healthit.gov/faq/what-computerized-provider-order-entry




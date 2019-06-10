---
layout: page
title: "AI in Medicine"
---

# What are some of the main differences between AI in healthcare in the 70s vs. now? 

# An AI “Success” Story: Predictive modeling for adverse events
Predictive analytics, specifically the application of machine learning to EHR data in order to predict future clinical events, has great potential to affect the efficient and effective delivery of healthcare as part of clinical decision support systems. By developing data-driven predictive models and making them available in clinical settings, researchers can enable EHRs to alert nurses, doctors, and other healthcare professionals in real time if patients are detected to be at risk for poor outcomes. Early detection can help with patient morbidity, mortality, and health care costs. Recently, several clinical challenges have been extensively modeled by such predictive models; for example, sepsis risk, 30-day hospital readmission risk, and appointment no-shows (Bresnick, 2018). Simple risk scores, like SIRS and SOFA for early detection of sepsis, exist and are often used in an attempt to identify patients at high risk, so interventions can be targeted early and effectively. However, these risk scores are often outperformed by machine learning models (e.g. Desautels, 2016).

Sepsis is one of the most expensive hospital conditions, and cost hospitals $23.7 billion in 2013 (Torio, 2016). Sepsis is an infection of the bloodstream that causes rapid deterioration and death within hours. With sepsis, every minute counts. Being able to focus interventions on patients with the highest sepsis risk can prevent many cases from developing, cutting down on that bottom line (Burkhardt, 2018). Additionally, once sepsis has developed, detecting it and starting treatment as soon as possible is critical. Recent reports have shown that predictive analytics for sepsis risk prediction has already reduced mortality due to sepsis. In 2018, for instance, sepsis mortality reported decreased by 18% at North Oaks Health System in Louisiana, thanks to a predictive analytics tool developed by researchers. According to the healthcare organizations Chief Health Information Officer, patients are receiving treatment 25% faster now once they develop sepsis (Kent, 2018).

Machine learning algorithms also have the ability to detect patterns long before humans would be able to discern them. A tool developed by Giannini et al. (2017) at the University of Pennsylvania Health System is able to identify patients who will develop sepsis a full 12 hours ahead of time (Bresnick, 2017). With a specificity of 98%, the model is also remarkable resistant to false positives.

Predictive modeling with EHR data for real-time clinical alerts is challenging for a host of reasons, but there have also been successes. The early detection of sepsis is just one example of a successful application in this realm. As the technology develops and adoption increases, we stand to see numerous benefits from predictively modeling other adverse events as well.

# What is “framing” in the context of AI, and how can framing (and alternate framing) be used to advance the field of AI in healthcare?

The field of AI is in part concerned with the ways in human knowledge, reasoning and problem-solving can be represented by machines, and this is often done by slicing various pieces of knowledge into representative parts. In his 1974 paper, “A Framework for Representing Knowledge,” cognitive scientist Marvin Minsky proposed a theory for representing data in AI systems using the concept of a frame, or a “data-structure for representing a stereotyped situation, like being in a certain kind of living room, or going to a child’s birthday party” (Minsky, 1974). The development of frames inherently involves assumptions about what humans assume to be true in certain situations, and linking frames into a frame system can therefore be used to represent a “stereotypical” situation. Framing has become one of the most commonly used data structures in the field of knowledge representation, and modern AI systems typically draw from such knowledge structures to respond to diverse situations (Reddy, 2018). 

In the field of healthcare AI, frame-based systems are commonly used to build clinical support tools like expert CDS systems (Moore & Loper, 2011), conversational agents (Laranjo et al. 2018), radiology decision support systems (Kahn, 1994) and anatomy/physiology representation systems. While many different frames can be compiled together to construct a relatively broad knowledge base, the limitations of frame-based systems in representing complex knowledge bases are apparent within the complex and ever-evolving field of medicine, despite the fact that such systems are used frequently in this field. For example, Noy et al. (2004) found that traditional approaches to frame-based knowledge representation are not sufficient for representing the highly relational and nuanced Digital Anatomist Foundational Model ontology, but that using a protocol for organizing many different frame systems into complex networks were largely sufficient for building the ontology.

However, frames are still finite chunks of information, even when linked to many other chunks of finite information. Each frame is still representative of a stereotypical piece of knowledge about a place, object or situation, and these types of systems therefore poorly represent non-stereotypical objects and situations. In the field of medicine, it is not unreasonable to expect that non-stereotypical situations will arise at a constant rate, given the unique anatomical, situational and historical characteristics that every single patient presents with. It is therefore critical to develop an awareness of the knowledge bases that medical AI systems interface with, and acknowledge their limitations in accuracy and nuance.

# The effects of human bias on AI implementations

One might like to think that computer algorithms do not judge or discriminate unfairly based on a patient’s race, gender, or other component of their identity. In many ways, this is true - computers are not humans and are therefore not subject to the unconscious biases that cause even the most well meaning individuals to make judgments based on race or other sensitive criteria. For example, a 2015 study (Haider et al. 2015) found that most surgical RNs consider themselves impartial to a person’s race, but that only 6.5% were truly indifferent, as measured by an implicit association test. Race and ethnicity are especially sensitive when it comes to healthcare, because decisions may have severe short or long term consequences. If a person is not given the appropriate treatment in a timely manner, they may be robbed of their ability to recover optimally. Racial disparities were subject to an extensive report by the National Academies of Medicine (formerly Institute of Medicine) in 2002, which reports that cardiologists often do not order the same catheterization procedures for black females that they would for black males, white males, or white females, even if they presented with the same symptoms (Institute of Medicine, 2002). Further, the full report states that “racial and ethnic disparities remain even after adjustment for socioeconomic differences and other healthcare access-related factors” (Institute of Medicine, 2003). 

If such differential treatment of people belonging to different ethnic groups is due to implicit biases by human beings, one might think that machine learning models may be able to help fix the problem. However, one important consideration must be kept in mind: machine learning algorithms will learn the patterns in the training data they are given. If training data are biased, a machine learning model must therefore becomes biased, too. For example, a machine learning algorithm may learn to recommend proper catheterization procedures to black women less often, simply on the basis of their race and gender.

A ubiquitous opportunity to introduce bias into machine learning data sets exists in digital medicine. Oftentimes, what we use as a gold standard in medicine is not guaranteed to be the truth, but rather it is the best expert opinion available to us. If a person decides what the ground truth label for a set of training data is, then these labels may be biased. If a machine learning model is subsequently trained on this data, it will learn to make decisions just like the human expert; and that means that the decisions may be unfair or otherwise biased. Only if the labels are objectively true, rather than an expert opinion, can we guarantee that no such human bias creeps in. 

In medicine, it is often infeasible or straight out impossible to know the truth. For example, it is basically impossible to determine whether ordering a catheterization procedure is truly the correct decision, for an African-American woman or a Caucasian woman, or anyone else. Thus, we sometimes have to define fairness in new ways. One way to do this is to strive to treat them both equally. However, this does not always result in equality of outcomes, equality of opportunity, or either. For an exploration of what it means for an algorithm to be fair, check out this visualization of an algorithm that decides whether to approve or deny loan applications: [Google Research: Attacking discriminatino in ML](http://research.google.com/bigpicture/attacking-discrimination-in-ml/)

# What are adversarial attacks, and what consequences do they have?

# References

Bresnick, J. (2018). 10 High-Value Use Cases for Predictive Analytics in Healthcare. Health IT Analytics.

Desautels, T., Calvert, J., Hoffman, J., Jay, M., Kerem, Y., Shieh, L., … Das, R. (2016). Prediction of Sepsis in the Intensive Care Unit With Minimal Electronic Health Record Data: A Machine Learning Approach. JMIR Medical Informatics, 4(3), e28. https://doi.org/10.2196/medinform.5909

Adapted from Burkhardt, Hannah. (2018) Machine Learning and Biomedical Informatics. BIME 530.

Torio, C. M., & Moore, B. J. (2016). National Inpatient Hospital Costs: The Most Expensive Conditions by Payer, 2013. https://doi.org/10.1377/hlthaff.2015.1194

Kent, J. (2018). Predictive Analytics, EHR Big Data Reduce Sepsis Mortality by 18%. Health IT Analytics.

Giannini, H. M., Chivers, C., Draugelis, M., Hanish, A., Fuchs, B., Donnelly, P., … Umscheid, C. (2017). Development and implementation of a machine-learning algorithm for early identification of sepsis in a multi-hospital academic healthcare system. Am J Respir Crit Care Med, 195, A7015. https://doi.org/10.1164/ajrccmconference.2017.D15

Bresnick, J. (2017). UPenn Uses Machine Learning, EHRs to Target Severe Sepsis.  Health IT Analytics.

Kahn, CE Jr. (1994). Artificial intelligence in radiology: decision support systems. Radiographics, 14(4): 849-861.DOI: 10.1148/radiographics.14.4.7938772

Laranjo, L. et al (2018). Conversational agents in healthcare: a systematic review. J Am Med Inform Assoc 25(9): 1248-1258. doi: 10.1093/jamia/ocy072

Minsky, M.L. A Framework for Representing Knowledge (1974). MIT-AI Laboratory Memo 306. Retrieved from https://courses.media.mit.edu/2004spring/mas966/Minsky%201974%20Framework%20for%20knowledge.pdf

Moore, M. & Loper, K.A. (2011). An Introduction to Clinical Decision Support Systems. Journal of Electronic Resources in Medical Libraries, 8(4): 348-366. DOI: 10.1080/15424065.2011.626345

Noy, N.F. et al. (2004). Pushing the envelope: challenges in a frame-based representation of human anatomy. Data & Knowledge Engineering, 48(3): 335-359. DOI: https://doi.org/10.1016/j.datak.2003.06.002

Reddy, S. (2018). Use of Artificial Intelligence in Healthcare Delivery. IntechOpen. DOI: 10.5772/intechopen.74714.

Institute of Medicine. (2002). Minorities More Likely to Receive Lower-Quality Health Care, Regardless of Income and Insurance Coverage. Retrieved from http://www8.nationalacademies.org/onpinews/newsitem.aspx?RecordID=10260

Institute of Medicine, (2003). Unequal Treatment: Confronting Racial and Ethnic Disparities in Health Care. Washington, DC: The National Academies Press. https://doi.org/10.17226/10260.
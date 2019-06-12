---
layout: page
title: "AI in Medicine"
---

# What are some of the main differences between AI in healthcare in the 70s vs. now?

When you think of visions of artificial intelligence in the 70s, you might think of alien-fighting robots or traveling-space robots like the ones shown in Star Wars, Battlestar Galactica or Doctor Who. But the type of AI that was used in healthcare at the time was far from that. The 70s was the time when AI made its debut in healthcare with expert system precursors like Dendral and MYCIN. Today, we often use AI for tasks like managing medical records, textual analysis of medical notes, tests or imaging, digital consultations, medication management, precision medicine based on the patients’ genetic data, and personal healthcare monitoring with wearables like Fitbit.
 
Dendral (Lederberg, 1987), an AI endeavor carried out at Stanford University in the mid-60s, was primarily used to help organic chemists identify unknown organic molecules. It is considered the first expert system because it automates the decision-making process and exhibits problem-solving behavior (Lindsay, 1980). Dendral worked by analyzing the mass spectra of organic molecules and identifying them using a chemistry knowledge base. From the basis of Dendral, MYCIN (Shortliffe & Buchanan, 1975) was created in the early 70s to identify bacteria that caused severe infections and recommend antibiotics dosages based on a patient’s weight. However, MYCIN was never actually used by caregivers because it required that physicians use a standalone server, and was therefore not easy to use in practice. However, both of these systems contributed significantly to the development of subsequent expert systems.
 
The 1980s 90s saw a massive expansion of computer usage in medicine in terms of computing power, genomic sequencing technology, data collection, data storing, and data processing. Alongside the proliferation of the internet, healthcare AI systems were trained to work in the absence of complete datasets and work in tandem with physician expertise (Miller, 1994). The major AI breakthroughs at that moment were in Bayesian networks (Reggia & Peng+, 1986) and artificial neural networks (Baxt, 1991) that were used to improve the clinical decision-making process. Additionally, it was at this time that machines were able to begin replicating human perception and decision-making in the fields of natural language processing (Banko & Brill, 2001), computer vision and robot-assisted surgeries (Lakhani & Sundaram, 2017). 


# An AI Success Story: Predictive modeling for adverse events

Predictive analytics, specifically the application of machine learning to EHR data for the purpose of predicting adverse clinical events, has the potential to improve the effectiveness and efficiency of healthcare delivery. By developing data-driven predictive models and making them available in clinical settings, researchers can enable EHRs to alert nurses, doctors, and other healthcare professionals in real time if patients are at risk for poor clinical outcomes. Early detection of these types of events can help curb patient morbidity, mortality, and health care costs. Recently, several clinical challenges have been extensively modeled by such predictive models: sepsis risk, 30-day hospital readmission risk, and appointment no-shows (Bresnick, 2018). Simple risk scores, like SIRS and SOFA for early detection of sepsis, are used to identify patients at risk and encourage early treatment interventions. However, these risk scores are often outperformed by machine learning models (e.g. Desautels, 2016).

Sepsis is one of the most expensive medical conditions for hospitals to treat, with nationwide hospital expenses amounting to $23.7 billion in 2013 (Torio, 2016). Sepsis is an infection of the bloodstream that causes rapid deterioration and death within hours. With this condition, every minute counts. Being able to focus interventions on patients with the highest sepsis risk can prevent many cases from developing altogether (Adapted from Burkhardt, 2018). Additionally, once sepsis has developed, detecting it and starting treatment as soon as possible is critical. Recent reports have shown that predictive analytics for sepsis risk prediction has already reduced mortality estimates. In 2018, for instance, reported sepsis-related mortalities decreased by 18% at the North Oaks Health System in Louisiana, thanks to a predictive analytics tool developed by researchers. According to the healthcare organization’s Chief Health Information Officer, patients are now receiving treatment 25% faster once they develop sepsis (Kent, 2018).

Machine learning algorithms also have the ability to detect patterns long before humans would be able to discern them. A tool developed by Giannini et al. (2017) at the University of Pennsylvania Health System is able to identify patients who will develop sepsis a full 12 hours ahead of time (Bresnick, 2017). With a specificity of 98%, the model is also remarkably resistant to false positives.

Predictive modeling with EHR data for real-time clinical alerts is challenging for a host of reasons, but there have also been successes. The early detection of sepsis is just one example of a successful application in this realm. As the technology develops and adoption increases, we stand to see numerous benefits from predictive modeling of other adverse events as well.

# The effects of human bias on AI implementations

One might like to think that computer algorithms do not judge or discriminate unfairly based on a patient’s race, gender, or other component of their identity. In many ways, this is true - computers are not humans and are technically not subject to the unconscious biases that cause even the most well meaning individuals to make judgments based on race or other sensitive criteria. For example, Haider et al. (2015) found that most surgical RNs consider themselves impartial to a person’s race, but that only 6.5% were truly indifferent, as measured by an implicit association test. Race and ethnicity are especially sensitive when it comes to healthcare, because decisions may have severe short or long terms consequences. If a person is not given the appropriate treatment in a timely manner, they may be robbed of their ability to recover optimally. Racial disparities in healthcare were subject to an extensive report by the National Academies of Medicine (formerly Institute of Medicine) in 2002, which reports that cardiologists often do not order the same catheterization procedures for black females that they would for black males, white males, or white females, even if they presented with the same symptoms (Institute of Medicine, 2002). Furthermore, the full report states that “racial and ethnic disparities remain even after adjustment for socioeconomic differences and other healthcare access-related factors” (Institute of Medicine, 2003). 

If such differential treatment of people belonging to different ethnic groups is due to humans’  implicit biases, one might think that machine learning models may be able to help fix the problem. However, one important consideration must be kept in mind: machine learning algorithms will learn the patterns in the training data they are given. If training data is biased, a machine learning model will therefore become biased as well. For example, a machine learning algorithm may learn to recommend proper catheterization procedures to black women less often, simply on the basis of their race and gender.

A ubiquitous opportunity to introduce bias into machine learning training data sets exists in digital medicine. Oftentimes, what we use as a gold standard in medicine is not guaranteed to be the truth, but rather it is the best expert opinion available to us. If a person decides what the ground truth label for a set of training data should be, then these labels may be biased. If a machine learning model is subsequently trained on this data, it will learn to make decisions just like the human expert; and that means that the decisions may be unfair or otherwise biased. Only if the labels are objectively true, rather than those based on expert opinion, can we guarantee that no such human bias creeps in.

In medicine, it is often unfeasible or simply impossible to know the truth. For example, it is basically impossible to determine whether ordering a catheterization procedure is truly the correct decision, for an African-American woman or a Caucasian woman, or anyone else. Thus, we sometimes have to define fairness in new ways. One way to do this is to strive to treat all patients equally. However, this does not always result in equality of outcomes or equality of opportunity. For an exploration of what it means for an algorithm to be fair, check out this visualization of an algorithm that decides whether to approve or deny loan applications: [Google Research: Attacking discrimination in ML](http://research.google.com/bigpicture/attacking-discrimination-in-ml/)


# What is “framing” in the context of AI, and how can framing (and alternate framing) be used to advance the field of AI in healthcare?

The field of AI is in part concerned with the ways in human knowledge, reasoning and problem-solving can be represented by machines, and this is often done by slicing various pieces of knowledge into representative parts. In his 1974 paper, “A Framework for Representing Knowledge,” cognitive scientist Marvin Minsky proposed a theory for representing data in AI systems using the concept of a frame, or a “data-structure for representing a stereotyped situation, like being in a certain kind of living room, or going to a child’s birthday party” (Minsky, 1974). The development of frames inherently involves assumptions about what humans believe to be true in certain “canonical” situations, and linking frames into a frame system can therefore be used to represent a stereotypical situation. Framing has become one of the most commonly used data structures in the field of knowledge representation, and modern AI systems typically draw from such knowledge structures to respond to diverse situations (Reddy, 2018). 

In the field of healthcare AI, frame-based systems are commonly used to build clinical support tools like expert CDS systems (Moore & Loper, 2011), conversational agents (Laranjo et al. 2018), radiology decision support systems (Kahn, 1994) and anatomy/physiology representation systems. While many different frames can be compiled together to construct a relatively broad knowledge base, the limitations of frame-based systems in representing complex knowledge bases are apparent within the complex and ever-evolving field of medicine, despite the fact that such systems are used frequently in this field. For example, Noy et al. (2004) found that traditional approaches to frame-based knowledge representation are not sufficient for representing the highly relational and nuanced Digital Anatomist Foundational Model ontology, but that using a protocol for organizing many different frame systems into complex networks were largely sufficient for building the ontology.

However, frames are still finite chunks of information, even when linked to many other chunks of finite information. Each frame is still representative of a stereotypical piece of knowledge about a place, object or situation, and these types of systems therefore poorly represent non-stereotypical objects and situations. In the field of medicine, it is not unreasonable to expect that non-stereotypical situations will arise at a constant rate, given the unique anatomical, situational and historical characteristics that every single patient presents with. It is therefore critical to develop an awareness of the knowledge bases that medical AI systems interface with, and acknowledge their limitations in accuracy and nuance.

# What are adversarial attacks, and what consequences do they have?

Adversarial attacks are a subset of techniques under adversarial machine learning that aim to fool trained machine learning models via malicious inputs. The underlying assumption of adversarial attacks is that the model’s training and test data sets are drawn from the same statistical distribution. However, in real world applications, there may exist adaptive adversarial examples that violate this assumption and lead to model manipulation. In the worst case scenario, these attacks could compromise the security of the machine learning system. Examples of common adversarial attacks include misspelling blacklisted words, adding in whitelisted words in a spam filtering dictionary to bypass a model trained to sort emails, using faults in biometric data to impersonate a real human being in an identification model, or obfuscating malicious code within network packets to avoid intelligent malware protection. Adversarial attacks pose a real threat to any trained machine learning model, and informaticians must be aware of such threats before deploying their systems in sensitive real world settings. 

In March 2019, Finlayson et al., published an interesting article titled “Adversarial attacks on medical machine learning” which summarizes existing adversarial techniques, vulnerabilities in deep learning, potential future applications of malicious intent, and the steps one can take to forge a better path forward. Below is just one example of adversarial attacks presented in the paper
 (all credit goes to [Finlayson et al. 2019](https://science.sciencemag.org/content/363/6433/1287) for the image):

![alt text](https://science.sciencemag.org/content/sci/363/6433/1287/F1.large.jpg?width=800&height=600&carousel=1 “Adversarial Image Example”)

OpenAI also has a great blog post about [Adversarial Machine Learning](https://openai.com/blog/adversarial-example-research/) where they discuss ways to defend against such attacks, including adversarial training (a brute force solution where the model trains with lots of adversarial examples) and defensive distillation (in which the model outputs are probabilities of multiple classes instead of absolute decisions). However, even these training methods can be broken given enough computing power and an informed, dedicated attacker. As with all arms races, it is up to us as informaticians to be prepared and work closer to perfecting our systems by acknowledging the cracks and filling them in one by one.

# References

Adapted from Burkhardt, Hannah. (2018) Machine Learning and Biomedical Informatics. BIME 530.

Banko, M., & Brill, E. (2001). Scaling to Very Very Large Corpora for Natural Language Disambiguation. Retrieved from https://aclweb.org/anthology/P01-1005

Baxt, W. G. (1991). Use of an Artificial Neural Network for the Diagnosis of Myocardial Infarction. Annals of Internal Medicine, 115(11), 843. https://doi.org/10.7326/0003-4819-115-11-843

Bresnick, J. (2017). UPenn Uses Machine Learning, EHRs to Target Severe Sepsis.  Health IT Analytics.

Bresnick, J. (2018). 10 High-Value Use Cases for Predictive Analytics in Healthcare. Health IT Analytics.

Desautels, T., Calvert, J., Hoffman, J., Jay, M., Kerem, Y., Shieh, L., … Das, R. (2016). Prediction of Sepsis in the Intensive Care Unit With Minimal Electronic Health Record Data: A Machine Learning Approach. JMIR Medical Informatics, 4(3), e28. https://doi.org/10.2196/medinform.5909

Finlayson SG, Bowers JD, Ito J, Zittrain JL, Beam AL, Kohane IS. Adversarial attacks on medical machine learning. Science (80- ). 2019;363(6433):1287. doi:10.1126/science.aaw4399

Giannini, H. M., Chivers, C., Draugelis, M., Hanish, A., Fuchs, B., Donnelly, P., … Umscheid, C. (2017). Development and implementation of a machine-learning algorithm for early identification of sepsis in a multi-hospital academic healthcare system. Am J Respir Crit Care Med, 195, A7015. https://doi.org/10.1164/ajrccmconference.2017.D15

Institute of Medicine. (2002). Minorities More Likely to Receive Lower-Quality Health Care, Regardless of Income and Insurance Coverage. Retrieved from http://www8.nationalacademies.org/onpinews/newsitem.aspx?RecordID=10260

Institute of Medicine, (2003). Unequal Treatment: Confronting Racial and Ethnic Disparities in Health Care. Washington, DC: The National Academies Press. https://doi.org/10.17226/10260.

Kahn, CE Jr. (1994). Artificial intelligence in radiology: decision support systems. Radiographics, 14(4): 849-861.DOI: 10.1148/radiographics.14.4.7938772

Kent, J. (2018). Predictive Analytics, EHR Big Data Reduce Sepsis Mortality by 18%. Health IT Analytics.

Lakhani, P., & Sundaram, B. (2017). Deep Learning at Chest Radiography: Automated Classification of Pulmonary Tuberculosis by Using Convolutional Neural Networks. Radiology, 284(2), 574–582. https://doi.org/10.1148/radiol.2017162326

Laranjo, L. et al (2018). Conversational agents in healthcare: a systematic review. J Am Med Inform Assoc 25(9): 1248-1258. doi: 10.1093/jamia/ocy072

Lederberg, J. (1987). How DENDRAL Was Conceived and Born. P270. Retrieved from https://profiles.nlm.nih.gov/BB/A/L/Y/P/

Lindsay, R. K. (1980). Applications of artificial intelligence for organic chemistry : the DENDRAL project. McGraw-Hill Book Co. Retrieved from https://profiles.nlm.nih.gov/BB/A/L/A/F/

Miller, R. A. (1994). Medical diagnostic decision support systems--past, present, and future: a threaded bibliography and brief commentary. Journal of the American Medical Informatics Association : JAMIA, 1(1), 8–27. https://doi.org/10.1136/jamia.1994.95236141

Minsky, M.L. A Framework for Representing Knowledge (1974). MIT-AI Laboratory Memo 306. Retrieved from https://courses.media.mit.edu/2004spring/mas966/Minsky%201974%20Framework%20for%20knowledge.pdf

Moore, M. & Loper, K.A. (2011). An Introduction to Clinical Decision Support Systems. Journal of Electronic Resources in Medical Libraries, 8(4): 348-366. DOI: 10.1080/15424065.2011.626345

Noy, N.F. et al. (2004). Pushing the envelope: challenges in a frame-based representation of human anatomy. Data & Knowledge Engineering, 48(3): 335-359. DOI: https://doi.org/10.1016/j.datak.2003.06.002

Reddy, S. (2018). Use of Artificial Intelligence in Healthcare Delivery. IntechOpen. DOI: 10.5772/intechopen.74714.

Reggia, J. A., & Peng+, Y. (1986). Modeling Diagnostic Reasoning: A Summary of Parsimonious Covering Theory. Retrieved from https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2244953/pdf/procascamc00020-0028.pdf

Shortliffe, E. H., & Buchanan, B. G. (1975). A model of inexact reasoning in medicine. Mathematical Biosciences, 23(3–4), 351–379. https://doi.org/10.1016/0025-5564(75)90047-4

Torio, C. M., & Moore, B. J. (2016). National Inpatient Hospital Costs: The Most Expensive Conditions by Payer, 2013. https://doi.org/10.1377/hlthaff.2015.1194


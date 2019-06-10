---
layout: post
title:  "Fuzzy definitions in CDS"
date:   2019-06-10
author: Hannah
categories: reactions
---

Clinical decision support is an exciting area of clinical informatics. The opportunities that electronic health records afford us in this realm are amazing. However, the challenges are equally mutifaceted. 

One of the grandest challenges with clinical decision support it to make it more accurate and relevant: in Osheroff et al.'s words, "intelligently filtered and presented at appropriate times". But how do we intelligently filter, and what are the appropriate times? These questions aren't easy to answer. An important first step is to filter alerts such that only applicable alerts are shown - e.g. don't show pregnancy warnings for male patients - but it's not always that clear cut. A medication interaction alert might be appropriate as far as the system can tell, but the patient might still have special circumstances that make the alert irrelevant, e.g. the patient may have a personal preference to continue taking the medication despite mild side effects. The next challenge is to show the information at times when they are valuable. This is sometimes translated to a requirement for alerts to be "actionable". However, I think that just because an alert is actionable doesn't mean it is useful, and a non-actionable alert could still be useful. For example, a user might be shown an alert if a patient is determined to be at high risk of sepsis. The alert might be vague, e.g. "The patient is at risk of deterioration", and therefore appear too non-specific to warrant any particular action. However, when the patient is the early stages of increased sepsis risk, the chances are best to make a big difference - even though the action that needs to be taken isn't clear cut. Similarly, a patient might run a fever after sepsis has already developed and therefore score highly on a sepsis risk scale. An alert might inform a nurse that the patient's temperature contributed to the sepsis risk score. Such an alert at first glance appears more actionable, because a fever can be brought down; however, the fever is only a symptom of the patient's infection. In both cases, the system can merely alert the healthcare professional that something is afoot, and clinical insight is needed to make the right decision. 

Osheroff and others have written about what it takes to develop and implement effective clinical decision support. However, it is my impression that we still have a ways to go when it comes to realizing the recommendations in effective ways in day-to-day patient care.



Osheroff, J. A., Teich, J. M., Middleton, B., Steen, E. B., Wright, A., & Detmer, D. E. (2007). A Roadmap for National Action on Clinical Decision Support. Journal of the American Medical Informatics Association, 14(2), 141–145. https://doi.org/10.1197/jamia.M2334
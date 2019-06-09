---
layout: post
title:  "Thoughts on electronic health records"
date:   2019-06-09
author: Harsh
categories: reactions
---
Although a bit late, I would like to take some time and post my thoughts on the current EHR systems available and some of the challenges I faced when becoming familiar with them. Coming from a background of pure biology and theoretical computer science, I was not as familiar with the implementation side of EHR systems. Class discussions and interacting the open source EHR demo really helped me wrap my head around how information is stored in common vendor systems and the continued reliance on SQL-query based information storage and retrieval. While this system has shown to have worked wonders in the past, I do think that a change will be needed in the future. From knowledge representation, we know that other ways of organization are available, but each with its own pros and cons. With the recent movement toward NoSQL databases (i.e. MongoDB) by some of the big tech giants (Microsoft, Amazon, etc.), I wonder if this representation structure would be appropriate in the healthcare world. NoSQL databases are modular and allow for rapid modification, data entry, and data retrieval. Further work would certainly have to be done in order to see if regulation privacy and security rules could be upheld in these new databases.

From my personal experience with EHR systems as a patient, I have found that time during a routine doctor's visit is largely compartmentalized into two or three sections: nurse interaction and medication / illness history entry, doctor interaction, and return of results after the visit. I think manual entry into different portions of common vendor EHR systems takes up a large time in any visit and poses a challenge for informaticians to solve in the next five to ten years. If we can shift that time to direct patient interaction, perhaps the quality of care will improve overall, especially the patient-provider relationship. It may also lead to lower provider burnout and better mental health of our doctors.

Overall, I still have more to learn about the current EHR systems available and look forward to exploring this aspect of our field in the future.


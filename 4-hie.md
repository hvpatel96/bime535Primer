---
layout: page
title: "Health Information Exchange"
---

<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega@5"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-lite@3.2.1"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-embed@4"></script>
<div id="vis"></div>
<script type="text/javascript">
                    var spec ={
  "config": {"view": {"width": 400, "height": 300}, "mark": {"tooltip": null}},
  "hconcat": [
    {
      "hconcat": [
        {
          "data": {
            "url": "https://vega.github.io/vega-datasets/data/us-10m.json",
            "format": {"feature": "states", "type": "topojson"}
          },
          "mark": "geoshape",
          "encoding": {
            "color": {
              "type": "quantitative",
              "field": "pct_phys_e_Rx_ehr",
              "legend": {"format": "%"},
              "title": "Percent"
            },
            "tooltip": [
              {
                "type": "quantitative",
                "field": "pct_phys_e_Rx_ehr",
                "format": ".0%",
                "title": "Percent"
              },
              {"type": "nominal", "field": "region"},
              {"type": "nominal", "field": "year"}
            ]
          },
          "projection": {"type": "albersUsa"},
          "title": "2008",
          "transform": [
            {
              "lookup": "id",
              "from": {
                "data": {"url": "data2008.json"},
                "key": "state_fips",
                "fields": ["pct_phys_e_Rx_ehr", "region", "year"]
              }
            }
          ]
        },
        {
          "data": {
            "url": "https://vega.github.io/vega-datasets/data/us-10m.json",
            "format": {"feature": "states", "type": "topojson"}
          },
          "mark": "geoshape",
          "encoding": {
            "color": {
              "type": "quantitative",
              "field": "pct_phys_e_Rx_ehr",
              "legend": {"format": "%"},
              "title": "Percent"
            },
            "tooltip": [
              {
                "type": "quantitative",
                "field": "pct_phys_e_Rx_ehr",
                "format": ".0%",
                "title": "Percent"
              },
              {"type": "nominal", "field": "region"},
              {"type": "nominal", "field": "year"}
            ]
          },
          "projection": {"type": "albersUsa"},
          "title": "2014",
          "transform": [
            {
              "lookup": "id",
              "from": {
                "data": {"url": "data2014.json"},
                "key": "state_fips",
                "fields": ["pct_phys_e_Rx_ehr", "region", "year"]
              }
            }
          ]
        }
      ]
    }
  ],
  "title": "Percent of physicians exchanging prescription information through Surescripts (Data from healthit.gov)",
  "$schema": "https://vega.github.io/schema/vega-lite/v3.2.1.json"
}
                    var opt = {"renderer": "canvas", "actions": false};  /* Options for the embedding */
                    vegaEmbed("#vis", spec, opt);
</script>

# What is Health Information Exchange and what are the current technologies and implementations?
Health Information Exchange (HIE) is the transfer of health-related information among healthcare providers and other entities who may need access to this type of information. Players might include clinics, hospitals, patients, labs, public health agencies, researchers, schools, and many others. These entities might exchange patient information for various reasons, e.g. to enable continuous healthcare delivery for the patients who are seeing providers at different clinics, to conduct public health surveillance and monitor intervention effectiveness, or to conduct data analytics for research or quality improvement purposes.

There are several types of Health Information Exchange (“What is HIE? \| HealthIT.gov,” n.d.): **Directed exchange** involves providers and other entities who wish to exchange information by sending information directly to each other over the internet, through channels such as secure/encrypted email or other messaging services. This type of exchange requires the exchange partners to have an established relationship (i.e. they know and trust each other). Direct exchange is utilized to exchange data like immunization information with public health agencies. In **query-based exchange**, healthcare providers (or other entities) request or search for a particular piece of information or an entire patient record. Query-based exchange is often used for emergency care. **Consumer-mediated exchange** is a third type of HIE, in which patients transfer their own data to other entities, e.g. they might share step data from a personal device with a healthcare provider. Consumers may also access and correct their own health information as part of consumer-mediated exchange.

An example of a query-based exchange service is Surescripts (“Surescripts \| The Nation’s Most Trusted Health Information Network,” n.d.). Surescripts maintains an electronic database of drug prescriptions which is automatically updated whenever a healthcare provider utilizes “e-prescribing” services. Healthcare organizations are responsible for enabling the e-prescribing functionality in their EHRs, which ensures that prescription data is continually sent to the Surescripts databases. Pharmacies and other providers then query this Health Information Exchange system for their patients’ prescription information.


# What is the current state of HIE adoption?

Since the passing of the Health Information Technology for Economic and Clinical Health (HITECH) Act in 2009, a lot of attention has been given to accelerating the adoption of health information technology. HITECH’s goals include promoting the adoption and use of Electronic Health Records (EHRs) and Health Information Exchange (HIE) for improving costs and quality of the US health care delivery system. Following the HITECH Act, between 2009 and 2014, the percentage of hospitals adopting basic EHRs grew from 12.2% to 75.5% (Mackert, Mabry-Flynn, Champlin, Donovan, & Pounders, 2016).
 
In 2014, Adler-Milstein & Jha reported that in the U.S., there are large state-to-state variations in HIE adoption and that for-profit hospitals were far less likely to engage in HIE than non-profit hospitals. However, states receive funding to develop and implement strategies in which all healthcare providers can access clinical data in at least one way, and ensure that key clinical data can flow across providers and services. In the same year, Furukawa et al., 2014 found that although office-based physicians had a high-rate of EHR adoption, HIE was considerably limited to providers within the same organization. Subsequently, Devine et al. (2017) reported that HIE implementation in 2015 had risen substantially over-time, with 82% of non-federal hospitals (2015), 38% of physician practices (2013) and 17% of long-term care facilities (2013) exchanging information. By 2017, Johnson, Pylypchuk, & Patel, along with the ONC, reported that about 70% of acute care hospitals participated in at least one HIE network nationwide. According to Sadoughi, Nasiri, & Ahmadi (2018), 68.75% of hospital EDs, 53.13% of hospitals, 46.88% of outpatient hospitals, 37.5% of clinics, 31.25% of medical centers and 25% of physician offices currently participate in HIE. The same study shows that the individuals and entities who participate in HIE are mostly physicians, radiologists, laboratories, pharmacies, clinical staff, and nurse practitioners.
 
*Potential issues in the HIE adoption and implementation (Ji, Yoo, Heo, Hwang, & Kim, 2017)*
 
A variety of issues have been reported in the process of improving the adoption of HIE systems (Ji, Yoo, Heo, Hwang, & Kim, 2017). These problems can be separated into 4 major categories: Usability, Documents and Data Elements, System Architecture and Standards, and HIE Consent. The first category relates to system speed, real-time responses, proper usability of the system, and disruption of provider workflows. The document and data item category relates to problems with the ‘exchange documents’ that include relevant clinical data and the standards needed for the creation of such documents. The third category, Architecture and Standards, relates to documentation issues for the architectural standards that support HIE among providers. The last category, Consent, refers to issues in the consent forms needed to exchange clinical information. All of these issues can potentially be solved by enhancing government policies that help smaller healthcare organizations implement HIE systems, even if they do not use market-leading EHRs or are not members of a large integrated health system (Everson & Cross, 2019).

# What are some of the benefits of HIE?

The primary benefits of a well-run, optimized Health Information Exchange system revolve around fast, real-time, and secure transfer of patient information between different nodes within the healthcare information network. Below are some benefits of HIEs provided by [HealthIT.gov](https://www.healthit.gov/topic/health-it-basics/hie-benefits):
<br />
<br />
> > 1. Provides a vehicle for improving quality and safety of patient care by reducing medication and medical errors
> > 2. Stimulates consumer education and patients' involvement in their own health care
> > 3. Increases efficiency by eliminating unnecessary paperwork
> > 4. Provides caregivers with clinical decision support tools for more effective care and treatment
> > 5. Improves public health reporting and monitoring
> > 6. Creates a potential loop for feedback between health-related research and actual practice
> > 7. Reduces health related costs
<br />
<br />
There are certainly more benefits than the ones listed above, but these are the key benefits that health informaticians should strive for when designed new HIE systems. As the U.S. collectively moves towards personalized medicine and active collaboration between patients and their care providers, it is going to be increasingly critical for infrastructure to exist that will allow for the quick and easy transfer of health information. Without research, development, and implementation efforts directed towards HIE systems and protocols, effective information transfer will stagnate. Connecting the above benefits to the different departments that exist in the UW BIME department, we see a heavy emphasis on clinical informatics and public health informatics information transfer in our curriculum (e.g. clinical decision support tools and public health monitoring). However, this does not mean that the development of HIEs will not impact the other health informatics disciplines. With proper implementation, consumer health informatics and bioinformatics will also be impacted as we learn more about how patients interact with one another, and face more challenges in representing biological knowledge. Despite these challenges, the benefits of HIE are too great to ignore and it will require careful collaboration between researchers, EHR vendors, technology experts, providers, public health departments, and others in the healthcare network to help usher in an age of seamless information sharing.

# What are the different institutional drivers and barriers of HIE adoption, and how do they agree and conflict with one another?

From a patient safety and satisfaction perspective, it seems like a no-brainer that HIE should be swiftly adopted by all entities involved in coordinating care for patients. After all, it has the power to reduce medical error, improve healthcare quality and outcomes, and improve clinical decision support tools, among many other care-related benefits (“What are the benefits of health information exchange? \| HealthIT.gov,” 2019). Additionally, HIE is technically within the best interest of healthcare payers and public health entities, because sharing information among providers can help reduce health-related costs by eliminating redundancy in the care process, and it can help improve public health monitoring by establishing a direct and immediate line of communication between providers and public health entities that are interested in gauging the health of a population using the rich information store within EHRs. Healthcare providers are required to implement HIE practices in order to fulfill the Stage 2 requirements of the Meaningful Use incentive plan, and the vast majority of providers recognize that HIE can improve the fluency and efficiency of their care workflows.

However, the various forces that determine whether HIE policies and practices are actually created, adopted and implemented operate within a complex framework of stakeholders with wildly different priorities. Even if the interoperability issues of HIE were not a major barrier to implementation, exchanging health information might not be within the immediate best interest of all entities involved in the exchange--even if it is within the best interest of the general public. In the case of healthcare providers, the costs of incorporating these new technical capabilities into the EHR and continuously training staff to use these new capabilities pose financial barriers to many smaller practices (Ross et al. 2010). Healthcare practices within less tightly knit communities are often more mistrustful of each other than those in communities with regular peer-peer professional and social interactions. As a result, practices are less likely to adopt HIE protocols when there are higher levels of mistrust and competition among providers. Additionally, healthcare providers in competitive markets are more likely to value ownership over their own patient health data, and they view sharing health data as a potential threat to their share of the healthcare market value (Yaeger et al. 2014). Finally, a reduction in the redundancy of care services may not necessarily be an incentive for HIE adoption among healthcare providers who participate in a fee-for-service payment system, since providers receives payment for services from third-party payers regardless of whether these services have already been performed by another provider for a given patient.

However, providers are certainly not the only stakeholders who may resist HIE adoption. Patients themselves may also oppose widespread HIE implementation due to security and privacy concerns, which are becoming increasingly common among patients. Esmaeilzadeh & Sambasivan (2017) reviewed 36 peer-reviewed journal articles on patient attitudes toward HIE efforts between 2005 and 2015, and found that although patients understand that HIE would facilitate communication among their providers and improve their quality of care, they are concerned by the thought of many different organizations (both health-related and otherwise) having access to their private health data. As a consequence, recent efforts to make security breaches among health organizations more transparent (as featured on websites like the Department of Health and Human Services “Wall of Shame”) might make patients more reticent to support HIE efforts.


# References

Adler-Milstein, J., & Jha, A. K. (2014). Health information exchange among U.S. hospitals: Who’s in, who’s out, and why? Healthcare, 2(1), 26–32. https://doi.org/10.1016/j.hjdsi.2013.12.005

Devine, E. B., Totten, A. M., Gorman, P., Eden, K. B., Kassakian, S., Woods, S., … Hersh, W. R. (2017). Health Information Exchange Use (1990-2015): A Systematic Review. EGEMs (Generating Evidence & Methods to Improve Patient Outcomes), 5(1), 27. https://doi.org/10.5334/egems.249

Esmaeilzadeh & Sambasivan (2017). Patients’ support for health information exchange: a literature review and classification of key factors. BMC Med Inform Decis Mak 17(1): 33. doi: 10.1186/s12911-017-0436-2.

Everson, J., & Cross, D. A. (2019). Mind the gap: the potential of alternative health information exchange. The American Journal of Managed Care, 25(1), 32–38. Retrieved from http://www.ncbi.nlm.nih.gov/pubmed/30667609

Furukawa, M. F., King, J., Patel, V., Hsiao, C.-J., Adler-Milstein, J., & Jha, A. K. (2014). Despite Substantial Progress In EHR Adoption, Health Information Exchange And Patient Engagement Remain Low In Office Settings. Health Affairs, 33(9), 1672–1679. https://doi.org/10.1377/hlthaff.2014.0445

Ji, H., Yoo, S., Heo, E.-Y., Hwang, H., & Kim, J.-W. (2017). Technology and Policy Challenges in the Adoption and Operation of Health Information Exchange Systems. Healthcare Informatics Research, 23(4), 314–321. https://doi.org/10.4258/hir.2017.23.4.314

Johnson, C., Pylypchuk, Y., & Patel, V. (2017). Methods Used to Enable Interoperability among U.S. Non-Federal Acute Care Hospitals in 2017. Retrieved from https://www.healthit.gov/sites/default/files/page/2018-12/Methods-Used-to-Enable-Interoperability-among-U.S.-NonFederal-Acute-Care-Hospitals-in-2017_0.pdf

Mackert, M., Mabry-Flynn, A., Champlin, S., Donovan, E. E., & Pounders, K. (2016). Health Literacy and Health Information Technology Adoption: The Potential for a New Digital Divide. Journal of Medical Internet Research, 18(10), e264. https://doi.org/10.2196/jmir.6349

Ross, S.E. et al. (2010). Health information exchange in small-to-medium sized family medicine practices: motivators, barriers, and potential facilitators of adoption. Int J Med Inf, 79(2): 123-129.

Sadoughi, F., Nasiri, S., & Ahmadi, H. (2018). The impact of health information exchange on healthcare quality and cost-effectiveness: A systematic literature review. Computer Methods and Programs in Biomedicine, 161, 209–232. https://doi.org/10.1016/J.CMPB.2018.04.023

Surescripts \| The Nation’s Most Trusted Health Information Network. (n.d.). Retrieved June 5, 2019, from http://www.surescripts.com

What are the benefits of health information exchange \| HealthIT.gov (2019). Retrieved June 9, 2019, from https://www.healthit.gov/faq/what-are-benefits-health-information-exchange.

What is HIE? \| HealthIT.gov. (n.d.). Retrieved June 5, 2019, from https://www.healthit.gov/topic/health-it-and-health-information-exchange-basics/what-hie.

Yaeger, V.A. et al (2014). Factors related to health information exchange participation and use. J Med Syst, 38(8): 1-9.



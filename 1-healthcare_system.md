---
layout: page
title:  "The US Healthcare system"
---
<script src="https://cdn.jsdelivr.net/npm/vega@4"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@2.6.0"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@3"></script>
<div id="vis"></div>
<script type="text/javascript">
                    var spec = {
  "config": {"view": {"width": 400, "height": 300}},
  "hconcat": [
    {
      "layer": [
        {
          "data": {
            "url": "life_expectancy_vs_expenditure.json",
            "format": {"type": "json"}
          },
          "mark": "line",
          "encoding": {
            "color": {"type": "nominal", "field": "Country"},
            "tooltip": [
              {"type": "nominal", "field": "Country"},
              {"type": "ordinal", "field": "Year"},
              {"type": "quantitative", "field": "Life expectancy (years)"}
            ],
            "x": {"type": "ordinal", "field": "Year"},
            "y": {
              "type": "quantitative",
              "field": "Life expectancy (years)",
              "scale": {"zero": false},
              "title": "Life expectancy at birth (years)"
            }
          },
          "title": "Life expectancy over time"
        },
        {
          "data": {
            "url": "life_expectancy_vs_expenditure.json",
            "format": {"type": "json"}
          },
          "mark": "circle",
          "encoding": {
            "color": {"type": "nominal", "field": "Country"},
            "tooltip": [
              {"type": "nominal", "field": "Country"},
              {"type": "ordinal", "field": "Year"},
              {"type": "quantitative", "field": "Life expectancy (years)"}
            ],
            "x": {"type": "ordinal", "field": "Year"},
            "y": {
              "type": "quantitative",
              "field": "Life expectancy (years)",
              "scale": {"zero": false},
              "title": "Life expectancy at birth (years)"
            }
          },
          "title": "Life expectancy over time"
        }
      ],
      "width": 120
    },
    {
      "layer": [
        {
          "data": {
            "url": "life_expectancy_vs_expenditure.json",
            "format": {"type": "json"}
          },
          "mark": "line",
          "encoding": {
            "color": {"type": "nominal", "field": "Country"},
            "order": {"type": "ordinal", "field": "Year"},
            "tooltip": [
              {"type": "nominal", "field": "Country"},
              {"type": "quantitative", "field": "Value", "title": "% GDP"},
              {"type": "quantitative", "field": "Life expectancy (years)"},
              {"type": "ordinal", "field": "Year"}
            ],
            "x": {
              "type": "quantitative",
              "field": "Value",
              "title": "% GDP spent on healthcare"
            },
            "y": {
              "type": "quantitative",
              "field": "Life expectancy (years)",
              "scale": {"domain": [76, 84]},
              "title": null
            }
          },
          "title": "Life expectancy vs. healthcare expenditures (2000-2015 OECD data)"
        },
        {
          "data": {
            "url": "life_expectancy_vs_expenditure.json",
            "format": {"type": "json"}
          },
          "mark": "circle",
          "encoding": {
            "color": {"type": "nominal", "field": "Country"},
            "order": {"type": "ordinal", "field": "Year"},
            "size": {
              "type": "ordinal",
              "field": "Year",
              "legend": null,
              "scale": {"range": [30, 60]}
            },
            "tooltip": [
              {"type": "nominal", "field": "Country"},
              {"type": "quantitative", "field": "Value", "title": "% GDP"},
              {"type": "quantitative", "field": "Life expectancy (years)"},
              {"type": "ordinal", "field": "Year"}
            ],
            "x": {
              "type": "quantitative",
              "field": "Value",
              "title": "% GDP spent on healthcare"
            },
            "y": {
              "type": "quantitative",
              "field": "Life expectancy (years)",
              "scale": {"domain": [76, 84]},
              "title": null
            }
          },
          "title": "Life expectancy vs. healthcare expenditures (2000-2015 OECD data)"
        }
      ]
    }
  ],
  "$schema": "https://vega.github.io/schema/vega-lite/v2.6.0.json"
}
                    var opt = {"renderer": "canvas", "actions": false};  /* Options for the embedding */
                    vegaEmbed("#vis", spec, opt);
</script>

## Healthcare Cost and Financing
Health care in the United States is more expensive than in any other Western nation; yet, patient outcomes do not reflect the investment. Understanding the reasons behind the astronomical health care costs and the disappointing outcomes in this country is an important pre-requisite to understanding what can be done about it. 

Two important contributors to the explosion of costs in the U.S. healthcare system today are (1) the current health insurance system and (2) the current payment model by which healthcare providers are compensated. However, there are many more.

### Health insurance: Community rating vs. Experience rating
Health insurance is unlike other insurance in that it is expected to cover most or all healthcare expenses, including routine and preventive care. Health insurance policies are therefore also often called health plans. 
The principle of the redistribution of funds is fundamental to how health insurance works: everyone pays a regular contribution, and those that get sick then benefit regardless of the sum of money they have contributed. Because only some will get sick in a given month or year, the collectively contributed money can cover all costs for the few that need payouts.

Premiums can be set through either experience rating or community rating. **Community rating** involves setting premiums to a fixed amount for everyone in a given community. Because everyone pays the same premium, this means that some people (e.g. the elderly or very sick) may receive benefits in excess of their contributions, whereas others (e.g. the young or generally healthy) may contribute more than they receive in benefits. This also means that individuals, even the very sick, are not left behind, but rather covered by society at large.

The alternative is **experience rating**, where premiums are set based on the expected typical needs for healthcare services and products, calculated from past usage (“experience”) for similar patients. Under this system, young and healthy individuals pay low fees, and old and sick people pay high fees. In a free market, insurers may choose to set premiums via experience rating, because this allows them to offer lower, more competitive premiums - as long as they control the amount of benefits paid out by avoiding the costliest patients. Those who are likely to have high healthcare needs will therefore have exceedingly high insurance premiums or will be altogether ineligible for insurance coverage.

In the U.S., Blue Shield/Blue Cross used community rating, which allowed these insurers to cover individuals at a fixed premium that was not dependent on healthcare needs. However, with the advent of for-profit insurance companies, the younger and healthier individuals flocked towards these cheaper plans, leaving the community rating insurers with only the high-cost patients – an unsustainable situation. Today, experience rating is the most commonly used pricing system for individual insurance, which many poor and/or sick people depend on, e.g. the unemployed or those with jobs without health insurance benefits. This contributes to health insurance being much more expensive, to the point of being completely unaffordable, for those who are most in need of health care. While the Affordable Care Act included regulations that disallow insurers from systematically excluding certain groups – e.g. those with pre-existing conditions – insurers are still free to set premiums as they see fit, which means that they can charge the sickest patient populations with exorbitant premiums. An inequality of access to healthcare services is created, which contributed to poor outcomes for certain populations.

### Paying for healthcare: Fee-for-service vs. Capitation and Salary
One of the most important contributors to rising healthcare costs is the fee-for-service financing structure that is used in most healthcare settings in the U.S. today. Under this model, physicians are compensated for each individual service they perform (e.g. tests, procedures, and visits). This creates an economic incentive for doctors to perform more services. Unfortunately, this sometimes leads to unnecessary tests and procedures being performed. For example, if a doctor is paid for each surgery they perform, they may choose to perform many more surgeries that are not strictly necessary than they otherwise would.

An alternative is the Capitation payment system, under which providers are paid a fixed amount of money for each patient in their care. Providers then have an incentive to provide the most effective care – to provide preventive care, take an active role in public health considerations (such as smoking cessation programs), and to only perform the most effective services. In other words, the doctor’s responsibility is shifted from providing as much care as possible to keeping the patient healthy, and if they get sick, to treat them in the most economical way. In the U.S. today, capitation is practiced by some physician groups, such as Health Maintenance Organizations (HMOs).

Finally, an additional possible alternative is to pay physicians by salary. With this approach, physicians are freed entirely from concerns around their own compensation. While this removes the incentive to perform unnecessary services, the fact that there is also no significant incentive to perform the highest quality care is a possible concern. As a result, salaried physicians may often earn additional bonuses for high performance.

### What can be done?
While the reasons why our healthcare system in the United States today is subpar, both in terms of outcomes and affordability and access, are manifold and complex, we can look to other countries and compare their systems to ours to find a possible path forward. 

Community rating is used to set premiums by many western countries, such as Japan, Canada, the UK, and Germany. In fact, these countries not only set premiums independently of healthcare needs, but they also scale contributions based on income. For example, in both Canada and the UK, healthcare is entirely funded by taxes, which are set as a percentage of income. In Germany and Japan, a percentage of each individual’s salary is deducted for health insurance (8.2% and 4.1%, respectively) with an additional contribution made by the employer.

Capitation is also used by several countries. For example, Canada has been shifting its payment model towards Capitation for many years, though much of reimbursement is still done on a fee-for-service basis. In the UK, most physicians have been paid through capitation since the early 20th century.

Hospital-based physicians are salaried in many countries, including Germany and Canada.

## Healthcare Quality
<img src='images/image1.gif'>
### What are the components of high-quality care?
- Adequate Access to Care: As people have more access to care, they would receive more quality care. People who cannot afford healthcare will not receive quality care.
- Adequate Scientific Knowledge: Insufficient scientific knowledge could lead to medical errors and in bad outcomes for patients. We need to ensure that caregivers have access to scientific knowledge so that the number of medical errors decreases.
- Competent Health Care Providers: 
    - Providers with more experience + better equipment in a hospital will have lower levels of mortality rates.
    - Understaffing essential staff like nurses will turn out in higher mortality rates.
    - The development of clear clinical practice guidelines will develop on lower mortality rates.
- Money and Quality care: As in the ‘adequate access to care’ component, people with higher income can access quality care whereas people with lower income will struggle to get quality care.
- Health Care Systems and Quality of Care: If the hospitals are not well organized and do not have a system for treating their patients in a careful and timely, the mortality rates of that hospital will increase. For this particular component, having the proper number of staff will be critical for optimizing the provided care.

### Are there informatics interventions that could enable each of these components?
Informatics interventions have been already made with the thought that it would improve quality in different aspects but it has had some mix results over time. At first, the EHR was thought to be the savior of the health care systems but it has complicated workflows for care providers that know has to worry about filling the electronic forms, which they didn’t have to do before. This brings unsatisfaction and change resistance over the implementation of new electronic systems.
### How might health systems work to improve quality? 
Prevention is key for improving quality. Without prevention and specific campaigns for attacking one of the possible sources for different diseases, quality will not be able to improve because care providers will have limited options on how to proceed with some specific disease. Focusing on social determinants of health is also important because it is tightly connected with prevention and how the public health campaigns are designed and implemented. We cannot longer have differences in treatment because on someone social or economic status, making them ‘destined’ to have some specific type of care regardless of their health condition.

## Healthcare Access
The book describes financial and non-financial barriers to care. Are one or both of these amenable to informatics interventions?

Financial barriers to care primarily include lack of insurance or underinsurance, whereas non-financial barriers to care can include anything from lack of prompt access to language, literacy, and cultural differences to factors such as gender and race biases. Historically, large interventions (nationwide and sponsored by the government) have focused primarily to addressing the financial barriers to care. Landscape changing legislation like the Affordable Care Act along with existing programs such as Medicaid and Medicare are the major examples of tackling the uninsured population’s inability to pay. While politicians, economists, and researchers still debate whether availability of insurance plays a large factor in more efficient diagnosis and resolution, there is no doubt that health insurance improves health outcomes in underserved populations and relieves financial loads that overwise accumulate over lifetimes. Also under financial barriers to care is underinsurance. Very few American adults and their families have good, quality health insurance compared to the masses and the rest of the world. It was reported in 2007 that roughly 62% of all bankruptcies in the US were caused by the inability to pay medical bills (Himmelstein et al., 2009). Interesting enough, Elizabeth Warren, a 2020 U.S. Presidential candidate, is an author on that paper. Health access and the controversies surrounding it has always been a hot topic issue in campaigns and we are sure to see discussions around it in the near future. Simply having insurance is often not enough to receive the care one needs, especially for chronic diseases and pre-existing conditions. A good quote on this topic is quite simply: “Access to health care does not guarantee good health, but without such access, health is certain to suffer.” (Bodenheimer and Grumbach, 2016).

Moving on to the non-financial barriers to care, recently, as the field of informatics and related disciplines move to a more active view on healthcare and place more attention on the patients, we have begun to uncover challenges that were not as closely studied in the past. These challenges include lack of prompt care, language and cultural differences between providers and their patients, and the influence of race/ethnicity and gender in the quality of care. Compared to the financial barriers of care, these factors have been understudied and amenable to informatics interventions. Studies on race, gender, age, and socioeconomic status with respect to healthcare access and outcomes have shown disparities in care, especially affecting the African American and Hispanic populations. Whether these were fueled by the availability of shareable electronic data or recent equality movements, it is clear to see that more work needs to be done to fully understand the cogs of this complex challenge so ingrained in our healthcare system. 

Specific examples of informatics interventions that can tackle both financial and non-financial barriers to care include better book-keeping and easier sharing of claims and health outcomes data. With electronic medical records, we are better able to understand the implicit workflows that govern the healthcare system and design ways to optimize and improve these workflows to better serve the patients. Interventions that could possibly improve non-financial barriers could include automated translation of languages and alerts reminding the providers to cover patient-specific needs (especially for gender and cultural biases). Lastly, an intervention that could help reduce the load of financial barriers may be as simple as tracking cost of care of chronic diseases of insured populations with different levels of coverage and analyzing whether overall cost per patient is minimized if better coverage is provided from the beginning.

## Healthcare Structure and Workforce
### Levels of Care
The US healthcare systems is organized into primary, secondary and tertiary levels of care that are meant to address different patient needs. In theory, each of these levels has the following attributes:
1. Primary Care
    - Characteristics: preventative, comprehensive, integrative, longitudinal, ambulatory
    - Example Conditions: asthma, diabetes, hypertension, no existing conditions (purely preventative)
    - Example Specialties: family medicine, pediatrics, internal medicine
2. Secondary Care
    - Characteristics: specialized, acute, emergency or referral-based, ambulatory or hospital-based
    - Example Conditions: broken bone(s), mental illness, heart murmur
    - Example Specialties: psychiatry, radiology, cardiology
3. Tertiary Care
    - Characteristics: highly specialized, acute, emergency or referral-based, hospital-based
    - Example Conditions: brain tumor, severe burns, neonatal emergencies
    - Example Specialties: cardiothoracic surgery, transplant surgery, complex oncology
In the **regionalized model** of healthcare organization, the three main levels of care are strictly segmented and primary care providers act as “gatekeepers” to higher levels of care, barring emergencies. Primary care services are numerous, widespread and serve smaller subpopulations, whereas secondary and tertiary care services are increasingly scarce and serve larger segments of a population. Specialized practitioners account for about half of all healthcare practitioners in the UK, which practices a regionalized model of organization.

The US healthcare system instead practices a **dispersed model** of organization in which care is less coordinated between providers, patients may refer themselves to secondary and even tertiary care specialists, and secondary and tertiary care services are widespread. Specialized practitioners account for the majority of all healthcare practitioners in the US.

It is well known that primary care services are less expensive than secondary and tertiary care services, and that most members of a population require primary care services. High functioning primary care models contribute to the **“triple aim”** of healthcare improvement (see Chapter 2). However, wide availability of more advanced medical services gives patients autonomy over their healthcare choices and allows new technologies to advance quickly. The high demand for advanced care in the US, though culturally synchronous, has made the primary care professions less desirable from an economic standpoint. Despite a sustained need for primary care serves throughout the country, the quality and quantity of primary care delivered to patients is decreasing.

### Healthcare Delivery Structures
The majority of those with health insurance in the US are covered by a **Health Maintenance Organization (HMO)** plan, through which providers and hospitals are paid a fixed amount per capita for their services, regardless of what and how many healthcare services are provided. Patients with HMO plans are limited to receiving care from a limited network of providers.

**Vertically integrated** HMOs like Kaiser-Permanente are managed under a single organizational roof that orchestrates all aspects of care: hospitals, physicians, pharmacies, home health agencies and the HMO health plan itself. This model more closely resembles the regionalized model of healthcare, and it offers an alternative to the traditional fee-for-service payment system. However, **virtually integrated** HMOs have become the far more popular plan among healthcare consumers in the US. Physicians and hospitals may form contractual relationships with many different HMOs.

**Preferred Provider Organization (PPO)** plans were developed in response to patients’ desire to more freely visit physicians and hospitals of their choice. These plans are fee-for-service based and propagate the dispersed model of care.

### Reformed Models of Care
In the face of the deteriorating primary care system in the US and rising healthcare costs, new models of care have been proposed to improve patient experience and outcomes. **Accountable Care Organizations (ACOs)** were formed as a result of the Affordable Care Act, which encouraged providers to voluntarily join together to form networks that manage all aspects of care for a given population. These groups are paid through payment models such as the Medicare Shared Savings Program, which incentivizes providers to reduce health care spending with a net savings bonus. The shared financial risk between payers and providers encourages a regionalized model of care and is meant to reduce healthcare costs.

The **patient-centered medical home (PCMH)** model is a theoretical framework for healthcare delivery that is comprehensive, patient-focused, team-based, accessible, and focused on safe and high-quality primary care. This proposed model would likely function in a “medical neighborhood” that resembles existing ACO structures. However, the practical implications of creating a personalized, integrated care experience for patients within a dispersed provider network are cause for concern in terms of achieving true healthcare reform. Novel payment models may need to be developed before the PCMH model can be achieved in reality.

The PCMH model quite literally extends to patients’ own homes in the context of improving long-term care for geriatric and terminally ill populations. In the US, long-term care has historically been provided by family members or in nursing homes. Institutionalized long-term care is often poorly orchestrated, inhumane and prohibitively expensive, while at-home care places an extensive emotional and physical burden on family caregivers. The **community model** of long-term care is focused on providing financial, practical and emotional support to at-home caregivers financed by a social insurance plan.


## References
Bodenheimer, T., & Grumbach, Kevin. (2016). Understanding health policy: A clinical approach (Seventh ed., McGraw-Hill's AccessMedicine). New York: McGraw-Hill Education.

Himmelstein, Thorne, Warren, & Woolhandler. (2009). Medical Bankruptcy in the United States, 2007: Results of a National Study. The American Journal of Medicine, 122(8), 741-746.

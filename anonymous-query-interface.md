# **Anonymous query interface **

### **enables AI learning over distributed & encrypted data**

There are many complicated \(from development and resource standpoint\) ways to query encrypted data \(multi-party computation, proxy re-encryption\), but luckily there is an actual ‘trusted device’ in the Iryo network- end user device \(phone/tablet/pc\). Since it needs to be able to read all the health data in plain text, it can also execute the queries over the same data.



We need a way to deliver queries to end user without breaking its anonymity or given consent.  
• First Iryo would verify research institutes to make sure they are legit and are not just trying to collect and re-sell the data.  
• Researchers would get ‘Iryo Research portal’ software they can use to send queries to Iryo network, using the [‘Archetype Query Language’](http://www.openehr.org/releases/QUERY/latest/docs/AQL/AQL.html) \(AQL, openEHR specification\)  
• When they do, Iryo would verify the query first; to check that query is not too broad, or repetitively asking for information trying to reconstruct the records \(over a longer period of time\),.  
• Patient's own device verifies that patient meets the query criteria. If it does the query details along with the name of the research institution and amount of tokens to be received by a patient is shown on device pending approval.



In an actual implementation, the patient's device will receive a silent notification which will wake up background process to query scope \(for instance; female, 30-35 years old, with diabetes\). If the a patient does not fall in the scope, silent notification disappears, without reporting anything back \(to keep users anonymous\). If it falls into the scope, a notification would be shown on the patients device including the name of the research institution, the justification for a query to be requested in the first place \(goals of the research\) and a number of tokens as an incentive to allow query results to be sent back.

  
Iryo envisions 3 types of \(opt-out\) anonymous requests that present different implication for privacy, and as such require distinct user consent.

**  
**

## **Copy then analyse**

### **PseudoAnonymous query - used for AI training dataset**

Request for medical data in plain form, without the directly identifiable personal information \(pseudonymous\). This bears high costs \(region of 100$ worth of IRYO tokens\) because even without personally identifiable information, this data can still be used to match against other databases and the patients could be identified if that data leaks from the researcher.[^1]

![](https://lh3.googleusercontent.com/AUgBnIHHDUIACaEr_ADU5H4AorJ9s1I1yLMGYxXWvDc-XPha7yNM34SKwzyMnAvwoIGm6Gc1V_LkFRLLT39W7DGaKGfuplZWLiclQwGhuOQhd_4etrnWnjfWMWj_0ZGLCzBk6ZQA)

A number of these request should be kept low \(up to 100 patients max\) and can be used to train and test machine learning algorithms freely. After results are found and the algorithm needs to be validated \(or invalidated\) over much bigger population sample size, they go to the next type of query.

**  
**

## **Analyze in place**

### **Anonymous query- used for AI validation dataset**

Anonymous query over medical data; it bears very low cost \(in the region of 0.1$ worth of IRYO tokens\) because this request takes some data, performs a formula over them, and then only sends back the result; numbers or binary \(true/false\). There is no leakage of personal information and it can not be compared to other databases.

These requests can be sent to all users in the Iryo.network and can be used to train and test machine learning algorithms, until the researcher finds and validates the missing link.

![](https://lh3.googleusercontent.com/K-45za5XnTVIweD6b0Ay4KRXrxxfsi3zBmelENeuLNJaHuId1hbJ2B9g7OZFWOHBDies1PLDatjvjVLSYwcblLMDy_FXFHIoMGkPXo-0gLT_UC7ZiRbcmuARsZBJmBd9kIpOifh6)

### **Anonymous query- used to save lives**

Anonymous query over medical data that sends nothing back, but rather shows actionable results. It’s philosophy that researchers should/could share the actionable algorithms they validated. Of course, algorithms need to go through regulatory authority \(FDA or EMA\), before they can become “medical advice” \(clinically verified\) and can be served back to Iryo patients without health risks.

![](https://lh3.googleusercontent.com/topFTnG-CWOnv6FT_XZ-S6L1GudYSpDZFS9QHDEFdQWztoHujmip-PCyApGTnj0XVvPhwlcKJAsDcixF8Hvj1BhS3BXgkUzOAs-m-RL09foR4JlSbWtYYs8qdxOQeZT1A8Pz08HR)

## **Benefits for researchers**

1.\) Use Iryo Research portal to enroll people with specific health conditions \(defined by a scope\). Direct acess to EHRs of specifically defined patients can decrease the time needed for patient recruitment, potentially decreasing the cost of pre-recruitment process. Recruitment agencies and services usually need to first attract potential patients and then check their eligibility. This can be much more time consuming than a query in the Iryo network.

2.\) Find 100 people that respond to it, and collect their health data.

3.\) Use machine learning \(AI\) to find patterns.

4.\) Verify learned formulas on the 10.000 more people with anonymous query, without ever exposing their information.



Since Iryo.network scales better \(because of inherent privacy\) to more patients internationally, researchers would be able to reach more people that way.

## **Benefits for Patients - find actionable early indicators of health problems/diseases **

When researchers find the correlations and those get clinically verified, users would get the anonymous queries that would seep through their data and present them with actionable advice. For instance; which specialist they need to see and which test to take. Those queries would not be reported back, they stay on the patients phone.  


Not sharing your health information but still getting the research results is something that wasn’t possible with the old style of EHR designs. Yet Iryo would deliver just that!



If the patient \(older or non-technical\) does not possess a phone or an app, he could give permission to his doctor to allow research after an-approval processes at the clinic.

  


[^1]: [https://en.wikipedia.org/wiki/Privacy\_for\_research\_participants](https://en.wikipedia.org/wiki/Privacy_for_research_participants)


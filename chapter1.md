# **OpenEHR**



According to a study published by [Dell’s](https://www.emc.com/analyst-report/digital-universe-healthcare-vertical-report-ar.pdf), the healthcare industry is expected to generate more than 500 exabytes of data with an expected annual growth rate of 48%. This presents a looming challenge in data management. Although multiple standards try to address this issue, a lot of that data is still stored inside local silos in proprietary formats. As such reusability of the data and interoperability between different actors is often too expensive or even impossible.

To make our data as open and as meaningful as possible we decided to use openEHR's approach to data modeling and exchange. At the core of openEHR are simple and [exchangeable archetypes](http://ckm.openehr.org/ckm/) that link values to their actual meaning \([blood pressure](https://github.com/ppazos/cabolabs-ehrserver/blob/master/opts/production/vital_signs/archetypes/openEHR-EHR-OBSERVATION.blood_pressure.v1.adl) as an example\). Simple and widely used archetypes can then be linked together in more complex structures to support various types of procedures required by clinics.

Archetypes don't only solve data storage problems but are also used in openEHR's Archetype Querying Language \(AQL\) where archetypes can be reused in building and running extensive queries across the data.

The openEHR community \(in collaboration with doctors and clinicians\) have been preparing specifications and collecting archetypes for the last 15 years and have already been chosen as a level of standard in nation-wide data exchange programs in some European Union countries. Taking this into consideration, we deem it the best option to manage handl patient data with vendor independence by using openEHR.

---

[http://www.openehr.org/ ](http://www.openehr.org/)


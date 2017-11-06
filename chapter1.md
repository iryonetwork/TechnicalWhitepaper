# **OpenEHR**

According to Dell’s study health care industry is expected to generate more than 500 exabytes of data with expected annual growth rate of 48%. Although multiple standards try to address this issue, a lot of that data is still stored inside local silos in proprietary formats. As such reusability of the data and interoperability between different actors is often to expensive or even impossible.

To make our data as open and as meaningful as possible we decided to use openEHR's approach to data modeling and exchange. Core of openEHR are simple \(ex:[blood pressure](https://github.com/ppazos/cabolabs-ehrserver/blob/master/opts/production/vital_signs/archetypes/openEHR-EHR-OBSERVATION.blood_pressure.v1.adl)\) and exchangeable \([http://ckm.openehr.org/ckm/](http://ckm.openehr.org/ckm/%29\) archetypes that link values to their actual meaning. Simple and widely used archetypes can then be linked together in more complex structures to support various types of procedures required in clinics.

Archetypes don't only solve data storage problems but are also reused in openEHR's Archetype Querying Language \(AQL\) where archetypes can be reused in building and running extensive queries over the data.

The openEHR community \(with large involvement from doctors and clinicians\) has been preparing the specifications and collecting archetypes for the last 15 years and was already chosen as a standard in nation wide data exchange programs in some European Union countries. As such we see it as the best option to handle lifetime of patients data with vendor independence.

[http://www.openehr.org/ ](http://www.openehr.org/)


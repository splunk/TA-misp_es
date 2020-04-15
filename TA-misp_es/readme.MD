This TA is designed to provide integration between MISP and Splunk Enterprise Security using the concept of local lookups, but using a separate set of MISP labeled csv lookups rather than the default local lookups provided with Enterprise Security. This is designed to show MISP specific data integrating into ES. Local lookups can easily be used instead by modifying the associated conf files.

Threat intelligence from MISP by default maps to the threat collections in this TA; Email, file, http, ip/domain, registery.

Saved searches are the key to getting MISP data into ES, so any modifications to the lookups is handled there by modifying the lookup in the | outputlook portion of the search.

This TA assumes that Splunk Enteprise Security is installed as well as MISP42Splunk, which contains the custom commands and APIs to integrate with MISP.
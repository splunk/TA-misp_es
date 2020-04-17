This TA is designed to provide integration between MISP and Splunk Enterprise Security using the concept of local lookups, but using a separate set of MISP labeled csv lookups rather than the default local lookups provided with Enterprise Security. This is designed to show MISP specific data integrating into ES. Local lookups can easily be used instead by modifying the associated conf files.

Pruning of the csv will be desired as the indicator pulls are currently appending which depending on the indicators can lead to extremely large csv files.

Threat intelligence from MISP by default maps to the threat collections in this TA; Email, file, http, ip/domain, registery.

Saved searches are the key to getting MISP data into ES, so any modifications to the lookups is handled there by modifying the lookup in the | outputlook portion of the search. The custom command from the MISP42Splunk app that searches MISP is called mispgetioc. A set of switches have been set but can be modified in the saved search to modify the flow of the indicators from MISP. It is recommended you test your mispgetioc search prior to implementing it in the saved search to ensure you get the data you expect coming into ES' Threat Intel Framework.

This TA assumes that Splunk Enteprise Security is installed as well as MISP42Splunk, which contains the custom commands and APIs to integrate with MISP.
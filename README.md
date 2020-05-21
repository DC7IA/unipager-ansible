--- Install unipager using ansible ---

Unipager is an amateur radio software for sending messages using POCSAG.

----- Usage ----

Define what Host in the file 'hosts'. Fill in the IP address / hostname and the username.

```ansible-playbook site.yml --ask-become-pass --extra-vars "pocsag_callsign="CALLSIGN" pocsag_api_key="xxxxx""```

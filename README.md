### Install unipager using ansible ###

Unipager is an amateur radio software for sending messages using POCSAG.

This will add the official .deb repo and set up unipager.

#### Usage ####

Define what host to use in the file 'hosts'. Fill in the IP address / hostname and the username.

```ansible-playbook site.yml --ask-become-pass --extra-vars "pocsag_callsign="CALLSIGN" pocsag_api_key="xxxxx""```

# Install unipager using ansible

Unipager is an amateur radio software for sending messages using POCSAG.

This will add the official .deb repo and set up unipager.

## Usage

### Provide call sign and API key via CLI

Define what host to use in the file 'hosts'. Fill in the IP address / hostname and the username.

Use this command with your call sign and api key:

```ansible-playbook site.yml --ask-become-pass --extra-vars "unipager_callsign="CALLSIGN" unipager_api_key="xxxxx""```

You may have to change roles/debian_unipager/templates/config.json.j2 according to your needs.
For example, if you use a raspager PCB, you will have to set the frequency correction.

If you want to use the web interface later, you can just skip this step.

### Provide call sign and API key via Ansible vault

Use ansible_vault_unencrypted_sample.yml as an example and save the content to an Ansible vault file.

Save the vault file to groups_vars/all/unipager_vault.yml

Use this command:

```ansible-playbook site.yml --ask-become-pass --ask-vault-pass```

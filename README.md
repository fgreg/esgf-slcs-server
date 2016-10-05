# esgf-slcs-server

This package provides a SLCS server that can authenticate users in an ESGF user database.

This server provides a SLCS service using the [Online CA service](https://github.com/cedadev/online_ca_service),
accessible using OAuth and Basic Auth credentials.


## Deploying a SLCS Server

The ESGF SLCS server is deployed using an [Ansible playbook](https://www.ansible.com/).
This playbook can be configured to deploy a development machine using [Vagrant](https://www.vagrantup.com/)
or a production machine using the regular Ansible inventory system.

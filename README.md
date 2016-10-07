# esgf-slcs-server

This package provides a SLCS server that can provide short-lived X509 certificates
for users in an ESGF user database.

Certificates can be obtained using two authentication methods:

  * Username and password using HTTP Basic Auth
  * OAuth2 delegated authority

The OAuth2 support allows a 3rd party service to obtain permission from a user to
obtain a certificate on their behalf without having to know the user's password.

The ESGF SLCS server is a Django application that utilises a number of other useful packages:

  * The "certificate authority over HTTP" functionality is provided by the
    [ContrailOnlineCAService package](https://github.com/cedadev/online_ca_service)
  * `ContrailOnlineCAService` provides a WSGI application which is mounted into Django
    using [django-wsgi](https://pythonhosted.org/django-wsgi/)
  * The OAuth token handling functionality is provided by the
    [django-oauth-toolkit](https://django-oauth-toolkit.readthedocs.io/en/latest/)


## Deploying a SLCS Server

The ESGF SLCS server is deployed using an [Ansible playbook](https://www.ansible.com/),
which is also [available on Github](https://github.com/cedadev/esgf-slcs-server-playbook).

This playbook can be configured to deploy a development machine using
[Vagrant](https://www.vagrantup.com/), or a production machine using the regular
Ansible inventory system.

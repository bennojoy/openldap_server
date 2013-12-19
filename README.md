openldap_server
===============

This roles installs the OpenLDAP server on the target machine. It has the
option to enable/disable SSL by setting it in defaults or overriding it.

Requirements
------------

This role requires Ansible 1.4 or higher, and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables that can be passed to this role and a brief description about
them are as follows:

    domain_name: example.com    # The domain prefix for ldap
    rootpw: passme              # This is the password for admin for openldap
    enable_ssl: true            # To enable/disable ssl for the ldap
    country: US                 # The self signed ssl certificate parameters
    state: Oregon
    location: Portland
    organization: IT


Examples
--------

1) Configure an OpenLDAP server without SSL:

    - hosts: all
      roles:
      - role: openldap_server
        domain_name: example.com
        rootpw: passme
        enable_ssl: false
       
2) Configure an OpenLDAP server with SSL:

    - hosts: all
      roles:
      - role: openldap_server
        domain_name: example.com
        rootpw: passme
        enable_ssl: true
        country: US
        state: Oregon
        location: Portland
        organization: IT

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Benno Joy



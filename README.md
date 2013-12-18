openldap_server
========

This roles installs openldap server on the Target. It has the option to enable/disable ssl
by setting it in defaults or overriding it.

Requirements
------------

This role requires ansible 1.4 or higher and platform requirements are listed in the metadata file

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

```
domain_name: example.com               # The domain prefix for ldap
rootpw: passme                         # This is the password for admin for openldap

enable_ssl: true                       # To enable/disable ssl for the ldap
country: US                            # The self signed ssl certificate parameters
state: oregon
location: portland
organization: IT
```

- Example

1) Configure an Openldap server without ssl

```
  - hosts: all
    roles:
     - role: openldap_server
       domain_name: example.com
       rootpw: passme
       enable_ssl: false
       
```

1) Configure an Openldap server with ssl
```
  - hosts: all
    roles:
     - role: openldap_server
       domain_name: example.com
       rootpw: passme
       enable_ssl: true
       country: US                           
       state: oregon
       location: portland
       organization: IT
       
```

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Benno Joy



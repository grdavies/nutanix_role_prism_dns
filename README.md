Nutanix Role for Prism DNS server configuration
=========

This Ansible role sets the DNS configuration for Prism Element and Prism Central.


Role Variables
--------------

| Variable                 | Required | Default | Choices                                                                         | Comments                                                                                                                                           |
|--------------------------|----------|---------|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| validate_certs           | no       | no      |                                                                                 | Whether to check if Prism UI certificates are valid.                                                                                               |
| prism_dns_server_list    | yes      | []      |                                                                                 | Provide a list of DNS server IP addresses; ["8.8.8.8", "8.8.4.4"].                                                                                 |

Dependencies
------------

- grdavies.nutanix_role_prism_init_api

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```     - hosts: localhost
       gather_facts: false
       roles:
         - role: grdavies.nutanix_role_prism_init_api
         - role: ../..
       vars:
         prism_ip: 10.38.185.37
         prism_username: admin
         prism_password: nx2Tech165!
         prism_dns_server_list:
           - 8.8.8.8
           - 8.8.4.4
```


License
-------

See LICENSE.md

Author Information
------------------

Ross Davies

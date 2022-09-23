# Nutanix Role for Prism DNS server configuration

This Ansible role sets the DNS server configuration for Prism Element and Prism Central.


## Role Variables

| Variable                 | Required | Default | Choices                                                                         | Comments                                                                                                                                           |
|--------------------------|----------|---------|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| validate_certs           | no       | no      |                                                                                 | Whether to check if Prism UI certificates are valid.                                                                                               |
| nutanix_dns_server_list  | yes      | []      |                                                                                 | Provide a list of DNS server IP addresses; ["8.8.8.8", "8.8.4.4"].                                                                                 |

## Dependencies

- grdavies.nutanix_role_nutanix_init_api

## Example Playbook

```
- hosts: localhost
  gather_facts: false
  roles:
    - role: grdavies.nutanix_role_nutanix_dns
  vars:
    nutanix_host: 10.38.185.37
    nutanix_password: admin
    nutanix_username: nx2Tech165!
    nutanix_dns_server_list:
      - 8.8.8.8
      - 8.8.4.4
```

## License

See LICENSE.md

## Author Information

Ross Davies

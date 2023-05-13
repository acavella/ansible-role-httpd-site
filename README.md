# Ansible Role: HTTPd Site

![CI](https://github.com/acavella/ansible-role-httpd-site/actions/workflows/ci.yml/badge.svg)
![GitHub last commit](https://img.shields.io/github/last-commit/acavella/ansible-role-httpd-site)
![GitHub repo size](https://img.shields.io/github/repo-size/acavella/ansible-role-httpd-site)

An Ansible Role to install and configure an HTTPd VirtualHost implementing configuration best practices and STIG settings.

## Requirements

| Name | Version | Notes |
| ----- | ----- | ----- |
| Red Hat Enterprise Linux | 7,8,9 | NA |
| Apache HTTPd | 2.4.x | NA |
| Ansible | 2.9+ | NA |

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
# Specifies the fqdn the virtual host responds to queries.
httpd_host_fqdn: example.com
# Defines variations of the fqdn that you also want the server to respond to.
httpd_host_alias: www.example.com
# Specifies an administrative email address responsible for the server.
httpd_host_email: admin@example.com
# Specifies the IP address of the network adaptor to listen.
httpd_host_ip: 10.25.0.115
# Specifies the port the host should listen on.
httpd_host_port: 80
# Specifies whether the virtual host should be tls encrypted or not.
httpd_host_encrypted: false
# Specifies the location of the server certificate, only used when httpd_host_encrypted.
httpd_host_certificate: 
# Specifies the location of the server private key, only used when httpd_host_encrypted.
httpd_host_key: 
# Specifies the location of trustchain, only used when httpd_host_encrypted.
httpd_host_chain: 
```

## Dependencies

None.

## Example Playbook

```yaml
- hosts: localhost
  roles:
    - { role: acavella.httpd-site }
```
## License

GNU General Public License v3.0

## Author Information

This role was created in 2023 by [Tony Cavella](https://www.cavella.com/)

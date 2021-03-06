ssl_certs
=========
[![Build Status](https://travis-ci.org/shoneslab/ansible-role-ssl_certs.svg?branch=master)](https://travis-ci.org/shoneslab/ansible-role-ssl_certs)

This ansible role is to create self signed ssl certs.

Requirements
------------

This role requires Ansible 2.2 or higher and platform requirements are listed in the metadata file.

Role Variables
--------------
csr config file information
```
ssl_certs_conf_country_name: 'US'
ssl_certs_conf_state: 'Georgia'
ssl_certs_conf_locality: 'Atlanta'
ssl_certs_conf_postal_code: '30338'
ssl_certs_conf_org_name: 'shoneslab'
ssl_certs_conf_org_unit_name: 'devops'
ssl_certs_conf_common_name: '*.vagrant.local'
ssl_certs_conf_email: 'devops@shoneslab.com'

ssl_certs_conf_default_bits: 4096
ssl_certs_conf_default_md: 'sha512'
ssl_certs_conf_defauly_keyfile: 'key.pem'
ssl_certs_conf_prompt: 'no'
ssl_certs_conf_encrypt_key: 'no'
```

Details about ssl directory and csr
```
ssl_certs_root_private_key_dir: '/etc/ssl/private'
ssl_certs_root_private_key: 'rootCA.key'
ssl_certs_root_ssl_cert: 'rootCA.pem'
ssl_certs_root_cert_days: 3650
ssl_certs_device_key_dir: '/etc/ssl/device'
ssl_certs_device_key: 'device.key'
ssl_certs_device_csr: 'device.csr'
ssl_certs_device_crt: 'device.crt'
ssl_certs_cert_days: 3650
```

Dependencies
------------

None

Example Playbook
----------------
```
- hosts: all
  roles:
    - role: ansible-role-ssl_certs
```
License
-------

BSD, MIT

Author Information
------------------

Shone Jacob

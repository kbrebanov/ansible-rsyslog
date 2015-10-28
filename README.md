rsyslog
=======

[![Ansible Role](https://img.shields.io/ansible/role/3392.svg)](https://galaxy.ansible.com/list#/roles/3392)

Installs and configures rsyslog

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                                    | Default                       | Description                                   |
|-----------------------------------------|-------------------------------|-----------------------------------------------|
| rsyslog_repeated_msg_reduction          | "on"                          | Enable/disable repeated msg redution          |
| rsyslog_action_file_default_template    | RSYSLOG_TraditionalFileFormat | Action file default template                  |
| rsyslog_klog_permit_non_kernel_facility | "on"                          | Enable/disable logging of non kernel facility |
| rsyslog_udp_enable                      | false                         | Enable or disable rsyslog to listen on UDP    |
| rsyslog_udp_address                     | 127.0.0.1                     | Address to bind to for UDP                    |
| rsyslog_udp_port                        | 514                           | UDP port                                      |
| rsyslog_tcp_enable                      | false                         | Enable or disable rsyslog to listen on TCP    |
| rsyslog_tcp_port                        | 514                           | TCP port                                      |

Dependencies
------------

None

Example Playbook
----------------

Install rsyslog
```
- hosts: all
  roles:
    - { role: kbrebanov.rsyslog }
```

Install rsyslog and disable repeated msg reduction
```
- hosts: all
  roles:
    - { role: kbrebanov.rsyslog, rsyslog_repeated_msg_reduction: "off" }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov

rsyslog
=======

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

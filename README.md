Custom Facts
============

Simple role to install custom facts

Requirements
------------

`jq` package is required for LVM custom facts

Role Variables
--------------

By default the role installs hard coded or dynamic custom facts:

```
custom_facts__templates:
  - groups

custom_facts__scripts:
  - current_active_users
  - current_sudo_users
```


More custom facts can be defined 

```
custom_facts__additional_templates:
  - item1
  - item2
```

Dependencies
------------

N/A

Example Playbook
----------------

When setting up a new machine, you can use:

```
- hosts: all
  name: Custom facts setup
  roles:
    - role: custom_facts
```

License
-------

GPL v3

Author Information
------------------

François TOURDE

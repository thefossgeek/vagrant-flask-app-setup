supervisor-ansible-role
=======================

An Ansible Role that installs Supervisor (process state manager) on Linux.

Requirements
------------

Nil

Role Variables
--------------

Available variables are documented along with default values (please see `defaults/main.yml`)

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: supervisor-ansible-role }

License
-------

MIT

Author Information
------------------

Mohan L <thefossgeek@gmail.com>

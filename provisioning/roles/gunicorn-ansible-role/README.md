gunicorn-ansible-role
=====================

An Ansible role for installing and configuring gunicorn. Provides the `Restart gunicorn` handler to reload gunicorn when you install/update your app.

Requirements
------------

Nil

Role Variables
--------------

Available variables are documented along with default values (please see `defaults/main.yml`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: gunicorn-ansible-role }

License
-------

MIT

Author Information
------------------

Mohan L <thefossgeek@gmail.com>

[![Build Status](https://travis-ci.org/CSCfi/ansible-role-puppetize.svg?branch=master)](https://travis-ci.org/CSCfi/ansible-role-puppetize)

ansible-role-puppetize
=========

A role for bootstrapping puppet clients.

Requirements
------------

N/A

Role Variables
--------------

Dependencies
------------

Example Playbook
----------------

```
- hosts: backend_servers
  become: yes
  become_user: root
  roles:
    - ansible-role-puppetize
```

License
-------

MIT

Testing
-------

This bit is manual, we do some testing in this role already but it does not setup a puppetmaster+agent.

Basic environment needed: an agent and a puppetmaster on different VMs/tainers with different FQDNs.

When testing this role it's a good idea to run it on a node:
  - which is already puppetized from before
  - which is not puppetized before (generate CSR and sign the certificate)
  - where we only run some tasks with "puppet_run_only=True"

Author Information
------------------

CSC - IT Center for Science

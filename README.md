Yourls Ansible Role
===================

Ansible role to install Yourls (Your Own URL Shortener, PHP web app).

Requirements
------------

This role has no requirements by itself, but Yourls needs PHP and MySQL.

Role Variables
--------------

Since nested variables are used here, so to avoid defining the while vars,
it's recommended to set `hash_behaviour = merge` or pass env var `ANSIBLE_HASH_BEHAVIOUR=merge`
at Ansible execution.

Example Playbook
----------------

There are some variables that you need to set like site URL, DB info, users ... etc.
A specific Yourls version could be selected, if not, it will get latest Yourls version.

```
yourls:
  version: latest
  path: /var/html/yourls
  owner: root
  group: root
  db:
    name: yourls
    user: yourls_db_password
    pass: yourls_db_username
    host: localhost
    prefix: yourls_
  users:
    user01: user01_password
  conf:
    site: http://your-own-domain-here.com
```

License
-------

GNU GPL v2

Author Information
------------------

[Ahmed AbouZaid](http://tech.aabouzaid.com/).

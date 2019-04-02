pddg.postfix
=========

A role for deploying postfix with TLS

Requirements
------------

You have to have `sudo` permission.
Postfix deployed by this role require Dovecot to SASL authentication.

Role Variables
--------------

See [defaults](./defaults/main.yml)

Dependencies
------------

- pddg.dovecot


Example Playbook
----------------

```yaml
- hosts: all
  become: yes
  roles:
    - name: pddg.postfix
      vars:
        postfix_domain: your.domain
        postfix_tls_options:
          cert: path/to/.crt
          key: path/to/.key
          ca: path/to/.pem
```

License
-------

MIT

Author Information
------------------

[pddg](https://github.com/pddg/)
  - Web: [poyo.info](https://www.poyo.info/)


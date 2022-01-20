fail2ban
========

Installs and sets up fail2ban

Requirements
------------

Requires firwalld role

Role Variables
--------------

fail2ban_bantime: default ban duration
fail2ban_findtime: how far back logs are checked
fail2ban_maxretry: max retries
fail2ban_sshd_bantime: sshd ban duration
fail2ban_sshd_maxretry: sshd max retries

Dependencies
------------

Depends on firwalld role handlers

Example Playbook
----------------

```
- name: Playbook
  hosts: servers
  roles:
    - {
        role: fail2ban,
        fail2ban_bantime: 1h,
        fail2ban_findtime: 1h,
        fail2ban_maxretry: 5,
        fail2ban_sshd_bantime: 1d,
        fail2ban_sshd_maxretry: 3
      }
```

License
-------

GPLv3

Author Information
------------------

github: @nekwebdev

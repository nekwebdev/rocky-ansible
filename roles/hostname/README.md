hostname
========

Sets the hostname, timezone and locale.

Role Variables
--------------

host_hostname: fqdn
host_timezone: timezone
host_locale: locale
host_language: language

Example Playbook
----------------
```
- name: Playbook
  hosts: servers
  roles:
    - {
        role: hostname,
        host_hostname: "domain.ltd",
        host_timezone: "Pacific/Tahiti",
        host_locale: "en_US.UTF8",
        host_language: "en_US.UTF8"
      }
```

License
-------

GPLv3

Author Information
------------------

github: @nekwebdev

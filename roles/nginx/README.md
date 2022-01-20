nginx
=====

Install and configure nginx with ModSecurity and ssl certificates by certbot for base domain and www subdomain that redirects to no-www.

Requirements
------------

Requires firwalld role

Role Variables
--------------

nginx_hostname: fqdn
nginx_user: user that has ownership of nginx www files
nginx_linode_apitoken: linode api key for domains
nginx_certbot_email: email to get notifications

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
        role: nginx,
        nginx_hostname: "domain.ltd",
        nginx_user: "admin",
        nginx_linode_apitoken: "dhjifdhafiowehfiweUIhhbIHADBilYU",
        nginx_certbot_email: "hostmaster@domain.ltd",
      }
```

License
-------

GPLv3

Author Information
------------------

github: @nekwebdev

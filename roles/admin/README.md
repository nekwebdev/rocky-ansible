admin
=====

Creates a new admin user with a properly setup ssh folder with a set authorized_key.

Role Variables
--------------

admin_username: name for the created user
admin_password: password for the created user
admin_password_salt: provide a random salt for idempotency
admin_sshpub: public ssh key for the created user

Example Playbook
----------------
```
- name: Playbook
  hosts: servers
  roles:
    - {
        role: admin,
        admin_username: admin,
        admin_password: myadminpassword,
        admin_password_salt: "salt",
        admin_sshpub: "my super long ssh pub string"
      }
```

License
-------

GPLv3

Author Information
------------------

github: @nekwebdev

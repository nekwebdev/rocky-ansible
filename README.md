Ansible playbook and roles to configure a server running Rocky Linux 8.

Creates admin user, git user to host repos, installs nginx with ModSecurity and auto ssl certificates with certbot using linode dns api, also performs basic sshd hardening and configures fail2ban.

Basically a clean and secure Rocky 8 Linode web host that can also host your repos. nginx conf examples are installed for easy reverse proxy with ssl to your apps.

I like to have all my variables in a single `/vars/vault_vars.yml` encrypted file, check `/vars/vault_vars.yml.example`. It is ignored by git by default, change `.gitignore` to your needs.

Run inside virtual env
```
pip install ansible docker molecule[docker,lint]
```

You can then run `molecule create/converge/destroy` commands inside the roles.
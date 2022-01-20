git
===

Add a git user and sets up repositories for hosting.
git user will have a limited login shell.

Role Variables
--------------

git_username: name for git user
git_password: password for git user
git_password_salt: provide a random salt for idempotency
git_sshpub: public ssh key for the git user
git_root: root directory for repositories
git_repositories: list of repositories names to be created

Example Playbook
----------------
```
- name: Playbook
  hosts: servers
  roles:
    - {
        role: git,
        git_username: "git",
        git_password: "git",
        git_password_salt: "salt",
        git_sshpub: "ssh-ed25519 gFtal5ygVwCw6epC",
        git_root: "/repositories",
        git_repositories:
          - repo1.git
          - repo2.git
      }
```

License
-------

GPLv3

Author Information
------------------

github: @nekwebdev

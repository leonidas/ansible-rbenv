rbenv
========

Install rbenv, ruby-build, ruby and ~/.gemrc with following content:

    gem: --no-document

.gemrc can be overriden by adding file files/rbenv/.gemrc to the playbook.

Requirements
------------

git, autoconf, bison, build-essential, libssl-dev, libyaml-dev, libreadline6, libreadline6-dev,
zlib1g, zlib1g-dev. Requirements are installed by the role.

Role Variables
--------------

* `rbenv.user` Remote user. Defaults to ansible `remote_user` or `sudo_user`
* `rbenv.version` rbenv version tag, or `HEAD`. Defaults to `v0.4.0`
* `rbenv.node_version` ruby version. Defaults to `2.0.0-p247`

Dependencies
------------

No depedencies.

Example Playbook
-------------------------

    - hosts: servers
      roles:
        - role: rbenv
          rbenv:
            user: deploy
            version: v0.4.0
            ruby_version: 2.0.0-p247

License
-------

BSD

Author Information
------------------

Jarno Keskikangas

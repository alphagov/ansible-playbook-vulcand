vulcand
=========

An ansible role to install a [vulcand](https://docs.vulcand.io/) server.

This is alpha quality and installs from a tarball. You probably don't want
to use it.

Requirements
------------

Only tested on Ubuntu 14.04.


Role Variables
--------------

- `vulcand_version`: version to install, e.g. `v0.8.0-beta.3`
- `vulcand_arch`: architecture to install, e.g. `linux-amd64`
- `vulcand_args`: hash of CLI arguments, e.g. `{ port: 8080 }`

Dependencies
------------

* None

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: vulcand
           vulcand_args:
             etcd: http://localhost:2379
             port: 8080
             apiPort: 8081

License
-------

See `LICENSE` file.

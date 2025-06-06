Ansible Role: Go language SDK
=============================

[![Tests](https://github.com/gantsign/ansible-role-golang/workflows/Tests/badge.svg)](https://github.com/gantsign/ansible-role-golang/actions?query=workflow%3ATests)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-gantsign.golang-blue.svg)](https://galaxy.ansible.com/gantsign/golang)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/gantsign/ansible-role-golang/master/LICENSE)

Role to download and install the [Go language SDK](https://golang.org/).

Requirements
------------

* Ansible Core >= 2.17

* Linux Distribution

    * Debian Family

        * Debian

            * Bullseye (11)
            * Bookworm (12)

        * Ubuntu

            * Jammy (22.04)
            * Noble (24.04)

    * RedHat Family

        * Rocky Linux

            * 9

        * Fedora

            * 41

    * SUSE Family

        * openSUSE

            * Tumbleweed

    * Note: other versions are likely to work but have not been tested.

Role Variables
--------------

The following variables will change the behavior of this role (default values
are shown below):

```yaml
# Go language SDK version number
golang_version: '1.24.2'

# Mirror to download the Go language SDK redistributable package from
golang_mirror: 'https://storage.googleapis.com/golang'

# Base installation directory the Go language SDK distribution
golang_install_dir: '/opt/go/{{ golang_version }}'

# Directory to store files downloaded for Go language SDK installation
golang_download_dir: "{{ x_ansible_download_dir | default(ansible_facts.env.HOME + '/.ansible/tmp/downloads') }}"

# Location for GOPATH environment variable
golang_gopath:
```

### Supported Go language SDK Versions

The following versions of Go language SDK are supported without any additional
configuration (for other versions follow the Advanced Configuration
instructions):

* `1.24.2`
* `1.24.1`
* `1.24.0`
* `1.23.8`
* `1.23.7`
* `1.23.6`
* `1.23.5`
* `1.23.4`
* `1.23.3`
* `1.23.2`
* `1.23.1`
* `1.23.0`
* `1.22.11`
* `1.22.10`
* `1.22.9`
* `1.22.8`
* `1.22.7`
* `1.22.6`
* `1.22.5`
* `1.22.4`
* `1.22.3`
* `1.22.2`
* `1.22.1`
* `1.22.0`
* `1.21.13`
* `1.21.12`
* `1.21.11`
* `1.21.10`
* `1.21.9`
* `1.21.8`
* `1.21.7`
* `1.21.6`
* `1.21.5`
* `1.21.4`
* `1.21.3`
* `1.21.2`
* `1.21.1`
* `1.21.0`
* `1.20.13`
* `1.20.12`
* `1.20.11`
* `1.20.10`
* `1.20.9`
* `1.20.8`
* `1.20.7`
* `1.20.6`
* `1.20.5`
* `1.20.4`
* `1.20.3`
* `1.20.2`
* `1.20.1`
* `1.20`
* `1.19.12`
* `1.19.11`
* `1.19.10`
* `1.19.9`
* `1.19.8`
* `1.19.7`
* `1.19.6`
* `1.19.5`
* `1.19.4`
* `1.19.3`
* `1.19.2`
* `1.19.1`
* `1.19`
* `1.18.10`
* `1.18.9`
* `1.18.8`
* `1.18.7`
* `1.18.6`
* `1.18.5`
* `1.18.4`
* `1.18.3`
* `1.18.2`
* `1.18.1`
* `1.18`
* `1.17.13`
* `1.17.12`
* `1.17.11`
* `1.17.10`
* `1.17.9`
* `1.17.8`
* `1.17.7`
* `1.17.6`
* `1.17.5`
* `1.17.4`
* `1.17.3`
* `1.17.2`
* `1.17.1`
* `1.17`
* `1.16.15`
* `1.16.14`
* `1.16.13`
* `1.16.12`
* `1.16.11`
* `1.16.10`
* `1.16.9`
* `1.16.8`
* `1.16.7`
* `1.16.6`
* `1.16.5`
* `1.16.4`
* `1.16.3`
* `1.16.2`
* `1.16.1`
* `1.16`
* `1.15.15`
* `1.15.14`
* `1.15.13`
* `1.15.12`
* `1.15.11`
* `1.15.10`
* `1.15.9`
* `1.15.8`
* `1.15.7`
* `1.15.6`
* `1.15.5`
* `1.15.4`
* `1.15.3`
* `1.15.2`
* `1.15.1`
* `1.15`
* `1.14.15`
* `1.14.14`
* `1.14.13`
* `1.14.12`
* `1.14.11`
* `1.14.10`
* `1.14.9`
* `1.14.8`
* `1.14.7`
* `1.14.6`
* `1.14.5`
* `1.14.4`
* `1.14.3`
* `1.14.2`
* `1.14.1`
* `1.14`
* `1.13.15`
* `1.13.14`
* `1.13.13`
* `1.13.12`
* `1.13.11`
* `1.13.10`
* `1.13.9`
* `1.13.8`
* `1.13.7`
* `1.13.6`
* `1.13.5`
* `1.13.4`
* `1.13.3`
* `1.13.2`
* `1.13.1`
* `1.13`
* `1.12.17`
* `1.12.16`
* `1.12.15`
* `1.12.14`
* `1.12.13`
* `1.12.12`
* `1.12.11`
* `1.12.10`
* `1.12.9`
* `1.12.8`
* `1.12.7`
* `1.12.6`
* `1.12.5`
* `1.12.4`
* `1.12.3`
* `1.12.2`
* `1.12.1`
* `1.12`
* `1.11.13`
* `1.11.12`
* `1.11.11`
* `1.11.10`
* `1.11.9`
* `1.11.8`
* `1.11.7`
* `1.11.6`
* `1.11.5`
* `1.11.4`
* `1.11.3`
* `1.11.2`
* `1.11.1`
* `1.11`
* `1.10.8`
* `1.10.7`
* `1.10.6`
* `1.10.5`
* `1.10.4`
* `1.10.3`
* `1.10.2`
* `1.10.1`
* `1.10`
* `1.9.7`
* `1.9.6`
* `1.9.5`
* `1.9.4`
* `1.9.3`
* `1.9.2`
* `1.9.1`
* `1.9`
* `1.8.7`
* `1.8.6`
* `1.8.5`
* `1.8.4`
* `1.8.3`
* `1.8.2`
* `1.8.1`
* `1.8`
* `1.7.4`
* `1.7.3`

Advanced Configuration
----------------------

The following role variable is dependent on the Go language SDK version; to use
a Go language SDK version **not pre-configured by this role** you must configure
the variable below:

```yaml
# SHA256 sum for the redistributable package (i.e. "go{{ golang_version }}.linux-amd64.tar.gz")
golang_redis_sha256sum: '6e3e9c949ab4695a204f74038717aa7b2689b1be94875899ac1b3fe42800ff82'
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - role: gantsign.golang
       golang_gopath: '$HOME/workspace-go'
```

Role Facts
----------

This role exports the following Ansible facts for use by other roles:

* `ansible_local.golang.general.version`

    * e.g. `1.7.3`

* `ansible_local.golang.general.home`

    * e.g. `/opt/golang/1.7.3`

More Roles From GantSign
------------------------

You can find more roles from GantSign on
[Ansible Galaxy](https://galaxy.ansible.com/ui/standalone/namespaces/2463/).

Development & Testing
---------------------

This project uses the following tooling:
* [Molecule](http://molecule.readthedocs.io/) for orchestrating test scenarios
* [Testinfra](http://testinfra.readthedocs.io/) for testing the changes on the
  remote
* [pytest](http://docs.pytest.org/) the testing framework
* [Tox](https://tox.wiki/en/latest/) manages Python virtual
  environments for linting and testing
* [pip-tools](https://github.com/jazzband/pip-tools) for managing dependencies

A Visual Studio Code
[Dev Container](https://code.visualstudio.com/docs/devcontainers/containers) is
provided for developing and testing this role.

License
-------

MIT

Author Information
------------------

John Freeman

GantSign Ltd.
Company No. 06109112 (registered in England)

[![MIT License](https://raw.githubusercontent.com/roles-ansible/ansible_role_base/master/.github/license.svg?sanitize=true)](https://github.com/roles-ansible/ansible_role_base/blob/master/LICENSE) | [![Ansible Lint check](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-linting-check.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-linting-check.yml) | [![Galaxy release](https://github.com/roles-ansible/ansible_role_base/actions/workflows/galaxy.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/galaxy.yml)

Ansible Role to install packages
---------------------

A base ansible role that should run on common Linux systems.

This role adds more package sources to Debian. And installs some useful tools. This role adds more package sources to Debian. And installs some useful tools. The complete list of tools to install can be found in the [vars/main.yml](https://github.com/roles-ansible/ansible_role_base/blob/master/vars/main.yml).

Optionally you can also set vim as the default editor and update all packages to ``latest``.


### variables:

For a complete overview of all variables have a deeper look into the ``vars`` nd the ``defaults`` Folder!.

```yml
---
# install these additional packages
base__extra_packages: []
# - foo
# - bar

# should we add additional package source?
base__add_ethz: true

# add nonfree/firmware packages?
base__pkg_non_free_firmware: false
base__pkg_contrib: false

# optionaly print some OS vars
base__print_os_vars: false

# choose latest or present for package state
# set this to latest for updating all packages!
base__package_state: 'present'

# should we update all packages?
base__upgrade_packages_to_latest_version: false

# install keychain (ssh agent)
base__install_keychain: true

# install vim (comand line editor)
base__install_vim: true

# perform a simple versions check (true is recomended)
submodules_versioncheck: false
```

### testing
This role is tested with [these github-action](https://github.com/search?q=topic%3Acheck-ansible+topic%3Agithub-actions+org%3Aroles-ansible&type=Repositories) tests for different versions of differen linux systems.
If you want to find out more about our tests, please have a look at the github marketplace.

| test status | Github Marketplace |
| :---------  | :----------------  |
| [![Galaxy release](https://github.com/roles-ansible/ansible_role_base/actions/workflows/galaxy.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/galaxy.yml) | [publish-ansible-role-to-galaxy](https://github.com/marketplace/actions/publish-ansible-role-to-galaxy) |
| [![Yamllint GitHub Actions](https://github.com/roles-ansible/ansible_role_base/actions/workflows/yamllint.yaml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/yamllint.yaml) | [yamllint-github-action](https://github.com/marketplace/actions/yamllint-github-action) |
| [![Ansible Lint check](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-linting-check.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-linting-check.yml) | [ansible-lint action](https://github.com/marketplace/actions/ansible-lint)
| [![Ansible check debian:latest](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-debian-latest.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-debian-latest.yml) | [ansible test with debian stable](https://github.com/marketplace/actions/check-ansible-debian-stable) |
| [![Ansible check debian:latest](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20debian:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+debian%3Alatest%22) | [ansible test with debian latest](https://github.com/marketplace/actions/check-ansible-debian-latest) |
| [![Ansible check debian:sid](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-debian-sid.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-debian-sid.yml) | [ansible test with debian sid](https://github.com/marketplace/actions/check-ansible-debian-sid) |
| [![Ansible check debian:stable](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-debian-stable.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-debian-stable.yml) | [ansible test with debian stable](https://github.com/marketplace/actions/check-ansible-debian-stable) |
| [![Ansible check debian:buster](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-debian-buster.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-debian-buster.yml) | [ansible test with debian buster](https://github.com/marketplace/actions/check-ansible-debian-buster) |
| | |
| [![Ansible check archlinux:latest](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-archlinux-latest.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-archlinux-latest.yml) | [ansible test with archlinux latest](https://github.com/marketplace/actions/check-ansible-archlinux-latest) |
| | |
| [![Ansible check ubuntu:latest](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-ubuntu-latest.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-ubuntu-latest.yml) | [ansible test with ubuntu latest](https://github.com/marketplace/actions/check-ansible-ubuntu-latest) |
| [![Ansible check ubuntu:bionic](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-ubuntu-bionic.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-ubuntu-bionic.yml) | [ansible test with ubuntu bionic](https://github.com/marketplace/actions/check-ansible-ubuntu-bionic) |
| [![Ansible check ubuntu:trusty](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-ubuntu-trusty.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-ubuntu-trusty.yml) | [ansible test with ubuntu trusty](https://github.com/marketplace/actions/check-ansible-ubuntu-trusty) |
| | |
| [![Ansible check fedora:latest](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-fedora-latest.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-fedora-latest.yml) | [ansible test with fedora latest](https://github.com/marketplace/actions/check-ansible-fedora-latest) |
| [![Ansible check fedora:33](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-fedora-33.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-fedora-33.yml) | [ansible test with fedora 33](https://github.com/marketplace/actions/check-ansible-fedora-33) |
| [![Ansible check fedora:32](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-fedora-32.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-fedora-32.yml) | [ansible test with fedora 32](https://github.com/marketplace/actions/check-ansible-fedora-32) |
| [![Ansible check fedora:31](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-fedora-31.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-fedora-31.yml) | [ansible test with fedora 31](https://github.com/marketplace/actions/check-ansible-fedora-31) |
| | |
| [![Ansible check centos:latest](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-centos-latest.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-centos-latest.yml) | [ansible test with centos latest](https://github.com/marketplace/actions/check-ansible-centos-latest) |
| [![Ansible check centos:centos8](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-centos-centos8.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-centos-centos8.yml) | [ansible test with centos centos8](https://github.com/marketplace/actions/check-ansible-centos-centos8) |
| [![Ansible check centos:centos7](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-centos-centos7.yml/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions/workflows/ansible-centos-centos7.yml) | [ansible test with centos centos7](https://github.com/marketplace/actions/check-ansible-centos-centos7) |

[![MIT License](https://raw.githubusercontent.com/roles-ansible/ansible_role_base/master/.github/license.svg?sanitize=true)](https://github.com/roles-ansible/ansible_role_base/blob/master/LICENSE)

Ansible Role to install packages
---------------------

A base ansible role that should run on common Linux systems.

This role adds more package sources to Debian. And installs some useful tools. This role adds more package sources to Debian. And installs some useful tools. The complete list of tools to install can be found in the [vars/main.yml](https://github.com/roles-ansible/ansible_role_base/blob/master/vars/main.yml).

Optionally you can also set vim as the default editor and update all packages to ``latest''.


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
This role is tested with [these github-action](https://github.com/search?q=topic%3Acheck-ansible+topic%3Agithub-actions+org%3Aroles-ansible&type=Repositories) tests for different versions of differen linux systems. Linting is tested via travis-ci and the  [ansible-lint action](https://github.com/marketplace/actions/ansible-lint).
If you want to find out more about our tests, please have a look at the github marketplace.

| test status | Github Marketplace |
| :---------  | :----------------  |
| [![Travis Build Status](https://travis-ci.com/roles-ansible/ansible_role_base.svg?branch=master)](https://travis-ci.com/roles-ansible/ansible_role_base) | [.travis.yml](https://github.com/roles-ansible/ansible_role_base/blob/master/.travis.yml) |
|||
| [![Ansible Lint check](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20Lint%20check/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+Lint+check%22) | [ansible-lint action](https://github.com/marketplace/actions/ansible-lint)
| [![Ansible check debian:stable](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20debian:stable/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+debian%3Astable%22) | [ansible test with debian stable](https://github.com/marketplace/actions/check-ansible-debian-stable) |
| [![Ansible check debian:latest](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20debian:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+debian%3Alatest%22) | [ansible test with debian latest](https://github.com/marketplace/actions/check-ansible-debian-latest) |
| [![Ansible check debian:sid](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20debian:sid/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+debian%3Asid%22) | [ansible test with debian sid](https://github.com/marketplace/actions/check-ansible-debian-sid) |
| [![Ansible check debian:buster](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20debian:buster/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+debian%3Abuster%22) | [ansible test with debian buster](https://github.com/marketplace/actions/check-ansible-debian-buster) |
| [![Ansible check debian:stretch](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20debian:stretch/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+debian%3Astretch%22) | [ansible test with debian stretch](https://github.com/marketplace/actions/check-ansible-debian-stretch) |
| | |
| [![Ansible check archlinux:latest](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20archlinux:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+archlinux%3Alatest%22) | [ansible test with archlinux latest](https://github.com/marketplace/actions/check-ansible-archlinux-latest) |
| | |
| [![Ansible check ubuntu:latest](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20ubuntu:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+ubuntu%3Alatest%22) | [ansible test with ubuntu latest](https://github.com/marketplace/actions/check-ansible-ubuntu-latest) |
| [![Ansible check ubuntu:bionic](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20ubuntu:bionic/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+ubuntu%3Abionic%22) | [ansible test with ubuntu bionic](https://github.com/marketplace/actions/check-ansible-ubuntu-bionic) |
| [![Ansible check ubuntu:eoan](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20ubuntu:eoan/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+ubuntu%3Aeoan%22) | [ansible test with ubuntu eoan](https://github.com/marketplace/actions/check-ansible-ubuntu-eoan) |
| [![Ansible check ubuntu:trusty](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20ubuntu:trusty/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+ubuntu%3Atrusty%22) | [ansible test with ubuntu trusty](https://github.com/marketplace/actions/check-ansible-ubuntu-trusty) |
| [![Ansible check ubuntu:xenial](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20ubuntu:xenial/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+ubuntu%3Axenial%22) | [ansible test with ubuntu xenial](https://github.com/marketplace/actions/check-ansible-ubuntu-xenial) |
| | |
| [![Ansible check fedora:latest](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20fedora:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+fedora%3Alatest%22) | [ansible test with fedora latest](https://github.com/marketplace/actions/check-ansible-fedora-latest) |
| [![Ansible check fedora:33](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20fedora:33/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+fedora%3A33%22) | [ansible test with fedora 33](https://github.com/marketplace/actions/check-ansible-fedora-33) |
| [![Ansible check fedora:32](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20fedora:32/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+fedora%3A32%22) | [ansible test with fedora 32](https://github.com/marketplace/actions/check-ansible-fedora-32) |
| [![Ansible check fedora:31](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20fedora:31/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+fedora%3A31%22) | [ansible test with fedora 31](https://github.com/marketplace/actions/check-ansible-fedora-31) |
| | |
| [![Ansible check centos:latest](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20centos:latest/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+centos%3Alatest%22) | [ansible test with centos latest](https://github.com/marketplace/actions/check-ansible-centos-latest) |
| [![Ansible check centos:centos8](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20centos:centos8/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+centos%3Acentos8%22) | [ansible test with centos centos8](https://github.com/marketplace/actions/check-ansible-centos-centos8) |
| [![Ansible check centos:centos7](https://github.com/roles-ansible/ansible_role_base/workflows/Ansible%20check%20centos:centos7/badge.svg)](https://github.com/roles-ansible/ansible_role_base/actions?query=workflow%3A%22Ansible+check+centos%3Acentos7%22) | [ansible test with centos centos7](https://github.com/marketplace/actions/check-ansible-centos-centos7) |

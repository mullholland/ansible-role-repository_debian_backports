# [Ansible role repository_debian_backports](#repository_debian_backports)

Adds the Debian Backports Repository (https://backports.debian.org/) to your system

|GitHub|Downloads|Version|
|------|---------|-------|
|[![github](https://github.com/mullholland/ansible-role-repository_debian_backports/actions/workflows/molecule.yml/badge.svg)](https://github.com/mullholland/ansible-role-repository_debian_backports/actions/workflows/molecule.yml)|[![downloads](https://img.shields.io/ansible/role/d/mullholland/repository_debian_backports)](https://galaxy.ansible.com/mullholland/repository_debian_backports)|[![Version](https://img.shields.io/github/release/mullholland/ansible-role-repository_debian_backports.svg)](https://github.com/mullholland/ansible-role-repository_debian_backports/releases/)|
## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/mullholland/ansible-role-repository_debian_backports/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true
  # vars:
  #   example_var: "value"
  roles:
    - role: "mullholland.repository_debian_backports"
```



## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/mullholland/ansible-role-repository_debian_backports/blob/master/defaults/main.yml):

```yaml
---
# Possible Ubuntu releases
#  bionic
#  devel
#  eoan
#  focal
#  groovy
#  hirsute
#  precise
#  trusty
#  xenial
# Possible Debian releases
#  bullseye
#  buster
#  stretch
repository_debian_backports_releases: "{{ ansible_distribution_release }}"

# Only Debian not Ubuntu
repository_debian_backports_sloppy: false
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/mullholland/ansible-role-repository_debian_backports/blob/master/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://mullholland.net) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/mullholland/ansible-role-repository_debian_backports/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/mullholland):

|container|tags|
|---------|----|
|[Debian](https://hub.docker.com/r/mullholland/debian)|all|
|[Ubuntu](https://hub.docker.com/r/mullholland/ubuntu)|all|

The minimum version of Ansible required is 2.10, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/mullholland/ansible-role-repository_debian_backports/issues).

## [License](#license)

[MIT](https://github.com/mullholland/ansible-role-repository_debian_backports/blob/master/LICENSE).

## [Author Information](#author-information)

[Mullholland](https://mullholland.net)

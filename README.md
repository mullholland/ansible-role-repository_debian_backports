# [repository_debian_backports](#repository_debian_backports)

|GitHub|GitLab|
|------|------|
|[![github](https://github.com/mullholland/ansible-role-repository_debian_backports/workflows/Ansible%20Molecule/badge.svg)](https://github.com/mullholland/ansible-role-repository_debian_backports/actions)|[![gitlab](https://gitlab.com/mullholland/ansible-role-repository_debian_backports/badges/master/pipeline.svg)](https://gitlab.com/mullholland/ansible-role-repository_debian_backports)|[![quality](https://img.shields.io/ansible/quality/unset)](https://galaxy.ansible.com/mullholland/repository_debian_backports)|

description

## [Role Variables](#role-variables)

These variables are set in `defaults/main.yml`:
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


## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
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





## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/mullholland):

-   [debian9](https://hub.docker.com/r/mullholland/docker-molecule-debian9)
-   [debian10](https://hub.docker.com/r/mullholland/docker-molecule-debian10)
-   [debian11](https://hub.docker.com/r/mullholland/docker-molecule-debian11)
-   [ubuntu1804](https://hub.docker.com/r/mullholland/docker-molecule-ubuntu1804)
-   [ubuntu2004](https://hub.docker.com/r/mullholland/docker-molecule-ubuntu2004)
-   [ubuntu2204](https://hub.docker.com/r/mullholland/docker-molecule-ubuntu2204)

The minimum version of Ansible required is 2.10, tests have been done to:

-   The previous versions.
-   The current version.
-   The [devel](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-devel-from-github-with-pip) version.



## [Exceptions](#exceptions)

Some variations of the build matrix do not work. These are the variations and reasons why the build won't work:

| variation                 | reason                 |
|---------------------------|------------------------|
| CentOS | Backports repositories only support Debian/Ubuntu |
| RedHat | Backports repositories only support Debian/Ubuntu |
| Almalinux | Backports repositories only support Debian/Ubuntu |
| RockyLinux | Backports repositories only support Debian/Ubuntu |
| AmazonLinux | Backports repositories only support Debian/Ubuntu |


If you find issues, please register them in [GitHub](https://github.com/mullholland/ansible-role-repository_debian_backports/issues)

## [License](#license)

MIT


## [Author Information](#author-information)

[Mullholland](https://github.com/mullholland)

## [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)

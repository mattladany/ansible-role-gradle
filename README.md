# Ansible Role - Gradle

![CI](https://github.com/mattladany/ansible-role-gradle/actions/workflows/ci.yml/badge.svg)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://raw.githubusercontent.com/mattladany/ansible-role-gradle/master/LICENSE)

A very simple ansible role that manually installs [gradle](https://gradle.org) on CentOS Linux.

## Requirements

- unzip - will be installed using the OS default package manager.
- Java - recommended role for Java installation: `geerlingguy.java`.

## Role Variables

Available variables are listed below, along with their default values (see ```defaults/main.yml```):

```gradle_version: 6.3.8```

Set this to the version of gradle you would like to install. See [here](https://gradle.org/releases/) for a list of gradle releases.

```gradle_install_dir: /opt```

Where the gradle zip should be unpacked to.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - geerlingguy.java
    - mattladany.gradle
```

## License

[MIT](https://raw.githubusercontent.com/mattladany/ansible-role-gradle/master/LICENSE)

## Author Information

This role was created by Matt Ladany.

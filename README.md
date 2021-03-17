# Ansible Role - Gradle

![CI](https://github.com/mattladany/ansible-role-gradle/actions/workflows/ci.yml/badge.svg)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://raw.githubusercontent.com/mattladany/ansible-role-gradle/master/LICENSE)

An Ansible role that manually installs [gradle](https://gradle.org) on Centos Linux.

## Requirements

Requires Java; recommended role for Java installation: `geerlingguy.java`.

## Role Variables

Available variables are listed below, along with their default values (see ```defaults/main.yml```):

```gradle_version: 6.3.8```

Set this to the version of gradle you would like to install. See [here](https://gradle.org/releases/) for a list of gradle releases.

```gradle_install_dir: /opt```

Where the gradle zip should be unpacked to.

```gradle_bin_path: "{{ gradle_install_dir }}/gradle-{{ gradle_version }}/bin```

The path to gradle's bin directory. Should not be changed.

```gradle_download_url: "https://services.gradle.org/distributions/gradle-{{ gradle_version }}-bin.zip"```

The URL of which the gradle zip should be downloaded from. Should not be changed.

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

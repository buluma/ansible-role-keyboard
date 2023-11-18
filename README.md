# [Ansible role keyboard](#keyboard)

Role for configuring keyboard layout etc.

|GitHub|GitLab|Downloads|Version|Issues|Pull Requests|
|------|------|-------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-keyboard/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-keyboard/actions)|[![gitlab](https://gitlab.com/shadowwalker/ansible-role-keyboard/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-keyboard)|[![downloads](https://img.shields.io/ansible/role/d/4747)](https://galaxy.ansible.com/buluma/keyboard)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-keyboard.svg)](https://github.com/buluma/ansible-role-keyboard/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-keyboard.svg)](https://github.com/buluma/ansible-role-keyboard/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-keyboard.svg)](https://github.com/buluma/ansible-role-keyboard/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-keyboard/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all

  pre_tasks:
    - name: update apt cache
      ansible.builtin.apt:
        update_cache: yes
      changed_when: no

  roles:
    - role: buluma.keyboard
      keyboard_model: pc105
      keyboard_layout: brai
      keyboard_variant: right_hand
      keyboard_options: 'lv3:alt_switch,compose:rctrl'
      keyboard_backspace: guess
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-keyboard/blob/master/defaults/main.yml):

```yaml
---
# The XKB keyboard model name.
keyboard_model: pc104

# The XKB keyboard layout name.
keyboard_layout: us

# The XKB keyboard variant components.
keyboard_variant: ''

# The XKB keyboard option components.
keyboard_options: ''

# The behavior of <BackSpace> and <Delete> keys.
keyboard_backspace: guess
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-keyboard/blob/master/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-keyboard/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Ubuntu](https://hub.docker.com/repository/docker/buluma/ubuntu/general)|bionic, focal|
|[Debian](https://hub.docker.com/repository/docker/buluma/debian/general)|all|

The minimum version of Ansible required is 2.1, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-keyboard/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-keyboard/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-keyboard/blob/master/LICENSE).

## [Author Information](#author-information)

[Michael Buluma](https://buluma.github.io/)

Please consider [sponsoring me](https://github.com/sponsors/buluma).

### [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)

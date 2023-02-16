# Arch linux ansible setup

My personal barebones setup script for a fresh Arch linux. This is meant as a replacement for the ["Post Installation"](https://wiki.archlinux.org/title/installation_guide#Post-installation) part of the installation.

## Requirements

A raw installation of Arch Linux with:

- `openssh`
- `python3`

## Role Variables

The variables are defined in `defaults/main.yml`. These should be configured as needed:

| Variable          | Default       | Info                                              |
| :---------------- | :------------ | :------------------------------------------------ |
| `arch_hostname`   | `test`        | Hostname of the system                            |
| `arch_user`       | `rein`        | User that will be created                         |
| `arch_user_pw`    | `linux`       | Password that will be prompted to change on login |
| `arch_groups`     | See defaults  | Groups the new user should be added to            |
| `packages_setup`  | See defaults  | General packages that should be installed         |
| `packages_gui`    | See defaimts  | GUI packages that should be installed             |

There is also a default option that will install a GUI (KDE-plasma) with my used software. 
This can be disabled:
```yml
enable_gui: false
```

## Warnings

The user will have a hardcoded password `linux` if unchanged.
**Please change this ASAP after using this role.**

## Example playbook

```yml
---
- name: test playbook
  hosts: general

  roles:
  - role: ansible-arch-setup
```

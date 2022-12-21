# Arch linux ansible setup

My personal barebones setup script for a fresh Arch linux. This is meant as a replacement for the ["Post Installation"](https://wiki.archlinux.org/title/installation_guide#Post-installation) part of the installation.

## Requirements

A raw installation of Arch Linux with:

- openssh
- python3

## Role Variables

The variables are defined in `defaults/main.yml`. These should be configured as needed:
    - hostname
    - user
    - groups
    - packages

There is also a default option that will install a GUI (KDE-plasma) with my used software. 
This can be disabled:
```yml
enable_gui: false
```

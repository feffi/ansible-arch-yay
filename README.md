# ansible-arch-yay

Ansible role to install yay AUR helper.

[![Build Status](https://img.shields.io/travis/feffi/ansible-arch-yay.svg)](https://travis-ci.org/feffi/ansible-arch-yay) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-arch-yay/total.svg)](https://github.com/feffi/ansible-arch-yay) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-arch-yay.svg?style=social&label=Fork)](https://github.com/feffi/ansible-arch-yay) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-arch-yay.svg?style=social&label=Star)](https://github.com/feffi/ansible-arch-yay) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-arch-yay.svg?style=social&label=Watch)](https://github.com/feffi/ansible-arch-yay) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-arch-yay/blob/master/LICENSE)

## Requirements

- Ansible 2.7.1
- pacman ;-)

### ansible.cfg

```yaml
hash_behaviour = merge
```

## Install

Just add the role to your ``requirements.yml`` file:

```yaml
- src: https://github.com/feffi/ansible-arch-yay.git
  name: ansible-arch-yay
```

## Role Defaults Variables

```yaml
ansible_arch_yay: {
  # The yay git source repository
  git: "https://aur.archlinux.org/yay.git",
  # The owner of the repository
  owner: {
    name: "feffi",
    group: "feffi"
  },
  # Destination to clone yay to
  dest: "/home/feffi/yay"
}
```

Example:

```yaml
- hosts: all
  vars:
    ansible_arch_yay:
      # The yay git source repository
      git: "https://aur.archlinux.org/yay.git"
      # The owner of the repository
      owner:
        name: "feffi"
        group: "feffi"
      # Destination to clone yay to
      dest: "/home/feffi/yay"
  roles:
    - { role: ansible-arch-yay }
```

# ansible-yay

Ansible role to install yay AUR helper.

[![Build Status](https://img.shields.io/travis/feffi/ansible-yay.svg)](https://travis-ci.org/feffi/ansible-yay) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-yay/total.svg)](https://github.com/feffi/ansible-yay) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-yay.svg?style=social&label=Fork)](https://github.com/feffi/ansible-yay) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-yay.svg?style=social&label=Star)](https://github.com/feffi/ansible-yay) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-yay.svg?style=social&label=Watch)](https://github.com/feffi/ansible-yay) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-yay/blob/master/LICENSE)
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
- src: https://github.com/feffi/ansible-yay.git
  name: ansible-yay
```

## Role Defaults Variables

```yaml
ansible_yay: {
}
```

Example:

```yaml
- hosts: all
  vars:
    ansible_yay:
  roles:
    - { role: ansible-yay }
```

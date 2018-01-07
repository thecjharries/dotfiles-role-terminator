# `dotfiles-role-terminator`
# `dotfiles-role-terminator`

[![Build Status](https://travis-ci.org/thecjharries/dotfiles-role-terminator.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-role-terminator)
[![Build Status](https://travis-ci.org/thecjharries/dotfiles-role-terminator.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-role-terminator)

## Requirements

Fedora 27 is recommended.

## Role Variables

Defaults are below.

```yml
---
owning_user: "{{ ansible_user }}"
owning_group: "{{ ansible_user }}"
root_dir: "/home/{{ ansible_user }}"
config_dir: "{{ root_dir }}/.config"
```

Additionally, these `vars` are set:

```yml
---
needed_packages:
  - terminator
```

## Dependencies

```yml
---
- src: git+https://github.com/thecjharries/dotfiles-role-common-software.git
- src: git+https://github.com/thecjharries/dotfiles-role-common-software.git
- src: git+https://github.com/thecjharries/dotfiles-role-package-installer.git
- src: git+https://github.com/thecjharries/dotfiles-role-package-installer.git
- src: git+https://github.com/thecjharries/dotfiles-role-generic-template.git
- src: git+https://github.com/thecjharries/dotfiles-role-generic-template.git
```

## Example Playbook

```yml
---
- hosts: all

  roles:
    - role: dotfiles-role-terminator
    - role: dotfiles-role-terminator
```

## License

ISC

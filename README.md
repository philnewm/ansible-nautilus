# Ansible Nautilus Role

[![Alma9-CI](https://github.com/philnewm/ansible-nautilus/actions/workflows/alma9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-nautilus/actions/workflows/alma9-ci-caller.yml) [![Rocky9-CI](https://github.com/philnewm/ansible-nautilus/actions/workflows/rocky9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-nautilus/actions/workflows/rocky9-ci-caller.yml) [![CentOSStream9-CI](https://github.com/philnewm/ansible-nautilus/actions/workflows/centosstream9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-nautilus/actions/workflows/centosstream9-ci-caller.yml) [![Debian12-CI](https://github.com/philnewm/ansible-nautilus/actions/workflows/debian12-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-nautilus/actions/workflows/debian12-ci-caller.yml) [![Ubuntu2204-CI](https://github.com/philnewm/ansible-nautilus/actions/workflows/ubuntu2204-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-nautilus/actions/workflows/ubuntu2204-ci-caller.yml)

This role includes a full vagrant based molecule testing setup at `molecule/default`

## Deprecated

This role only makes sense with a desktop environment and was tehrefore integrated into this [role](https://github.com/philnewm/ansible-gnome)

## Structure

```code
📦 ansible-nautilus
 ┣ 📂 defaults
 ┃ ┗ 📜 main.yml
 ┣ 📂 meta
 ┃ ┗ 📜 main.yml
 ┣ 📂 molecule
 ┃ ┗ 📂 default
 ┃   ┗ 📜, 📜, 📜, scenario_files
 ┣ 📂 tasks
 ┃ ┣ 📜 main.yml
 ┃ ┣ 📜 present.yml
 ┃ ┣ 📜 dependencies.yml
 ┃ ┣ 📜 absent.yml
 ┃ ┗ 📜 init.yml
 ┣ 📂 vars
 ┃ ┗ 📜 main.yml
 ┗ 🗒️ README.md
 ┗ 📓 requirements.txt

```

Describe and explain role structure.

## Requirements

This role needs an installed gnome desktop environment to be functional.

## Role Variables

* defaults/main.yml
  * nautilus_package - name of the nautilus package per linux os family
  * nautilus_settings - dconf related nautilus configuration
  * enable_plugins - plugin switch
  * nautilus_plugins - plugin list
* vars/main.yml
  * dependencies - to enable all features of this role

## Dependencies

This role doesn't depend on any additional ansible-galaxy roles

## Example Playbook

Add an example playbook

```yaml
---

tasks:
  - name: Include ansible-nautilus present
    ansible.builtin.include_role:
      name: ansible-nautilus
    vars:
      state: present

...
```

## License

Add license - if any.

# workspace

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/users)
[![General Workflow](https://github.com/rolehippie/users/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/users/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/users/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/users/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/users/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/users/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/users)](https://github.com/rolehippie/users/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.users-blue)](https://galaxy.ansible.com/rolehippie/users)

Ansible role to manage system users.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [users_bashit_version](#users_bashit_version)
  - [users_castles_force](#users_castles_force)
  - [users_enable_profile_load](#users_enable_profile_load)
  - [users_extra](#users_extra)
  - [users_general](#users_general)
  - [users_homeshick_version](#users_homeshick_version)
  - [users_ohmyzsh_version](#users_ohmyzsh_version)
  - [users_override_zshenv](#users_override_zshenv)
  - [users_packages_general](#users_packages_general)
  - [users_packages_zfs](#users_packages_zfs)
  - [users_packages_zsh](#users_packages_zsh)
  - [users_zfs_home](#users_zfs_home)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### users_bashit_version

Version of bash-it to install

#### Default value

```YAML
users_bashit_version: latest
```

### users_castles_force

Force to update homeshick castels

#### Default value

```YAML
users_castles_force: false
```

### users_enable_profile_load

Enable loading of profile.d within zshenv

#### Default value

```YAML
users_enable_profile_load: true
```

### users_extra

List of extra users

#### Default value

```YAML
users_extra: []
```

#### Example usage

```YAML
users_extra:
  - name: thomas
    primary_group: staff
    comment: Thomas Mustermann
    ansible.builtin.shell: /bin/bash
    castles:
      - tboerger/homeshick-base
      - name: tboerger/homeshick-osx
        force: True
    groups:
      - admin
    sshkeys:
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAINaQYR0/Oj6k1H03kshz2J7rlGCaDSuaGPhhOs9FcZfn tboerger@host1
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIC7oOi3qaDtfQVFhPKyd0Wk0C/y+QM71vtln8Rl44NlB tboerger@host2
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIFcPTmdo+7eK+8n2yE7Kx1vyQ4yJwHBngvQOt1MPhKhR tboerger@host3
  - name: buser
    primary_group: staff
    ansible.builtin.shell: /bin/bash
    bashit: True
    groups:
      - admin
  - name: zuser
    primary_group: staff
    ansible.builtin.shell: /bin/zsh
    ohmyzsh: True
    groups:
      - admin
  - name: user-to-delete
    remove: True
    state: absent
```

### users_general

List of global users

#### Default value

```YAML
users_general: []
```

#### Example usage

```YAML
users_general:
  - name: thomas
    primary_group: staff
    comment: Thomas Mustermann
    ansible.builtin.shell: /bin/bash
    castles:
      - tboerger/homeshick-base
      - name: tboerger/homeshick-osx
        force: True
    groups:
      - admin
    sshkeys:
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAINaQYR0/Oj6k1H03kshz2J7rlGCaDSuaGPhhOs9FcZfn tboerger@host1
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIC7oOi3qaDtfQVFhPKyd0Wk0C/y+QM71vtln8Rl44NlB tboerger@host2
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIFcPTmdo+7eK+8n2yE7Kx1vyQ4yJwHBngvQOt1MPhKhR tboerger@host3
  - name: buser
    primary_group: staff
    ansible.builtin.shell: /bin/bash
    bashit: True
    groups:
      - admin
  - name: zuser
    primary_group: staff
    ansible.builtin.shell: /bin/zsh
    ohmyzsh: True
    groups:
      - admin
  - name: user-to-delete
    remove: True
    state: absent
```

### users_homeshick_version

Version of homeshick to install

#### Default value

```YAML
users_homeshick_version: latest
```

### users_ohmyzsh_version

Version of bash-it to install

#### Default value

```YAML
users_ohmyzsh_version: latest
```

### users_override_zshenv

Override zshenv provided by system

#### Default value

```YAML
users_override_zshenv: true
```

### users_packages_general

List of general packages to install

#### Default value

```YAML
users_packages_general:
  - acl
  - bash
  - git
```

### users_packages_zfs

List of packages for zfs to install

#### Default value

```YAML
users_packages_zfs:
  - zsys
```

### users_packages_zsh

List of packages for zsh to install

#### Default value

```YAML
users_packages_zsh:
  - zsh
```

### users_zfs_home

Enable home on ZFS by zsysctl command

#### Default value

```YAML
users_zfs_home: false
```

## Discovered Tags

**_users_**

## Dependencies

- [ansible.posix](https://github.com/ansible-collections/ansible.posix)
- [community.general](https://github.com/ansible-collections/community.general)

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)

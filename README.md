# users

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/users) [![Build Status](https://img.shields.io/drone/build/rolehippie/users/master?logo=drone)](https://cloud.drone.io/rolehippie/users) [![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/users)](https://github.com/rolehippie/users/blob/master/LICENSE) 

Ansible role to manage system users. 

## Sponsor 

[![Proact Deutschland GmbH](https://proact.eu/wp-content/uploads/2020/03/proact-logo.png)](https://proact.eu) 

Building and improving this Ansible role have been sponsored by my employer **Proact Deutschland GmbH**.

## Table of content

* [Default Variables](#default-variables)
  * [users_castles_force](#users_castles_force)
  * [users_extra](#users_extra)
  * [users_general](#users_general)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

## Default Variables

### users_castles_force

Force to update homeshick castels

#### Default value

```YAML
users_castles_force: false
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
    shell: /bin/bash
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
    shell: /bin/bash
    bashit: True
    groups:
      - admin
  - name: zuser
    primary_group: staff
    shell: /bin/zsh
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
    shell: /bin/bash
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
    shell: /bin/bash
    bashit: True
    groups:
      - admin
  - name: zuser
    primary_group: staff
    shell: /bin/zsh
    ohmyzsh: True
    groups:
      - admin
  - name: user-to-delete
    remove: True
    state: absent
```

## Dependencies

* None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)

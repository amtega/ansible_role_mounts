# Ansible mounts role

This is an [Ansible](http://www.ansible.com) role which manages mount points through the mount module.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Example Playbook

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - amtega.mounts
  vars:    
    mounts:
      - path: /mnt/disk0
        src: /dev/disk0
        fstype: ext4
        opts: ro
        state: present

      - path: /mnt/disk1
        src: /dev/disk1
        fstype: ext4
        opts: ro
        state: present    
```

## Testing

Tests are based on [molecule with vagrant virtual machines](https://molecule.readthedocs.io/en/latest/installation.html).

```shell
cd amtega.mounts

molecule test --all
```

## License

Copyright (C) 2022 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Juan Antonio Valiño García.

ssh_keys
========

This role adds and/or removes ssh keys of a user.

Notes
-----

* Please be aware that it runs on root per default.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

| Name                | Comment                          | Default value |
|---------------------|----------------------------------|---------------|
| ssh_keys_user       | Which user will be configured    | `root`        |
| ssh_keys_to_add     | A list of SSH keys to be present |               |
| ssh_keys_to_remove  | A list of SSH keys to be absent  |               |

Example Playbook
----------------

```yaml
- name: SSH Keys
  hosts: servers
  roles:
    - role: oxivanisher.ssh_keys
      tags:
        - basic_access
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_base](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_base/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_base).

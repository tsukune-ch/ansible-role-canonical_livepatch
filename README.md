# Ansible Role: Canonical Livepatch

[![CI](https://github.com/tsukune-ch/ansible-role-canonical_livepatch/workflows/CI/badge.svg?event=push)](https://github.com/tsukune-ch/ansible-role-canonical_livepatch/actions?query=workflow%3ACI)
[![Ansible Role](https://img.shields.io/ansible/role/49018)](https://galaxy.ansible.com/tsukune_ch/canonical_livepatch)
![Ansible Role](https://img.shields.io/ansible/role/d/49018)
![Ansible Quality Score](https://img.shields.io/ansible/quality/49018)

Installs and configures the [Canonical Livepatch Service](https://ubuntu.com/livepatch) on Ubuntu servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    canonical_livepatch_token: ""

The token under which Canonical Livepatch will use.

If you don't have a token yet, you can get one [here](https://auth.livepatch.canonical.com/).

When using this role with a public repository or a private repository managed by more than one person,
I strongly recommend that you encrypt this value using [ansible-vault](https://docs.ansible.com/ansible/latest/user_guide/vault.html).

## Dependencies

None.

## Example Playbook

    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
        - tsukune_ch.canonical_livepatch

*Inside `vars/main.yml`*:

    canonical_livepatch_token: [YOUR_TOKEN_HERE]

## License

MIT

## Author Information

This role was created in 2020 by [tsukune-ch](https://github.com/tsukune-ch).

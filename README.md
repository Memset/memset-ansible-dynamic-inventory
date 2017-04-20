# Memset Ansible Dynamic Inventory

This will allow you to create a dynamic Ansible inventory for your Memset servers, using the [Memset API](https://www.memset.com/apidocs/).

## Installation

If you already have a `/etc/ansible/hosts` file, rename this to `/etc/ansible/hosts-local`.

Create a folder in its place: `/etc/ansible/hosts`.

Clone or download this repository to your local machine, and move `memset` to `/etc/ansible/hosts`, ensuring that it is executable.

You can merge the backup (`/etc/ansible/hosts-local`) with the file `hosts-local` in this repository, to mix dynamic and static groups.

## Usage

This creates the Ansible host groups:

[memset-linux], [memset-windows], [memset-reading], [memset-dunsfold]

This also creates the Ansible variables, listed in [Docs/Variables.md](Docs/Variables.md)

The variable ANSIBLE_MEMSET_KEY must be exported before running any ansible command:
```
export ANSIBLE_MEMSET_KEY=XXXXXX
```

You can now access your Memset hosts through ansible:
```
ansible memset-linux -m ping
ansible memset-reading -l memset-linux -m ping
```

## API Key Requirements
API key must have access to at least:
`method:server.list`, `method:server.info` & `method:service.info`

## License

This is free software under the terms of MIT the license (check the COPYING file included in this repository).

## Contact and support

The project website is at:

  * https://github.com/memset/memset-ansible-dynamic-inventory

There you can file bug reports, ask for help or send pull requests.

## Authors

  * Tom Whitwell <tom.whitwell@memset.com>

Contributors
------------

  * Your name goes here!

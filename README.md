# Memset Ansible Dynamic Inventory

This will allow you to create a dynamic Ansible inventory for your Memset servers, using the [Memset API](https://www.memset.com/apidocs/).

## Installation

If you already have a `/etc/ansible/hosts` file, rename this to `/etc/ansible/hosts-local`.

Create a folder in its place: `/etc/ansible/hosts`.

Clone or download this repository to `/etc/ansible/hosts`, ensuring that `/etc/ansible/hosts/memset` is executable.

You can merge the backup (`/etc/ansible/hosts-local`) with the file `hosts-local` in this repository.

## Usage

This creates the Ansible host groups:

[memset-linux], [memset-windows], [memset-reading], [memset-dunsfold]

The variable MEMSET_KEY must be exported before running any ansible command:
```
export MEMSET_KEY=XXXXXX
```

You can now access your Memset hosts through ansible:
```
ansible memset-linux -m ping
ansible memset-reading -l memset-linux -m ping
```

## API Key Requirements
API key must have access to at least:
`method:server.list`, `method:server.info` & `method:service.info`

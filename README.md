[![Actions Status - Master](https://github.com/juju4/ansible-brim/workflows/AnsibleCI/badge.svg)](https://github.com/juju4/ansible-brim/actions?query=branch%3Amaster)
[![Actions Status - Devel](https://github.com/juju4/ansible-brim/workflows/AnsibleCI/badge.svg?branch=devel)](https://github.com/juju4/ansible-brim/actions?query=branch%3Adevel)

# brim ansible role

Install [Brimsec Brim](https://github.com/brimsec/brim/), an open source desktop application for security and network specialists

## Requirements & Dependencies

### Ansible

It was tested on the following versions:
 * 2.10

### Operating systems

Tested on Ubuntu 18.04, 20.04, Centos 7 and 8.

## Example Playbook

Just include this role in your list.
For example

```
- host: myhost
  roles:
    - juju4.brim
```

you probably want to review variables

## Variables

```
brim_version: v0.24  # should match github tag
brim_checksum: "sha256:xxx"  # optional
```


## Continuous integration

This role has a molecule test suite with docker.

```
$ pip install molecule docker
$ molecule test
$ MOLECULE_DISTRO=ubuntu:20.04 molecule test --destroy=never
```

## Troubleshooting & Known issues

N/A

## License

BSD 2-clause


# ansible-role-elrepo

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-elrepo.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-elrepo)

RHEL/CentOS - ELRepo Project

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    elrepo_pkg: elrepo-release
    elrepo_rel: "{{ ansible_distribution_major_version }}"
    elrepo_repos:
      elrepo: False
      elrepo_extras: False
      elrepo_kernel: False
      elrepo_testing: False

The version of the kernel you want to install, mainline or long term. Defaults to mainline.

    elrepo_version: ml
    elrepo_version: lt

Boolean that determines if we want to install the elrepo kernel or not. Defaults to true.

    elrepo_install_kernel: true

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    ---
    - hosts: servers
      gather_facts: true
      vars:
        elrepo_repos:
          elrepo: True
          elrepo_extras: True
          elrepo_kernel: True
          elrepo_testing: False
        elrepo_install_kernel: true
      roles:
        - role: pgporada.elrepo
    ...

## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org). Forked by Phil Porada.

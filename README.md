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

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.elrepo
          elrepo_repos:
            elrepo: True

## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).

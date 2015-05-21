# Ansible Role: Swap

[![Ansible Galaxy](http://img.shields.io/badge/galaxy-novuso.swap-000000.svg)](https://galaxy.ansible.com/list#/roles/3867)
[![MIT License](http://img.shields.io/badge/license-MIT-003399.svg)](http://opensource.org/licenses/MIT)

An Ansible role that manages swap space on Ubuntu 14.04

## Requirements

None

## Role Variables

Ansible variables are listed here along with their default values:

`swap_file` sets the swap file location.

    swap_file: "/swapfile"

`swap_size` sets the swap file size in megabytes.

    swap_size: "1024"

`swap_swappiness` sets the `vm.swappiness` setting.

    swap_swappiness: 10

`swap_vfs_cache_pressure` sets the `vm.vfs_cache_pressure` setting.

    swap_vfs_cache_pressure: 50

`swap_use_dd` flags to use `dd` if `fallocate` doesn't work.

    swap_use_dd: false

## Dependencies

None

## Example Playbook

    ---
    - hosts: all
      vars:
      - swap_size: "2048"
      roles:
      - novuso.swap

## License

This is released under the [MIT license](http://opensource.org/licenses/MIT).

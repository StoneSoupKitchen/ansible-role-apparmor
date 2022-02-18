[![CI](https://github.com/StoneSoupKitchen/ansible-role-apparmor/actions/workflows/ci.yml/badge.svg)](https://github.com/StoneSoupKitchen/ansible-role-apparmor/actions/workflows/ci.yml)

# Ansible role: apparmor

An Ansible role for configuring apparmor on Linux systems.

## Requirements

Supported operating systems:
* Debian 10 (Buster)
* Debian 11 (Bullseye)

## Role Variables

The following table lists all variables that can be overridden
and their default values.

| Name                     | Default Value | Description                      |
| ------------------------ | ------------- | -------------------------------- |
| `apparmor_package` | apparmor | Name of the apparmor package. Use `name=ver` format to pin. |
| `apparmor_package_state` | present | Installation state for apparmor package. |
| `apparmor_utils_package` | apparmor-utils | Name of the apparmor-utils package. Use `name=ver` format to pin. |
| `apparmor_utils_package_state` | present | Installation state for apparmor-utils package. |

## Examples

```yaml
- hosts: all
  roles:
    - stonesoupkitchen.apparmor
```

## Development

A Makefile is included for easier development with `pipenv`.
After cloning this repository,
use the following commands to set up an environment.

    pipenv install --dev

To lint your changes with ansible-lint:

    make lint

To run tests with molecule:

    make test

## License

See [LICENSE](./LICENSE).


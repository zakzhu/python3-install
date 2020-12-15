# Python3-Install

<!-- [![build status][shield-build]][info-build] -->
<!-- [![gitter room][shield-gitter]][info-gitter] -->

[![license][shield-license]][info-license]
[![release][shield-release]][info-release]
[![prs welcome][shield-prs]][info-prs]

Ansible playbook for python3 installation.

[TOC]

## Requirements

- **Platforms:**
  - CentOS-7
- **Dependencies:**
  - ansible

## Installation

```bash
yum -y install ansible
```

```bash
git clone https://github.com/zakzhu/python3-install.git
```

## Usage

```bash
vim python3-install/inventories/production/host_vars/localhost.yml
```

> EXAMPLE:
>
> ```yaml
> deploy_root: /usr/local
>
> package:
>   name: python
>   alias: python
>   version: "3.7.9"
>   dgst_algo: md5
>   checksum: 389d3ed26b4d97c741d9e5423da1f43b
>   type: source
>
> package_url: "https://www.python.org/ftp/python/3.7.9/Python-3.7.9.tar.xz"
> ```

```bash
ansible-playbook -i inventories/production/inventory site.yml
```

## Contributing

See the [contribution guide][info-contribute].

## Frequently asked questions

Please see [FAQ.md][info-faq] for frequently asked questions.

## Thanks

The following excellent people helped massively:

- [Rowan Manning](https://rowanmanning.com)

## License

Python3-Install is licensed under the [BSD-3-Clause][info-license] license.
Copyright &copy; 2020, Zak Zhu

[info-build]: https://travis-ci.org/github/zakzhu/python3-install
[info-contribute]: CONTRIBUTING.md
[info-faq]: FAQ.md
[info-gitter]: https://gitter.im/zakzhu/python3-install
[info-license]: LICENSE
[info-release]: https://github.com/zakzhu/python3-install/releases
[info-prs]: https://github.com/zakzhu/python3-install/pulls
[shield-build]: https://img.shields.io/travis/zakzhu/python3-install
[shield-gitter]: https://img.shields.io/gitter/room/zakzhu/python3-install
[shield-license]: https://img.shields.io/github/license/zakzhu/python3-install
[shield-release]: https://img.shields.io/github/v/release/zakzhu/python3-install
[shield-prs]: https://img.shields.io/badge/PRs-welcome-brightgreen

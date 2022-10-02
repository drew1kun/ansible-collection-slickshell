# Ansible Collection - drew1kun.slickshell

[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Role][collection-badge]][galaxy-link]

This collection contains Ansible roles to make your shell experience on Mac and Linux hosts slick.
It is also a dependency for my workstation setup Ansible playbook.

The roles included:

  - `drew1kun.slickshell.ohmyzhs` ([doc](https://github.com/drew1kun/ansible-collection-slickshell/blob/main/roles/ohmyzsh/README.md))
  - `drew1kun.slickshell.vim` ([doc](https://github.com/drew1kun/ansible-collection-slickshell/blob/main/roles/vim/README.md))
  - `drew1kun.slickshell.mpd` ([doc](https://github.com/drew1kun/ansible-collection-slickshell/blob/main/roles/mpd/README.md))

## Installation

Install via Ansible Galaxy:

```
ansible-galaxy collection install drew1kun.slickshell
```

Or include this collection in your playbook's `requirements.yml` file:

```yaml
---
collections:
- name: drew1kun.slickshell
  version: '*'
  type: galaxy
```
And run:
```
ansible-galaxy install -r requirements.yml
```

## Usage

**NOTE:** For maximum slickness, consider using my [drew1kun.fancyfonts collection][fancyfonts-collection-link]

[![FancyFonts Galaxy Role][fancyfonts-collection-badge]][fancyfonts-galaxy-link]

Example of the play:

```yaml
- hosts: localhost
  connection: local
  collections:
  - drew1kun.fancyfonts
  - drew1kun.slickshell
  roles:
    - nerdfonts
    - terminus_powerline
    - ohmyzsh
    - vim
    - mpd
```

## License

[MIT][mit-link]

## Author Information

Andrew Shagayev | [e-mail](mailto:drew-kun@protonmail.com)

[collection-badge]: https://img.shields.io/badge/collection-drew1kun.slickshell-green.svg
[galaxy-link]: https://galaxy.ansible.com/drew1kun/slickshell
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/drew1kun/ansible-collection-slickshell/main/LICENSE
[fancyfonts-collection-badge]: https://img.shields.io/badge/collection-drew1kun.fancyfonts-green.svg
[fancyfonts-collection-link]: https://github.com/drew1kun/ansible-collection-fancyfonts
[fancyfonts-galaxy-link]: https://galaxy.ansible.com/drew1kun/fancyfonts

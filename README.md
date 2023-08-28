# Ansible Role: Amok Exifsorter

Install Amok Exifsorter via download.

- Download and verify (md5) the specified Amok Exifsorter
- Install to `/opt`
- Create Menu-Entry for all users

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

| Name           | Default Value   | Description                        |
| -------------- | --------------- | -----------------------------------|
| `download_dir_on_remote_host` | "/home/{{ ansible_user }}/Downloads/automatically_by_ansible_playbook" | Download Base Directory on Remote Host |
| `amok_exifsorter.version` | "3.2.0-linux_x86_64" | Amok Exifsorter Version you want to install |
| `amok_exifsorter.checksum` | "md5:1e84aacf9f870b68710dd588fed020df" | Checksum of the version to be downloaded |

## Dependencies

None.

## Example Playbook

```yaml
---
- hosts: all
  gather_facts: yes
  become: true

  roles:
    - role: jakoblichterfeld.amok_exifsorter

```

## License

MIT

## Author Information

This role was created in 2023 by [Jakob Lichterfeld](https://github.com/JakobLichterfeld).

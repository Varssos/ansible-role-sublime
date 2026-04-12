# sublime

Ansible role to install [Sublime Text](https://www.sublimetext.com/) editor on Debian/Ubuntu systems.

## Requirements

- Debian or Ubuntu host
- `become: true` privileges (sudo)

## Role Variables

| Variable | Default | Description |
|---|---|---|
| `sublime_package_name` | `sublime-text` | Package name to install via apt |
| `sublime_gpg_key_url` | `https://download.sublimetext.com/sublimehq-pub.gpg` | URL to the GPG signing key |
| `sublime_gpg_key_tmp` | `/tmp/sublimehq-pub.gpg` | Temporary path for the downloaded GPG key |
| `sublime_gpg_keyring` | `/etc/apt/keyrings/sublimehq-pub.gpg` | Path for the converted keyring file |

## Example Playbook

```yaml
- hosts: all
  become: true
  roles:
    - role: sublime
```

## License

MIT

## Author

Varssos
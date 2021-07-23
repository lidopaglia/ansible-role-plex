# Ansible Role: Plex

[![CI](https://github.com/lidopaglia/ansible-role-plex/actions/workflows/ci.yml/badge.svg)](https://github.com/lidopaglia/ansible-role-plex/actions/workflows/ci.yml)
[![Ansible Galaxy](https://img.shields.io/badge/Ansible%20Galaxy-plex-blue.svg)](https://galaxy.ansible.com/lidopaglia/ansible-role-plex)

An Ansible Role to install [Plex Media Server][0] on Debian / Ubuntu.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

### Enforce the package state (e.g. `present`, `absent`, or `latest`).

Controls whether the `plexmediaserver` service is started and enabled on system boot:

```
plex_service_state: started
plex_service_enabled: true
```

### Specify a custom `Preferences.xml` file.

The template to use for the Plex `Preferences.xml` file, and the path to which the config file will be written.

```
plex_config_template: plex_preferences.xml.j2
plex_config_file_path: /var/lib/plexmediaserver/Library/Application Support/Plex\ Media\ Server/Preferences.xml
```

### Server IP address and Port

The FQDN or IP address and port Plex should use.

```
plex_server_port: 32400
plex_server_host: "0.0.0.0"
```

## Dependencies

None

## Example Playbook

```yaml
- hosts: plex
  roles:
    - lidopaglia.plex
```

## License

MIT

## Author

Created by Lido Paglia.

[0]: https://www.plex.tv/
[1]: https://support.plex.tv/articles/201105343-advanced-hidden-server-settings/
[2]: https://forums.plex.tv/t/customizing-your-plex-configuration/205443

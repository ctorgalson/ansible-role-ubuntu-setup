# Ansible Role Ubuntu Setup

This is a very simple Ansible role designed to perform various first-run
installation (using `apt` and `deb`) and setup tasks on Ubuntu.

# Role Variables

| Variable name | Default value | Description |
|---------------|---------------|-------------|
| `apt_packages`      | `[]`                   | A list of package names to install. |
| `apt_removals`      | `[]`                   | A list of package names to uninstall. |
| `default_keyserver` | `keyserver.ubuntu.com` | Default keyserver to use when adding PPAs. |
| `ubuntu_release`    | `yakkety`              | Default ubuntu version name to use when adding PPAs. |
| `ppas`              | `[]`                   | A list of PPAs to install. Each item in the array should include `source`, `fingerprint`, and `keyserver`. See `defaults/main.yml` for examples. |
| `no_ppa_packages`   | `[]`                   | A list of `*.deb` packages to install directly. May be a path on the remote machine or a URL (since Ansible 1.6). |
| `default_user`      | `someuser`             | A valid username. |
| `default_group`     | `somegroup`            | A valid groupname. |
| `default_files`     | `[]`                   | A list of files, links, or directories containing (at minimum) `dest`, and `state` for each item. See Ansible's [File module](http://docs.ansible.com/ansible/file_module.html) and `defaults/main.yml` for details. |
| `vagrant_plugins`   | `[]`                   | A list of Vagrant plugins to install. The related task does not currently verify the presence of Vagrant. |
| `gtk_theme`         | `Arc-Darker`           | Theme name for setting `org.gnome.desktop.interface.gtk-theme`. |
| `icon_theme`        | `Paper`                | Icon theme name for setting `org.gnome.desktop.interface.icon-theme`. |
| `theme`             | `Arc-Darker`           | Window manager theme name for setting `org.gnome.desktop.wm.preferences.theme`. |

## License

MIT

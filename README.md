# Ansible: The Lounge for ArchLinux

This Playbook installs and configures [TheLounge](https://thelounge.chat/) on an Arch Linux host. The [ansible-aur](https://github.com/kewlfft/ansible-aur) module is used to install [thelounge](https://aur.archlinux.org/packages/thelounge/) and any other AUR packages such as [nodejs-jsonlint](https://aur.archlinux.org/packages/nodejs-jsonlint/).

### Usage
First ensure there are no major issues reported before removing `--check` verification.

`ansible-playbook --check --diff thelounge.yml`

## Config variables
```
thelounge_home: "/etc/thelounge"
thelounge_public: "true"
thelounge_users: []
thelounge_port: 9000
thelounge_reverse_proxy: "false"
thelounge_max_history: 10000
thelounge_enable_https: "true"
thelounge_https_key: ""
thelounge_https_cert: ""
thelounge_https_ca: ""
thelounge_prefetch: "true"
thelounge_prefetch_storage: "true"
thelounge_prefetch_max_image_size: 2048
thelounge_enable_file_upload: "true"
# metric: kilobytes
thelounge_max_file_upload_size: 10240
thelounge_leave_message: "The Lounge - https://thelounge.chat"
thelounge_display_network: "true"
thelounge_lock_network: "true"
# can also use `default` theme
thelounge_default_theme: "thelounge-theme-solarized"
thelounge_install_themes: "True"
thelounge_themes:
  - thelounge-theme-abyss
  - thelounge-theme-amoled
  - thelounge-theme-ion
  - thelounge-theme-light
  - thelounge-theme-material
  - thelounge-theme-solarized
  - thelounge-theme-zenburn
# IRC network
network_name: "MyNetwork"
network_host: "irc.example.tld"
network_port: 6697
network_password: ""
network_enable_tls: "true"
network_reject_unauthorized: "true"
network_nick: "thelounge%%"
network_username: "thelounge"
network_realname: "The Lounge User"
network_join_channels: "#foo, #bar"
# Debug
thelounge_debug:
  irc_framework: false
  raw: false
```

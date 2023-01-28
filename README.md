# docker-mod-terminfos

A Docker mod for linuxserver.io Docker images to install terminfo entries.

This mod currently installs the following terminfo entries:
- rxvt-unicode-256color
- xterm-kitty

## How to use

Set `DOCKER_MODS=ghcr.io/neingeist/docker-mod-terminfos`.

For example, in a `docker-compose.yml` file for an openssh-server container:

```
# [...]
services:
  sshd-halde:
    image: lscr.io/linuxserver/openssh-server:latest
    # [...]
    environment:
      - DOCKER_MODS=linuxserver/mods:universal-package-install|ghcr.io/neingeist/docker-mod-terminfos
      - INSTALL_PACKAGES=tmux|vim|ncdu
# [...]
```

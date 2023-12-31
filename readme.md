# James' Ansible configs

These playbooks should make it quicker to set up new personal computers.

## Manual step

### Linux

#### User

- Set a password

#### Qutebrowser

Set it as the default:

```bash
xdg-settings set default-web-browser org.qutebrowser.qutebrowser.desktop
```

Install the English dictionary:

```bash
/usr/share/qutebrowser/scripts/dictcli.py install en-US
```

#### spotify-tui

In order for the Spotify part of waybar to work, you need to authenticate with
Spotify:

```bash
spt
```

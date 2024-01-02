# James' Ansible configs

These playbooks should make it quicker to set up new personal computers.
If you're not me, feel free to use them, but know that I have some me-specific
things in them (like a hard-coded "james" username) that you'll want to change.

## Linux usage

Note that these steps all assume that you're setting up Arch Linux with Wayland
and Sway on an Intel laptop with integrated graphics.

For new systems, you'll need to follow [the installation guide](https://wiki.archlinux.org/title/Installation_guide).

One you're booted into the newly installed OS and logged in as a non-root user
with a password, install some dependencies:

```bash
pacamn -S git ansible ansible-core neovim
```

Then clone this repo:
```bash
git clone https://github.com/jamesbvaughan/ansible && cd ansible
```

Allow the `wheel` group to use `sudo`:
```bash
EDITOR=nvim visudo
```

Run the main playbook:
```bash
ansible-playbook main.yaml
```

### Extra steps

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

## macOS usage

At this point, these playbooks don't do much for macOS.
Eventually, I'd like to use them to keep installed dev utilities and things in
sync between my Mac and Linux workstations.

For now, I just have one playbook intended for use on macOS:
```bash
ansible-playbook playbooks/packages-macos.yaml
```

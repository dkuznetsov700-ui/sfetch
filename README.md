# sfetch

A minimal, customizable system info fetcher written in Python — my personal alternative to fastfetch/neofetch.

![screenshot](screenshot.png)
![screenshot](screenshot2.png)
![screenshot](screenshot3.png)
## Features

- Distro detection via `/etc/os-release`
- Kernel, uptime, shell, CPU model, RAM usage
- Per-distro ASCII art
- ANSI-colored output
- Zero config, single file, pure Python

## Supported distros
  - Arch, CachyOS, Ubuntu, Debian, Fedora, Linux Mint, RHEL, Gentoo, openSUSE, Alpine. Unknown distros fall back to a generic ASCII art with no color.

- Want to add yours? Add an elif distro == "your_id": branch in sfetch.py with an ASCII art, and a color entry in dcolors.

## Requirements

- Python 3.10+
- Linux (reads `/proc`, `/etc/os-release`)
- `psutil`

## Install

### With pipx (recommended)

```bash
pipx install git+https://github.com/dkuznetsov700-ui/sfetch
```
### If you dont have pipx yet:
```bash
# Arch based
sudo pacman -S python-pipx
pipx ensurepath

# Debian / Ubuntu based
sudo apt install pipx
pipx ensurepath
```
### From source
```bash
git clone https://github.com/dkuznetsov700-ui/sfetch
cd sfetch
python -m venv .venv
source .venv/bin/activate
pip install -e .
```

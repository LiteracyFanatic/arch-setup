# arch-setup
This is a system configuration script meant to be used after completing an installation of Arch Linux. Running it will do the following:

- Configure makepkg to use all available cores
- Perform a full system upgrade
- Populate the mirror list using [reflector](https://xyne.archlinux.ca/projects/reflector/)
- Download, build, and install the AUR helper [yay](https://github.com/Jguer/yay)
- Install packages
- Install and modifie system configuration files under /etc/
- Enable a number of systemd services

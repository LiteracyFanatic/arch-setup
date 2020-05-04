# arch-setup
`arch-setup` is a bash script meant to be used after completing an installation of Arch Linux. Running it will do the following:

- Configure makepkg to use all available cores
- Perform a full system upgrade
- Populate the mirror list using [reflector](https://xyne.archlinux.ca/projects/reflector/)
- Download, build, and install the AUR helper [yay](https://github.com/Jguer/yay)
- Install packages
- Install and modify system configuration files under /etc/
- Enable a number of systemd services

The package lists are sorted automatically by a pre-commit git hook which can be installed by running `ln -sr hooks/* .git/hooks/`.

Some additional useful scripts are included. `tracked-pkgs` expands package groups to print the list of packages which will be installed by `arch-setup`. It accepts the following flags to modify its behavior: `-e/--explicit` and `-d/--deps`. `missing-pkgs` prints a list of packages which should be installed but are not present. `untracked-packages` lists all explicitly installed packages which aren't managed by `arch-setup`. This lets you install packages to try them out and see if you like them before adding them to `arch-setup`. Later you can run `untracked-packages` and decided whether you want to keep each package and add it to the package list or remove it from your system.

This branch is for a Raspberry Pi 3 which I use to run an MPD server, display music visualizations, and perform network backups to an external hard drive. The mirror list is not modified because the default mirror for Arch Linux Arm automatically redirects to the geographically closest mirror.

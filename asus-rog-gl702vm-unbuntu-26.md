# ASUS ROG GL702VM Ubuntu 26

## BIOS

* Had to disable Secure Boot
* Had to enable CSM boot
* Had to fix Clock in BIOS for installer to not shit its pants since HTTPS calls would fail due to bad cert checks

## Gotchas
* Didn't work at first. Burnt USB with BelanaEtcher and worked
* Installer was a mother-fucker, had to tend to Interactive Installer and not let it sit, otherwise it would crash (might have been due to BIOS clock being fucked)

## Installing

* Used drive encryption w/ passphrase, because fuck trying to get secureboot working with the TPM

## Post-install

### Updates

```bash
sudo apt-get update && sudo apt-get upgrade -y
```

### (Oh!) Snaps

* Update Snaps
* Remove FireFux
* Install Brave Browser
* Install KeePassXC
* Install ONLYOFFICE

### Non-Snaps
* Install Private Internet Access desktop client
  * Need to `sudo apt install -y libopeng10` first
* Install `asusctl` https://github.com/OpenGamingCollective/asusctl
  * Need to `sudo apt install gettext` first
* Install podman
  * Need to `sudo apt install podman` first
* Install podman desktop via flatpak
  * Need to `sudo apt install flatpak`
  * `flatpak remote-add --user --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo`
  * `flatpak install flathub org.freedesktop.Platform//26.08`
  * `flatpak install flathub org.freedesktop.Sdk//26.08`
  * `flatpak install -y --user ~/Downloads/podman-desktop-1.31.0.flatpak`
  * Install podman compose extension
  * `alias docker=podman`
* Install DropBox and login
* Install Raspberry Pi Imager
* Install BalenaEtcher

## Useful commands

* BIOS infos
  * `cat /sys/class/dmi/id/bios_version`
  * `sudo dmidecode -t bios`

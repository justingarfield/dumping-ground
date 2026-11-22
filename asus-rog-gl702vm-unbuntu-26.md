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
* Install DropBox and login
* Install Raspberry Pi Imager
* Install BalenaEtcher

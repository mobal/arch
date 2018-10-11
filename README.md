
# Arch Linux notes

## aurman

AUR helper with almost pacman syntax

### Install:

First install ```base-devel``` and ```python``` packages if missing. Clone the GitHub repository and install the compiled package:

```
git clone https://aur.archlinux.org/aurman.git
cd aurman
makepkg -si
```
### Using aurman:

Search for application:

```
aurman -Ss <package>
```

Install an application using aurman:

```
aurman -S <package>
```

## Transmission

Blocklist:

```console
http://john.bitsurge.net/public/biglist.p2p.gz
```

If you have **IPv4** and **IPv6** addresses at once, port checking is not working. To solve, add the following line to the ```/etc/hosts``` file:

```console
87.98.162.88 portcheck.transmissionbt.com
```

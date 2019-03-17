
# Arch Linux notes

## aurman

AUR helper with almost pacman syntax. **Since August 2018, the development has stopped. Use yay instead**.

### Install:

First install ```base-devel``` and ```python``` packages if missing. Clone the GitHub repository and compile:

```
git clone https://aur.archlinux.org/aurman.git
cd aurman
makepkg -si
```
### Using aurman:

Search for packages:

```
aurman -Ss <package>
```

Install a package using aurman:

```
aurman -S <package>
```

## yay

Yet another Yogurt - An AUR Helper written in Go

### Installation:

First install ```base-devel``` package. Clone the GitHub repository and compile:

```
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

### Using yay:

Search for packages:

```
yay -Ss <package>
```

Install a package using yay:

```
yay -S <package>
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

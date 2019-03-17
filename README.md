
# Arch Linux notes

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

## zsh

The Z shell (Zsh) is a Unix shell that can be used as an interactive login shell and as a command interpreter 
for shell scripting. Zsh is an extended Bourne shell with a large number of improvements, including some 
features of Bash, ksh, and tcsh. (from Wikipedia)

### Installation:

```
pacman -S zsh
```

Change your default shell using the ```chsh``` command.

To list all installed shells, run:

```
chsh -l
```

And to set ```zsh``` as default for your user do:

```
chsh -s /bin/zsh
```

Default bash configuration for zsh:

```
export PS1="[$USER@%m %1~]$ "
alias ls="ls --color=auto"
```


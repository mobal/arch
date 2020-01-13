
# Arch Linux notes

## yay

Yet another Yogurt - An AUR Helper written in Go

### Installation:

First install ```base-devel``` package. Clone the GitHub repository and compile:

```
git clone https://aur.archlinux.org/yay-bin.git
cd yay-bin
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
bindkey "${terminfo[kich1]}" overwrite-mode
bindkey "${terminfo[kdch1]}" delete-char
bindkey "${terminfo[khome]}" beginning-of-line
bindkey "${terminfo[kend]}" end-of-line
bindkey "${terminfo[kpp]}" up-line-or-history
bindkey "${terminfo[knp]}" down-line-or-history
```

## Adopt OpenJDK

AdoptOpenJDK provides rock-solid OpenJDK binaries for the Java ecosystem and also provides infrastructure as code, and a Build farm for builders of OpenJDK, on any platform.

[https://adoptopenjdk.net/](https://adoptopenjdk.net/)

### Installation:

Install ```java-environment-common``` and ```java-runtime-common``` packages:

```
pacman -S java-environment-common
pacman -S java-runtime-common
```

Extract the downloaded binary to ```/usr/lib/jvm/<package>``` (for example: ```jdk-11.0.3+7``` or ```jdk8u212-b03```).

Use ```archlinux-java status``` to list all available Java environments:

```
[mobal@think arch (master)]$ archlinux-java status
Available Java environments:
  jdk-11.0.3+7
  jdk8u212-b03 (default)
```

Using ```archlinux-java set``` force <JAVA_ENV> as default:

```
archlinux-java set jdk8u212-b03
```

Check whether the change was successful:

```
java -version
javac -version
```


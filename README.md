
# Arch Linux notes

## Transmission

Blocklist:

```console
http://john.bitsurge.net/public/biglist.p2p.gz
```

If you have **IPv4** and **IPv6** addresses at once, port checking is not working. To solve, add the following line to the ```/etc/hosts``` file:

```console
87.98.162.88 portcheck.transmissionbt.com
```

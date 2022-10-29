# snell

An encrypted proxy service program

## Highlights

* Extreme performance.
* Snell v2 supports reusing TCP connections to improve performance and reduce latency.
* Single binary with zero dependency. (except glibc)
* A wizard to help you start.
* Traffic obfuscating is embedded. (HTTP & TLS)
* Proxy server will report remote errors to client if encounters. Clients may choose countermeasures for different scenarios.
* The server-side program is able to auto-negotiate cipher and version with clients.
* Protocol is ready for multiple users ACL. (No implementation yet)

## Please use root users to run

## Auto install (use systemd for autostart)

1. Debian & Ubuntu users please run
```
wget https://github.com/Kingsmanvn-Official/snell/raw/master/install-snell.sh
chmod +x install-snell.sh
./install-snell.sh
```

2. Centos & RedHat users please run
```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/Kingsmanvn-Official/snell/master/install-snell.centos.sh
chmod +x install-snell.sh
./install-snell.sh
```

## The default end slogan `443` and psk `kingsmanvn` was installed for the first time, please modify it Run after all scripts are run
```
vi /etc/snell/snell-server.conf
systemctl restart snell
```

## View the running status：
```
systemctl status snell
```

## Unloading method：
```
wget --no-check-certificate -O uninstall-snell.sh https://raw.githubusercontent.com/primovist/snell.sh/master/uninstall-snell.sh
chmod +x uninstall-snell.sh
./uninstall-snell.sh
```

## Add a proxy line in Surge  (The latest beta version is required):
```
Proxy = snell, [SERVER ADDRESS], 443, psk=kingsmanvn, obfs=tls
```

## Opens Source

We haven't decided whether to open source the project for complicated reasons.

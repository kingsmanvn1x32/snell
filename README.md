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

## Auto install on Ubuntu (use systemd for autostart)

1. Run on terminal
```
wget https://github.com/Kingsmanvn-Official/snell/raw/master/install-snell.sh
./install-snell.sh
```

2. Wait install.

3. Done on server.

4. Add a proxy line in Surge  (The latest beta version is required):
    * `Proxy = snell, [SERVER ADDRESS], 443, psk=kingsmanvn, obfs=tls`

## Change the value of `psk` in [`install-snell.sh`](./install-snell.sh)

## Opens Source

We haven't decided whether to open source the project for complicated reasons.

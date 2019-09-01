### Scanner un squid

```
nmap -sV -p 3128 192.42.185.3
PORT     STATE SERVICE    VERSION
3128/tcp open  http-proxy Squid http proxy 3.5.12
```

`curl -x 192.42.185.3:3128 127.0.0.1`

[Proxychains](https://github.com/haad/proxychains)

```
[Après avoir modifié le fichier /etc/proxychains.conf en rajoutant une ligne 'http <IP> <port>'
et en commentant la ligne socks 4]
proxychains nmap -sV -sT -p- 127.0.0.1
[...]
|S-chain|-<>-192.42.185.3:3128-<><>-127.0.0.1:1337-<><>-OK
|S-chain|-<>-192.42.185.3:3128-<><>-127.0.0.1:3128-<><>-OK
```
### Bruteforcer l'authent du proxy

`nmap --script http-proxy-brute -vv -p 3128 192.113.9.3`

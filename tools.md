### DNS
```
dig -t AXFR <URL> @<DNS SERVER IP> (Zone transfert)
dig -t RRSIG <URL> @<DNS SERVER IP> (DNSSEC)
nmap -R -sL --dns-servers <IP> -Pn <IP RANGE> | grep "("
```

### memcached
```
nmap -p 11211 --script memcached-info <IP>
memcstat --servers=<IP>
memcstat --servers=<IP> --username=<USERNAME> --password=<PASSWORD>
memcdump --servers=<IP>
memccat --servers=<IP> --username=<USERNAME> --password=<PASSWORD> <KEY>
~/tools/scripts/memcache# bash memcache-dictionary-attack.sh <IP> <USERNAME> <WORDLIST>
```

### nmap
```
Updated script list: https://nmap.org/nsedoc/
```

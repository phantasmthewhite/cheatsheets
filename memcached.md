```
nmap -p 11211 --script memcached-info <IP>
memcstat --servers=<IP>
memcstat --servers=<IP> --username=<USERNAME> --password=<PASSWORD>
memcdump --servers=<IP>
memccat --servers=<IP> --username=<USERNAME> --password=<PASSWORD> <KEY>
~/tools/scripts/memcache# bash memcache-dictionary-attack.sh <IP> <USERNAME> <WORDLIST>
```
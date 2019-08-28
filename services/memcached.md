### NMAP Script
nmap -p 11211 --script memcached-info <IP>

### Infos basiques
memcstat --servers=<IP>

### Authentification
memcstat --servers=<IP> --username=<USERNAME> --password=<PASSWORD>

### Dump la liste des clefs d'un serveur
memcdump --servers=<IP>

### Dump la liste des clefs d'un serveur avec authentification
memccat --servers=<IP> --username=<USERNAME> --password=<PASSWORD> <KEY>
  
### Autre
~/tools/scripts/memcache# bash memcache-dictionary-attack.sh <IP> <USERNAME> <WORDLIST>
```
